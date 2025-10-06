# Screenshot Generation Settings

## Default Resolutions
When generating screenshots for this project, use the following standard resolutions:

- **Mobile**: 375x667 (iPhone SE)
- **Tablet**: 768x1024 (iPad)
- **Desktop**: 1920x1080 (Full HD)
- **Large Desktop**: 2560x1440 (2K)

## Screenshot Storage
- Save all screenshots to `.playwright-mcp/dev/` directory
- Use descriptive filenames with resolution: `{device}-{width}x{height}.png`
- Always use full-page screenshots unless specified otherwise

## Workflow
When asked to generate screenshots:
1. Open the target file using Playwright
2. Resize browser to each resolution
3. Capture full-page screenshot
4. Name files appropriately (e.g., `mobile-375x667.png`)

## Design Rule: No Vertical Scrolling
**IMPORTANT**: The webpage MUST fit within the viewport height at all given screen resolutions without requiring vertical scrolling. All content should be visible within the initial viewport:

- Mobile (375x667): Content must fit in 667px height
- Tablet (768x1024): Content must fit in 1024px height
- Desktop (1920x1080): Content must fit in 1080px height
- Large Desktop (2560x1440): Content must fit in 1440px height

When developing or reviewing the site, ensure all elements are visible without scrolling at each resolution.

## File to Test
- Primary file: `index.html`
