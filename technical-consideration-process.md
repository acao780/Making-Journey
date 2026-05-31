# Technical Consideration, Decision, and Learning Process

This document records the technical process used to turn the Figma design for **Your Food Diary Forest** into an interactive frontend application. The goal was not only to reproduce the visual style, but also to make the frontend code modular enough that assets, page sections, and positioned objects can be adjusted without rewriting the whole interface.

## 1. Reading the Figma Design and Choosing the Frontend Framework

At the beginning of the project, we used the Figma design as the source of truth. The first task for Codex was to read the Figma page and understand the design direction, page structure, reusable visual elements, and interaction requirements.

The main technical question was: should this be a static HTML page, a component-based frontend, or a heavier application framework?

We decided to use:

```text
React + Vite + TypeScript
```

This decision was based on several technical considerations.

First, the website is made of repeated and reusable visual sections: a home page, a forest community page, a food diary page, and an about page. Each section has its own layout and assets, but they all share global navigation, full-screen scrolling behavior, fonts, and responsive sizing rules. React gives us a clear way to express each section as a component.

Second, the project needed to support iterative layout tuning. The design depends heavily on exact placement of image assets, text blocks, stamps, windbells, trees, and page decorations. React components plus CSS classes make it easier to isolate a visual element and adjust only its owner component.

Third, TypeScript was selected because it helps keep the page model explicit. For example, the app stores page information in a section configuration structure, and TypeScript helps protect against accidental missing fields or invalid usage.

Finally, Vite was chosen because it is lightweight, fast to start, and suitable for a small interactive frontend. It gives hot reload during development and a simple production build process.

The resulting application uses a single-page structure with full-screen sections. The top navigation remains fixed, while the main content switches between pages.

![Home page screenshot](./assets/technical-consideration/01-home.png)

## 2. Modular Page and Component Structure

One important early decision was to avoid treating the Figma export as one giant static screenshot. A screenshot would look close at one viewport size, but it would be difficult to modify, animate, or make responsive.

Instead, we split the site into logical components:

```text
App
HomePage
ForestCommunityPage
FoodDiaryPage
AboutPage
```

The shared responsibilities stay in `App`, including:

- fixed navigation
- current section state
- hash navigation
- page switching
- scroll and keyboard page transitions

Each page component owns its local visual composition. This means page-specific assets and page-specific positioning rules are kept close together. For example, the food diary page owns the tree stump and diary book layers, while the forest community page owns the ground block and possible tree slots.

The styling was also designed around parent-owned layout. In other words, child assets do not decide their own global position. Their position is defined by the parent page or stage component. This is useful because the same asset can later be reused in a different page or state with different placement rules.

For example, on the food diary page, the tree stump and book were eventually separated into different layers:

```text
diary-stage
  diary-stump
  diary-book
```

This is better than using one merged image, because the book can be moved, scaled, replaced, or animated independently from the stump.

![Food diary page screenshot](./assets/technical-consideration/03-food-diary.png)

## 3. Assetisation Process

The Figma design contained many decorative and illustrative elements: backgrounds, diary assets, food icons, windbell assets, photo stamps, tree stumps, ribbons, and forest ground blocks.

The assetisation process means converting the design into usable frontend assets instead of relying on full-page screenshots.

The intended process was:

1. Use Figma tooling to inspect the design.
2. Extract or reproduce individual visual assets.
3. Save each asset into the project asset folder.
4. Use assets as independent layers in the frontend.
5. Tune placement through CSS.

In practice, the Figma MCP tool had technical limitations. There were call limits, and some asset extraction operations were not always reliable for the exact level of separation we needed. Because of this, we used a hybrid method.

The final asset workflow included:

- using Figma when available to understand the design structure
- using supplied assets from `unsorted_assets`
- using image generation to recreate missing bitmap assets
- using local post-processing to remove chroma-key backgrounds and produce transparent PNGs
- manually splitting important assets into separate layers when needed

