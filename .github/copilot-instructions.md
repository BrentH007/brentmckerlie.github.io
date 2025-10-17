# Copilot Instructions for Portfolio Site

## Project Architecture
This is a single-file HTML portfolio website designed for GitHub Pages deployment. The architecture prioritizes:
- **Zero-dependency approach**: Pure HTML/CSS with minimal vanilla JS
- **Accessibility-first**: ARIA labels, semantic HTML, and high contrast focus styles
- **Dark/light mode**: Automatic theme switching via `prefers-color-scheme`

## Key Files & Structure
```
/Brent-McKerlie-Portfolio/
  brent_mc_kerlie_git_hub_portfolio_index.html  # Main portfolio file (rename to index.html for deployment)
```

## Content Update Patterns

### Adding New Projects
1. Duplicate the `PROJECT CARD TEMPLATE` comment block (lines 167-189)
2. Update the `.project` article with:
   - `.tag` span for category/year
   - `h3` for project name
   - Description paragraph
   - `.badge` spans for tech stack
   - `.links` for repo/demo URLs
3. Use `.project.large` class for featured projects (spans full grid width)

### Theme Customization
Update CSS custom properties in `:root` (lines 30-39):
- `--accent`: Primary brand color (#6b4eff)
- `--accent-2`: Secondary accent (#00d6a3)
- `--bg`, `--surface`, `--text`, `--muted`: Color scheme values

### Hero Section Updates
The hero section (lines 130-158) contains:
- Main heading and tagline
- CTA buttons (GitHub, projects, resume)
- Profile card with avatar, location, and contact links

## CSS Architecture Patterns
- **Component-based classes**: `.btn`, `.project`, `.badge`, `.chip`
- **Layout utilities**: `.grid` (12-column), `.wrap` (max-width container)
- **Responsive design**: Grid columns collapse on mobile via `@media (max-width:900px)`
- **CSS Grid**: Projects use `grid-column: span 6` (half-width) or `span 12` (full-width)

## Deployment Workflow
1. Rename file to `index.html`
2. Commit to GitHub repository
3. Enable GitHub Pages in repo settings (Settings → Pages → Deploy from branch)
4. Update placeholder links (`https://github.com/your-username` → actual URLs)

## Accessibility Conventions
- All interactive elements have proper focus states (`:focus-visible`)
- Screen reader support via `.sr-only` class and ARIA labels
- High contrast focus rings (`--ring` variable)
- Semantic HTML structure with proper heading hierarchy

## Content Guidelines
- Project descriptions: One sentence explaining what it does and why it matters
- Tech stack badges: Keep to 3-4 key technologies per project
- External links: Always include `target="_blank" rel="noopener"` for security
- SVG placeholders: Replace with actual project screenshots (recommended 16:9 aspect ratio)