## Brief overview

Project-specific guidelines for building and maintaining this Astro portfolio. Covers Astro best practices, component architecture, TailwindCSS v4 styling patterns, and consistent design system implementation.

## Astro component structure

- Use Astro's frontmatter syntax (`---`) for imports and logic
- Keep components focused and single-purpose
- Use semantic HTML elements (`<section>`, `<article>`, `<nav>`)
- Add descriptive section IDs for navigation (e.g., `id="About"`, `id="Contact"`)
- Leverage Astro's partial hydration - keep components static when possible
- Import constants from [`@consts`](src/consts.ts) using path aliases

## Import conventions

- Use path aliases: `@components`, `@/components`, `@consts`, `@/styles`
- Organize imports: Astro components first, then utilities/constants
- Example: `import { SITE } from "@consts";` followed by component imports
- Maintain consistency between `@/` and `@` prefix patterns already in use

## TailwindCSS v4 styling

- Use Tailwind v4's new `@import "tailwindcss"` syntax in [`global.css`](src/styles/global.css)
- Define custom theme using `@theme` directive with CSS variables
- Use OKLCH color space for all color definitions for better perceptual uniformity
- Apply the custom `.heading` utility class for all heading elements
- Implement mobile-first responsive design with breakpoints (`sm:`, `md:`, `lg:`)
- Use `clamp()` for fluid typography (e.g., `text-[clamp(4rem,8vw,6rem)]`)

## Design system consistency

- **Colors**: Primary green (`#27FF0B`), black foreground, white background, gray secondary
- **Fonts**: IBM Plex Mono for headings (`.heading`), Geist for body text
- **Spacing**: Consistent gap values (gap-2.5, gap-4, gap-8, p-6)
- **Borders**: Use `outline-1 outline-dashed outline-secondary` for dashed borders
- **Rounded corners**: Large radius values (rounded-2xl, rounded-3xl, rounded-4xl)
- **Transitions**: Add `transition` class for smooth hover effects

## Layout patterns

- Use `container mx-auto` for centered content sections
- Apply grid layouts for responsive designs (`grid grid-cols-1 md:grid-cols-2`)
- Maintain consistent padding (`p-6`) on main sections
- Implement min-height screens for full-viewport sections (`min-h-screen`)
- Use flexbox for button groups (`flex flex-col md:flex-row gap-2.5`)

## Typography hierarchy

- Large uppercase headings using the `.heading` class
- Heading sizes: `text-5xl md:text-9xl` for main titles, `text-2xl` for subtitles
- Body text in secondary color: `text-lg md:text-2xl text-secondary`
- Strong emphasis with `<strong>` tags for key terms
- Consistent letter spacing: `tracking-[-2%]` on headings

## Image optimization

- Use WebP format for all images (`portrait.webp`, `project.webp`)
- Maintain aspect ratios with `aspect-[width/height]` utility
- Apply `object-cover` for responsive images within containers
- Wrap images in `overflow-hidden rounded-3xl` containers
- Store images in [`/public`](public/) directory for static assets

## Interactive elements

- Buttons: Full-width on mobile (`w-full sm:w-auto`), centered content
- Hover states: Background swap with dashed outline (`hover:bg-background hover:outline hover:outline-1 hover:outline-dashed`)
- Use `cursor-pointer` explicitly on clickable elements
- Consistent padding: `py-3 px-6 sm:py-4 sm:px-10` for buttons

## TypeScript usage

- Define Props types in component frontmatter for type safety
- Use TypeScript in Astro config ([`astro.config.mjs`](astro.config.mjs))
- Leverage content collections for type-safe content ([`src/content.config.ts`](src/content.config.ts))

## File organization

- Components in [`src/components/`](src/components/)
- Layouts in [`src/layouts/`](src/layouts/)
- Pages in [`src/pages/`](src/pages/) following file-based routing
- Content collections in [`src/content/`](src/content/)
- Global styles in [`src/styles/`](src/styles/)
- Static assets in [`public/`](public/)