For transparent assets, the safe process was to generate the image on a flat chroma-key background and then remove that background locally. This helped avoid accidental rectangular backgrounds around objects. It was especially important for assets like the ribbon, food charms, photo clusters, diary book, and tree stump.

The project now has page-specific asset folders such as:

```text
public/assets/page1
public/assets/page2
public/assets/page3
public/assets/page4
public/assets/fonts
```

This folder structure keeps the asset ownership clear. Page 1 assets are not mixed with page 4 assets, and fonts are shared globally.

## 4. Fonts and Visual Fidelity

The design uses different fonts for different visual roles, so font choice became a key part of the implementation.

The main font decisions were:

```text
Navigation: Life Savers
Home title: Irish Grover
Home button and subtitle: Oranienbaum
Forest page heading: Oranienbaum
Food diary title/button: Oranienbaum
About title: Life Savers
About body copy: Nunito
```

Fonts were loaded locally using `@font-face` so that the result would not depend on browser-installed fonts. This also makes the app more stable during demos or offline development.

One learning point was that visual font matching is not only about font family. Font weight matters. For example, the About title initially used Life Savers bold, but the design needed a softer look, so it was changed to Life Savers regular.

Another learning point was that annotation tools are useful for font and spacing corrections. Instead of guessing, we selected the exact text element in the browser and gave Codex a specific annotation such as:

```text
font-family: Life Savers -> Nunito
```

This made it easier to apply the change to the correct CSS owner rather than changing global styles accidentally.

![About page screenshot](./assets/technical-consideration/04-about-us.png)

## 5. Using Codex Annotations for Precise Styling

Codex is useful for generating code structure, asset wiring, and responsive CSS, but it is not always perfect at exact visual placement. Precise placement is especially hard in a design like this because many elements are decorative images rather than normal rectangular UI components.

Because of this, we used browser annotations as a practical adjustment workflow.

The workflow was:

1. Open the app in the browser.
2. Select a visible element.
3. Add a comment describing the exact desired visual change.
4. Let Codex locate the owning component or CSS selector.
5. Apply the change in source code.
6. Rebuild and visually verify.

This was used for changes such as:

- navigation height
- navigation font
- windbell placement
- photo stamp placement
- About title font
- About body copy font
- centering text
- separating the diary book and tree stump layers

For example, when the diary book and stump were merged into one generated asset, the page looked acceptable but was not flexible. We later separated them into two layers so the book could be adjusted independently:

```tsx
<div className="diary-stage" aria-hidden="true">
  <img className="diary-stump" src="/assets/page3/tree-stump.png" alt="" draggable={false} />
  <img className="diary-book" src="/assets/page3/diary-book.png" alt="" draggable={false} />
</div>
```

This is a good example of how annotation-based iteration led to a better technical structure.

## 6. Full-Screen Page Switching

Another important technical decision was the page transition model.

The website is not a normal continuous scroll page. Each section should take the full screen height, and scrolling should switch from one section to the next without a middle state.

To implement this, the app uses a page track that translates vertically based on the active page index:

```text
page-track height = 400svh
section height = 100svh
active page transform = translateY(-index * 100svh)
```

Wheel, keyboard, touch, and navigation clicks all update the same active section state. This creates a controlled full-page interaction instead of relying on native scrolling.

The navigation stays fixed at the top for all pages.

This interaction model also affected layout calculations. Each page section uses the remaining height after navigation:

```css
inset: var(--nav-height) 0 0;
```

That keeps the page content below the navigation and prevents visual overlap.

## 7. Forest Community and Tree Placement Logic

The forest community page was designed to support future interaction: users will eventually place or grow trees on the ground.

Instead of hard-coding a single tree image into the background, the page defines possible tree placement slots. These slots are currently visual markers, but technically they act like a coordinate system for future tree placement.

The tree slot data is stored as an array:

