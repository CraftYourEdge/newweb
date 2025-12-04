# Intent Visibility Platform - CraftAI

## Overview
CraftAI is a modern static website built with HTML5 and Tailwind CSS. The platform helps consumer brands transform their visibility in AI-driven search conversations across ChatGPT, Gemini, and Perplexity. The site features a professional landing page with intent-driven messaging, responsive design, and custom branding.

**Current State:** Fully functional static website running on Replit with automated Tailwind CSS build process and deployment configuration.

## Recent Changes
- **December 3, 2025**: Complete landing page redesign with dynamic animations
  - Hero Section: Dynamic fact rotation (40% guidance-seeking, 73% lack sources, 340% visibility boost)
  - Hero Section: "From Keywords to Intent" with strikethrough Keywords styling
  - Hero Section: Typewriter animation cycling through AI platforms (ChatGPT, Perplexity, Gemini, Claude, Copilot)
  - Hero Section: Website input field with "Check your Brand Visibility" CTA
  - Hero Section: Redesigned trust elements with gradient icons
  - Questions Section: "No More Google Search for Best Brands" heading with floating questions animation
  - Dashboard Section: Skeleton loading states, animated counters, platform performance bars
  - Four Pillars Section: Diagonal ascending layout with micro-interactions on hover
  - FAQ Section: Collapsible toggle functionality
  - Social Proof: Floating notification bar with customer success stories

- **December 1, 2025**: Initial project setup in Replit environment
  - Installed Node.js 20 and all npm dependencies
  - Built Tailwind CSS to generate compiled main.css
  - Configured static file server workflow on port 5000
  - Set up deployment configuration for static hosting
  - Copied favicon.ico to root directory for proper loading

## Project Architecture

### Technology Stack
- **Frontend**: Pure HTML5 with semantic markup
- **Styling**: Tailwind CSS v3.4.17 with custom configuration
- **Build Tool**: Tailwind CLI with @dhiwise/component-tagger
- **Dev Server**: http-server for local development
- **Fonts**: Google Fonts (Inter, JetBrains Mono)

### File Structure
```
.
├── index.html              # Entry point (redirects to landing page)
├── pages/
│   └── landing_page.html   # Main landing page
├── css/
│   ├── tailwind.css        # Source CSS with Tailwind directives
│   └── main.css            # Compiled CSS (auto-generated)
├── assets/
│   └── images/             # Image assets
├── public/
│   ├── favicon.ico         # Site favicon
│   ├── manifest.json       # PWA manifest
│   └── dhws-data-injector.js
├── package.json            # Node dependencies and scripts
└── tailwind.config.js      # Tailwind configuration
```

### Custom Tailwind Configuration
The project uses a comprehensive Tailwind setup with:
- **Custom Color Palette**: Navy, blue, gray, green, yellow, and red scales
- **Brand Colors**: Primary (navy), secondary (gray), accent (blue)
- **Custom Components**: `.btn-primary`, `.btn-secondary`, `.card`, `.metric-card`, `.form-input`
- **Extended Fonts**: Inter (sans-serif), JetBrains Mono (monospace)
- **Custom Shadows**: Multiple elevation levels for depth
- **Responsive Breakpoints**: sm (640px), md (768px), lg (1024px), xl (1280px), 2xl (1536px)

### Available NPM Scripts
- `npm run build:css` - Build production CSS
- `npm run watch:css` - Watch and rebuild CSS on changes
- `npm run dev` - Alias for watch:css (development mode)

## Replit Environment Setup

### Workflows
- **Static Web Server**: Runs `http-server` on port 5000 (0.0.0.0)
  - Serves all files from the project root
  - Configured for webview output
  - Auto-starts when Replit loads

### Deployment Configuration
- **Type**: Static site deployment
- **Build Command**: `npm run build:css`
- **Public Directory**: `.` (root)
- The site will be built and deployed as static HTML/CSS/JS files

## Development Workflow

### Local Development
1. The Tailwind CSS is pre-built - `css/main.css` is already generated
2. The static server automatically serves the site on port 5000
3. For CSS changes:
   - Edit `css/tailwind.css` or HTML files
   - Run `npm run build:css` to rebuild
   - Refresh the browser

### Making Changes
1. **Content Changes**: Edit HTML files in root or `pages/` directory
2. **Styling Changes**: 
   - Modify `css/tailwind.css` for custom styles
   - Update `tailwind.config.js` for theme changes
   - Run `npm run build:css` to compile
3. **Component Classes**: Use utility classes or custom components defined in `tailwind.css`

## Key Features
- **Responsive Design**: Mobile-first approach with Tailwind breakpoints
- **Modern UI**: Gradient backgrounds, animations, custom shadows
- **SEO Optimized**: Semantic HTML with proper meta tags
- **Fast Loading**: Static files with optimized CSS
- **Professional Branding**: Custom color scheme and typography

## External Dependencies
- Google Fonts API (Inter, JetBrains Mono)
- Rocket.new integration scripts (in HTML files)
- Tailwind CSS plugins: forms, animate, elevation, fluid-type

## Notes
- The site automatically redirects from `index.html` to `pages/landing_page.html`
- All styling is handled through Tailwind utility classes and custom components
- The favicon is available at both `/favicon.ico` (root) and `/public/favicon.ico`
- No backend or database required - purely static content
