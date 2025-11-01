# Kasper Template - AI Development Guide

## Project Overview

This is a modern responsive HTML/CSS template called "Kasper" implementing a single-page website design with multiple sections. The project focuses on clean, maintainable CSS architecture and responsive design practices.

## Key Components & Architecture

### CSS Structure

- **Variables** (`style.css`): Global variables defined in `:root` for consistent theming

```css
:root {
    --main-color: #19c8fa;
    --transparent-color: rgb(15 116 143 / 70%);
    --section-padding: 100px;
}
```

- **Components**: Reusable UI patterns like `main-heading` with consistent styling patterns
- **Global Rules**: Base styles and reset rules
- **Container System**: Responsive container with breakpoints:
    - Small: 768px -> 750px width
    - Medium: 992px -> 970px width
    - Large: 1200px -> 1170px width 
### Layout Patterns

1. **Section Structure**: Most sections follow this pattern:

```html
<section class="[section-name]">
    <div class="container">
        <div class="main-heading">
        <h2>Section Title</h2>
        <p>Section description...</p>
        </div>
        <!-- Section-specific content -->
    </div>
</section>
```

2. **Grid Systems**:
    - Uses both Flexbox and CSS Grid
    - Services: `grid-template-columns: repeat(auto-fill, minmax(450px, 1fr))`
    - Portfolio: Flex-based responsive grid

### Media Queries

- Mobile-first approach with breakpoints at:
    - 767px (mobile)
    - 768px (tablet)
    - 992px (desktop)
    - 1199px (large desktop)

## Development Workflow

### Adding New Sections

1. Create section markup in `index.html` following the section structure pattern
2. Add corresponding styles in `style.css` using the section class
3. Implement responsive design using existing breakpoint patterns
4. Include navigation link in header if needed

### CSS Conventions

- BEM-like naming: `block__element--modifier`
- Section-specific styles grouped together
- Media queries included with their component styles
- Use CSS variables for colors and spacing

### Common Patterns

- Overlay effects use pseudo-elements:

```css
.section::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgb(0 0 0 / 60%);
}
```

- Image handling:
```css
img {
    max-width: 100%;
}
```

## Integration Points

1. **Font Awesome Icons**: Used throughout for icons
2. **Google Fonts**: Open Sans font family
3. **Normalize.css**: For consistent cross-browser styling

## Testing & Validation

1. Test responsiveness at key breakpoints: 767px, 768px, 992px, 1199px
2. Verify hover/active states on interactive elements
3. Check image loading and aspect ratios
4. Validate form functionality in contact sections

## Common Issues & Solutions

- For overlapping text issues, check z-index and positioning context
- Image aspect ratio problems: use appropriate background-size properties
- Mobile menu toggle: verify event handling and display properties
- Form validation: ensure proper input types and aria attributes