```ts
const treeSlots = [
  { x: 16, y: 57, size: "small" },
  { x: 25, y: 48, size: "medium" },
  { x: 35, y: 61, size: "small" },
  { x: 43, y: 43, size: "large" },
  { x: 51, y: 55, size: "small" },
  { x: 58, y: 38, size: "medium" },
  { x: 66, y: 52, size: "small" },
  { x: 74, y: 44, size: "large" },
  { x: 82, y: 57, size: "medium" },
];
```

This was an important learning point. Instead of positioning every tree manually in JSX, we define placement data and let the component render it. Later, this can be extended into real user data:

```text
meal entry -> generated tree -> selected slot -> rendered on ground
```

This makes the forest page more modular and easier to turn into an interactive feature later.

![Forest community page screenshot](./assets/technical-consideration/02-forest-community.png)

## 8. Responsive Sizing Strategy

The design needs to work across laptop and desktop screens. A fixed-pixel layout would only match one viewport, so we used responsive CSS units.

Important techniques included:

- `svh` for full-screen section height
- container query units such as `cqw` and `cqh` inside page components
- `clamp()` for font sizes and element sizes
- page-local absolute positioning
- parent-controlled stage containers for grouped assets

For example, instead of giving the diary stage a fixed width, it uses a responsive formula:

```css
width: min(42cqw, calc(62cqh * 1.5));
```

This means the element scales based on both available width and available height. It helps prevent the layout from becoming too large on wide screens or too tall on short screens.

The tradeoff is that exact positioning becomes more complex. Some values still needed manual tuning after visual inspection.

## 9. Testing With Browser and Playwright MCP

After each meaningful frontend change, we used the browser and Playwright MCP workflow to test the app.

The testing process included:

1. Run the production build.
2. Open the app in the browser.
3. Navigate to the target section.
4. Inspect computed styles when needed.
5. Capture screenshots for visual verification.
6. Check whether fonts, sizes, and positions are applied as expected.

Examples of checks included:

```text
fontFamily: "Life Savers", Georgia, serif
fontWeight: 400
fontFamily: Nunito, Arial, sans-serif
textAlign: center
```

This was important because CSS can look correct in source code but still fail in the browser if the font file is missing, the selector is overridden, or the wrong element owns the style.

The build command was used repeatedly:

```bash
npm run build
```

This checks TypeScript and confirms that Vite can produce a production bundle.

## 10. Debugging and Learning Process

The main debugging process was based on understanding the frontend framework and then keeping changes scoped to the correct component.

Because the project was intentionally modular, debugging usually followed this pattern:

1. Identify which page has the issue.
2. Identify which component owns that page.
3. Identify whether the issue is structural JSX, asset preparation, or CSS positioning.
4. Apply the smallest change.
5. Build and visually verify.

This process worked well because each page component is independent. For example, changing the About body font did not require touching the Home page, Forest page, or Food Diary page.

The most important learning was that visual implementation is not only a coding task. It is also a design translation task. Codex can generate a reasonable implementation, but precise visual matching needs a loop:

```text
design reference -> implementation -> screenshot -> annotation -> code adjustment -> verification
```

Another learning was that asset separation matters. A single image is faster at first, but separate layers are better for future interaction. The tree slots, diary book, stump, windbell, photo stamp, and About decorations all benefit from being independent assets.

## 11. Final Technical Direction

The final technical direction is:

- Use React components for each major page.
- Use Vite for fast development and simple builds.
- Use TypeScript for explicit page and data structures.
- Keep assets page-specific and reusable.
- Use local fonts through `@font-face`.
- Use responsive CSS based on parent containers.
- Use browser annotations for precise design corrections.
- Use Playwright/browser MCP for verification.
- Keep interactive elements, such as tree slots, data-driven rather than hard-coded.

This gives the project a flexible base. It can now evolve from a visual prototype into a more interactive application where food diary entries generate trees, wind chimes, or other forest objects.

