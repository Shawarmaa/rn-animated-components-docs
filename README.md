# RN Animated Components Documentation

Professional documentation site for React Native Animated Components, built with [Fumadocs](https://fumadocs.dev/) and Next.js.

## Overview

This documentation site showcases a collection of beautiful, performant React Native animated components including:

- **AnimatedNumber** - Smooth number transitions with separators
- **CircleLoader** - Circular animated loader with Skia
- **LiquidSwitch** - Liquid-effect toggle switch 
- **ScratchCard** - Interactive scratch-to-reveal component

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm/yarn/pnpm

### Installation

```bash
# Clone the repository
git clone [repository-url]
cd rn-animated-components-docs

# Install dependencies
npm install

# Start development server
npm run dev
```

Visit `http://localhost:3000` to view the documentation site.

## Project Structure

```
/
├── app/                    # Next.js app router
│   ├── (home)/            # Home page layout
│   ├── docs/              # Documentation layout
│   ├── layout.config.tsx  # Shared layout configuration
│   └── layout.tsx         # Root layout
├── content/docs/          # MDX documentation files
│   ├── components/        # Component documentation
│   ├── getting-started/   # Setup guides
│   ├── faq.mdx           # Frequently asked questions
│   ├── troubleshooting.mdx # Common issues & solutions
│   └── contributing.mdx   # Contribution guidelines
├── public/videos/         # Component demo videos
├── lib/                   # Utilities and configurations
└── source.config.ts       # Fumadocs configuration
```

## How It Works

### Documentation Framework

Built on **Fumadocs**, a modern documentation framework that provides:

- **File-based routing** - MDX files automatically become pages
- **Built-in components** - Cards, Callouts, Accordions, TypeTables
- **Search functionality** - Full-text search across all content
- **Responsive design** - Mobile-friendly navigation and layout
- **Dark mode** - Automatic theme switching

### Content Management

- **MDX Format** - Markdown with JSX components for rich content
- **Frontmatter** - Page metadata (title, description) in YAML
- **Navigation** - Controlled via `meta.json` files in each directory
- **Video Demos** - Local MP4 files for fast loading

## Maintaining Documentation

### Adding New Components

1. **Create component page**:
   ```bash
   touch content/docs/components/my-component.mdx
   ```

2. **Add to navigation**:
   ```json
   // content/docs/components/meta.json
   {
     "title": "Components",
     "pages": ["animated-number", "circle-loader", "my-component"]
   }
   ```

3. **Component page template**:
   ```mdx
   ---
   title: MyComponent
   description: Brief description of the component
   ---
   
   Brief overview of what the component does.
   
   <video src="/videos/my-component.mp4" autoPlay loop muted width="400" height="800" style={{maxHeight: "600px", height: "auto", margin: "0px 0", display: "block"}} />
   
   ## Features
   
   - Feature 1
   - Feature 2
   
   ## Dependencies
   
   ```bash npm2yarn
   npx expo install react-native-reanimated
   ```
   
   ## Usage
   
   [Usage examples and code]
   
   ## Props
   
   import { TypeTable } from 'fumadocs-ui/components/type-table';
   
   <TypeTable
     type={{
       prop1: {
         description: 'Description of prop',
         type: 'string',
         required: true,
       },
     }}
   />
   ```

### Adding Video Demos

1. **Place video file**: `public/videos/component-name.mp4`
2. **Optimal video specs**:
   - Format: MP4 (H.264)
   - Max width: 800px 
   - Frame rate: 30-60fps
   - Duration: 5-10 seconds
   - File size: <1MB

### Updating Content

- **Edit MDX files** directly in `content/docs/`
- **Hot reload** - Changes appear instantly in development
- **Navigation changes** require server restart

### Using Built-in Components

```mdx
<!-- Cards for navigation -->
<Cards>
  <Card href="/docs/components/animated-number" title="AnimatedNumber">
    Description here
  </Card>
</Cards>

<!-- Callouts for important notes -->
<Callout type="info">
Important information here
</Callout>

<!-- Accordions for FAQ sections -->
<Accordions type="single">
  <Accordion title="Question">
    Answer here
  </Accordion>
</Accordions>

<!-- Code blocks with package manager tabs -->
```bash npm2yarn
npm install package-name
```

<!-- Props documentation -->
<TypeTable
  type={{
    propName: {
      description: 'What this prop does',
      type: 'string | number',
      default: 'defaultValue',
      required: true,
    },
  }}
/>
```

## Deployment

### Build

```bash
npm run build
```

### Deploy

The site can be deployed to any static hosting provider:

- **Vercel** (recommended) - Automatic deployments from Git
- **Netlify** - Static site hosting with forms
- **GitHub Pages** - Free hosting for public repos
- **AWS S3** - Scalable cloud storage

### Environment Variables

No environment variables required for basic functionality.

## Development

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production  
- `npm run start` - Start production server

### Customization

- **Styling** - Tailwind CSS classes in components
- **Layout** - Modify `app/layout.config.tsx`
- **Branding** - Update logo and colors in layout config
- **Search** - Powered by Fumadocs' built-in search

## Acknowledgments

This documentation site is made possible by amazing open-source projects:

### Core Framework
- **[Fumadocs](https://fumadocs.dev/)** - Modern documentation framework by [SonnyZ](https://github.com/SonnyZ)
- **[Next.js](https://nextjs.org/)** - React framework by Vercel
- **[React](https://react.dev/)** - UI library by Meta

### Styling & Components  
- **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first CSS framework
- **[Radix UI](https://radix-ui.com/)** - Unstyled, accessible components
- **[Lucide React](https://lucide.dev/)** - Beautiful & consistent icons

### Content & Processing
- **[MDX](https://mdxjs.com/)** - Markdown with JSX components
- **[TypeScript](https://www.typescriptlang.org/)** - JavaScript with type safety
- **[Shiki](https://shiki.matsu.io/)** - Syntax highlighting

### Special Thanks

- **[ogulcanbagatir](https://github.com/ogulcanbagatir)** - Creator of the original RN Animated Components
- **[niche.guys](https://github.com/niche-guys)** - Component development team  
- **Fumadocs community** - For excellent documentation tools
- **All contributors** - Who help improve this documentation

## Contributing

Contributions are welcome! Please see our [Contributing Guide](/docs/contributing) for details.

## License

This documentation site is open source. The documented components maintain their original licenses.

---

Made with love using **Fumadocs**
