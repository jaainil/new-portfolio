# Portfolio - Jainil Prajapati

A clean, modern portfolio built with Astro showcasing professional experience, projects, and blog posts.

## 🌐 Live Demo

[View Portfolio](https://jaainil.com)

## ✨ Features

- **Experience Section** - Showcase professional experience with detailed cards
- **Projects Showcase** - Display your work with interactive project cards
- **Blog Support** - Share your thoughts and tutorials
- **Responsive Design** - Mobile-friendly and fully responsive
- **SEO Optimized** - Built-in SEO best practices
- **Content Collections** - Organized content management for experience, projects, and blog posts
- **Minimal & Bold Typography** - Clean, modern design aesthetic
- **Contact Form** - Easy way for visitors to get in touch

## 🛠️ Tech Stack

- [Astro](https://astro.build/) – Static site builder
- [TypeScript](https://www.typescriptlang.org/) – Type-safe development
- [Tailwind CSS v4](https://tailwindcss.com/) – Utility-first styling with latest features
- Content Collections – Type-safe content management

## 📁 Project Structure

```text
├── public/
│   ├── favicon.svg
│   └── [images]
├── src/
│   ├── components/
│   │   ├── About.astro
│   │   ├── Card.astro
│   │   ├── Contact.astro
│   │   ├── Experience.astro
│   │   ├── Footer.astro
│   │   ├── FormattedDate.astro
│   │   ├── Head.astro
│   │   ├── Header.astro
│   │   ├── Hero.astro
│   │   ├── Posts.astro
│   │   └── Projects.astro
│   ├── content/
│   │   ├── blog/
│   │   ├── experience/
│   │   └── projects/
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   ├── 404.astro
│   │   ├── about.astro
│   │   ├── blog/
│   │   │   ├── [...id].astro
│   │   │   └── index.astro
│   │   ├── contact.astro
│   │   ├── experience/
│   │   │   ├── [...id].astro
│   │   │   └── index.astro
│   │   ├── index.astro
│   │   └── projects/
│   │       ├── [...id].astro
│   │       └── index.astro
│   ├── styles/
│   │   └── global.css
│   ├── consts.ts
│   └── content.config.ts
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- pnpm (recommended) or npm

### Installation

1. Clone the repository:

```bash
git clone https://github.com/jaainil/new-portfolio.git
cd new-portfolio
```

2. Install dependencies:

```bash
pnpm install
```

3. Start the development server:

```bash
pnpm dev
```

4. Open [http://localhost:4321](http://localhost:4321) in your browser

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                | Action                                           |
| :--------------------- | :----------------------------------------------- |
| `pnpm install`         | Installs dependencies                            |
| `pnpm dev`             | Starts local dev server at `localhost:4321`      |
| `pnpm build`           | Build your production site to `./dist/`          |
| `pnpm preview`         | Preview your build locally, before deploying     |
| `pnpm astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `pnpm astro -- --help` | Get help using the Astro CLI                     |

## 📝 Adding Content

### Experience

Add new experience entries by creating markdown files in `src/content/experience/`:

```markdown
---
title: "Your Position"
description: "Brief description of your role"
company: "Company Name"
location: "Location"
startDate: "Start Date"
endDate: "End Date" # or "Present"
image: { url: "/image.webp", alt: "Image description" }
---

Your detailed experience content here...
```

### Projects

Add new projects by creating markdown files in `src/content/projects/`:

```markdown
---
title: "Project Name"
description: "Project description"
liveUrl: https://example.com
githubUrl: https://github.com/username/repo
image: { url: "/project.webp", alt: "Project image" }
---

Your project details here...
```

### Blog Posts

Add new blog posts by creating markdown files in `src/content/blog/`:

```markdown
---
title: "Post Title"
description: "Post description"
date: 2024-01-01
tags: ["tag1", "tag2"]
image: { url: "/post.webp", alt: "Post image" }
---

Your blog post content here...
```

## 🎨 Customization

### Colors & Styling

Update colors and design tokens in `src/styles/global.css`:

```css
@theme {
  --color-primary: #27ff0b;
  --color-background: #ffffff;
  --color-foreground: #000000;
  /* ... */
}
```

### Site Information

Update site metadata in `src/consts.ts`:

```typescript
export const SITE = {
  URL: "https://yourdomain.com",
  TITLE: "Your Name",
  DESCRIPTION: "Your description",
  EMAIL: "your@email.com",
};
```

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- Built with [Astro](https://astro.build/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)
- Inspired by modern portfolio designs

---

Made with ❤️ by [Jainil Prajapati](https://jaainil.com)
