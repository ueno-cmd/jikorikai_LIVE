# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Vite-powered** music event website for "ジコリカイLIVE" (Jiko Rikai LIVE). The project has been modernized from static HTML to a proper build-based development environment with separated CSS and JavaScript files.

## Project Structure

```
music-event-site/
├── index.html                 # Main HTML file
├── package.json              # Dependencies and scripts
├── vite.config.js           # Vite configuration
├── src/
│   ├── js/
│   │   └── main.js          # Main JavaScript functionality
│   ├── styles/
│   │   └── main.css         # All CSS styles
│   └── assets/              # Images and other assets
├── public/                  # Static assets
└── reference/
    └── live_event_lp.html   # Original HTML reference
```

## Development Commands

### Essential Commands
```bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Install dependencies
npm install
```

### Development Workflow
1. Run `npm run dev` to start the development server
2. Edit files in `src/` directory
3. Changes are automatically reflected in the browser
4. Build with `npm run build` when ready for deployment

## Technical Architecture

### Build System
- **Vite** - Modern build tool with fast HMR (Hot Module Replacement)
- **Vanilla JavaScript** - No framework dependencies for simplicity
- **CSS Modules** - Separated and organized stylesheets
- **ES6 Modules** - Modern import/export syntax

### File Organization
- **Separated Concerns**: CSS and JS are in dedicated directories
- **Import System**: `src/js/main.js` imports `../styles/main.css`
- **Clean HTML**: No inline styles or scripts
- **Modular Structure**: Easy to maintain and extend

### CSS Architecture
- Uses CSS Grid and Flexbox for responsive layouts
- CSS custom properties for consistent theming
- Heavy use of CSS animations and transitions for visual effects
- Responsive design with mobile-first approach using media queries
- Component-based class naming (`.sns-card`, `.ticket-card`, etc.)

### JavaScript Features
- Real-time countdown timer functionality (target: 2026-06-13)
- Smooth scrolling navigation
- Intersection Observer for scroll-triggered animations
- Modular function organization
- ES6+ syntax with proper imports

## Key Sections

### Website Sections
1. **Hero Section** - Main landing with animated background
2. **Features Section** - Event highlights and benefits  
3. **Artist Lineup** - Featured performers including "UENO & KUBOTA"
4. **Countdown Section** - Live timer to event date
5. **Ticket Section** - Pricing and purchase information (Peatix integration)
6. **SNS Section** - Social media links (Twitter, Instagram, YouTube, TikTok)
7. **Recruitment Section** - Artist/staff/sponsor applications

### Design System
- **Primary Colors**: `#ff6b6b` (red) to `#4ecdc4` (teal) gradients
- **Background**: Dark theme with blue/purple gradients
- **Effects**: Backdrop-filter blur, floating animations, hover transitions
- **Typography**: Arial-based with gradient text effects
- **Icons**: Emoji-based with custom styling

## Content Management

### Current Event Details
- **Event Name**: ジコリカイLIVE (Jiko Rikai LIVE)
- **Date**: 2026年6月吉日 (June 2026, auspicious day)
- **Venue**: 東京ビッグサイト (Tokyo Big Sight)
- **Language**: Primarily Japanese with some English elements

### SNS Placeholders
All SNS links currently use placeholder URLs (`href="#"`):
- Twitter: `@jikorikai_live`
- Instagram: `@jikorikai_live`  
- YouTube: `ジコリカイLIVE公式`
- TikTok: `@jikorikai_live`

## Deployment Considerations

### Static Site Generation
- Vite builds to static files suitable for Netlify/Cloudflare
- No server-side rendering required
- Optimized bundles with automatic code splitting

### Build Output
```bash
npm run build
# Generates dist/ folder with optimized static files
```

### External Dependencies
- **Forms**: Google Forms integration planned
- **Payments**: Peatix platform integration
- **Hosting**: Netlify or Cloudflare Pages compatible

## Performance Features

- **Fast Development**: Vite's instant HMR
- **Optimized Builds**: Automatic minification and bundling
- **Modern JavaScript**: ES6+ with proper module system
- **CSS Optimization**: Separated stylesheets with efficient loading
- **Asset Management**: Automatic optimization of images and static files

## Initial Launch Changes (2024-07-20)

### Modifications for Initial Public Release
The following sections were modified for the initial launch as the related features were not yet ready:

1. **Artist Lineup Section** - Changed to "Coming Soon" placeholder
   - Removed specific artist names (ELECTRIC STORM, NEON DREAMS, TOKYO NIGHTS, BASS REVOLUTION, COSMIC HARMONY, UENO & KUBOTA)
   - Added preparation message for future artist announcements

2. **Countdown Timer Section** - Completely removed
   - Removed countdown timer functionality and display
   - JavaScript timer code may need cleanup in main.js

3. **Ticket Information Section** - Replaced with placeholder
   - Removed specific pricing (¥12,000, ¥20,000, ¥35,000)
   - Removed purchase buttons and Peatix integration
   - Added "ticket sales preparation" message

4. **SNS Section** - Replaced with preparation message
   - Removed placeholder social media links
   - Changed to "SNS accounts in preparation" message

5. **Recruitment Section** - Removed application forms
   - Kept recruitment messaging but removed interactive buttons
   - Added "application process in preparation" status
   - Removed form modal HTML code (no longer needed)

### Future Enhancements

- Real SNS account integration
- Google Forms embedding for recruitment
- SEO optimization (meta tags, structured data)
- Analytics integration
- Accessibility improvements
- Restore artist lineup when confirmed
- Restore countdown timer when launch date finalized
- Restore ticket purchasing when Peatix integration ready