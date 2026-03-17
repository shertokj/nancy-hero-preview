# Nancy Shertok Website - Design System

Ground truth for all styling decisions. Refer to this before making changes.

## Colors

| Token            | Value     | Usage                        |
|------------------|-----------|------------------------------|
| `--bg`           | #FDFBF7   | Page background              |
| `--text`         | #1A1A1A   | Primary text                 |
| `--muted`        | #6B6B6B   | Secondary text               |
| `--border`       | #E8E4DD   | Borders, dividers            |
| `--accent`       | #1A1A1A   | CTAs (dark)                  |
| `--accent-hover` | #2D2D2D   | CTA hover state              |

## Typography

- **Headings:** 'Playfair Display', serif
- **Body:** 'Inter', sans-serif
- **H1 (page/header):** 2.8rem, weight 600, color #1A1A1A, line-height 1.3, letter-spacing -0.5px
- **H1 (hero):** Same as above, margin-bottom 32px
- **H1 (responsive < 768px):** 2.2rem
- **H1 (responsive < 480px):** 1.8rem
- **H2 (section):** 2.2rem, weight 600, centered, margin-bottom 48px
- **H3 (card):** 1.25rem, weight 600, color #1A1A1A
- **Body text:** 1rem, color #555-#6B6B6B, line-height 1.6-1.8

## Nancy Photo

| Context      | Class        | Desktop max-width | Mobile max-width | Aspect Ratio |
|--------------|--------------|--------------------|------------------|--------------|
| Homepage     | `.hero-photo` | 320px              | 400px (< 900px)  | 4/5          |
| About page   | `.about-photo`| 320px              | 400px (< 900px)  | 4/5          |

Both classes share: `width: 100%; object-fit: cover; background: var(--border); border-radius: 4px; display: block; margin: 0 auto;`

## Page Headers

Standard subpages use `.page-header` wrapper:
- Padding: `140px 0 64px`
- Text-align: center
- H1 + subtitle paragraph pattern

About page uses `.about-hero` (2-column grid) but h1 styling matches the shared `.page-header h1` values.

## Layout

- **Max content width:** 1100px, centered
- **Page padding:** 0 24px (mobile: 0 16px)
- **Section padding:** 60-100px vertical
- **Grid gap:** 48-60px

## Buttons

- **Primary (`.btn-primary`, `.cta`):** bg #1A1A1A, text #FFF, padding 14px 40px, border-radius 4px
- **Secondary (`.btn-secondary`):** Same but padding 12px 28px
- **Full-width (`.btn-full`):** 100% width, padding 16px 32px

## Cards

- Background: #FFFFFF
- Padding: 28-36px
- Border: 1px solid #E8E4DD
- Border-radius: 8px
- Hover: border #1A1A1A, shadow, translateY(-2px)

## Responsive Breakpoints

- **968px:** Nav collapses, mobile menu
- **900px:** Hero/about grid stacks
- **768px:** Typography scales down, form rows stack
- **480px:** Further type reduction

## File Structure

- `css/shared.css` - All shared styles (typography, buttons, cards, forms, nav, footer, responsive)
- `css/magazine.css` - Base/reset styles, nav, footer, layout grid
- Page-specific styles in `<style>` blocks within each HTML file
