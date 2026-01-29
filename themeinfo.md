# LahzaPay Theme Documentation

## Color Palette

### Primary Colors
```css
--primary-color: #2196F3;    /* Main brand blue */
--primary-dark: #1976D2;     /* Darker shade for hover states */
```

### Background Colors
```css
--background-dark: #1a2433;  /* Main dark background */
--background-light: #2d3748; /* Secondary background */
```

### Text Colors
```css
--text-color: #ffffff;                    /* Primary text color */
--text-secondary: rgba(255, 255, 255, 0.7); /* Secondary text color */
```

### Social Media Colors
```css
/* Facebook */
--facebook-base: rgba(66, 103, 178, 0.2);    /* Facebook button background */
--facebook-hover: rgba(66, 103, 178, 0.3);   /* Facebook button hover state */

/* WhatsApp */
--whatsapp-base: rgba(37, 211, 102, 0.2);    /* WhatsApp button background */
--whatsapp-hover: rgba(37, 211, 102, 0.3);   /* WhatsApp button hover state */
--whatsapp-group-base: rgba(37, 211, 102, 0.15); /* WhatsApp group button background */
--whatsapp-group-hover: rgba(37, 211, 102, 0.25); /* WhatsApp group button hover state */
```

## Spacing System
```css
--spacing-xs: 0.5rem;   /* Extra small spacing */
--spacing-sm: 1rem;     /* Small spacing */
--spacing-md: 1.5rem;   /* Medium spacing */
--spacing-lg: 2rem;     /* Large spacing */
```

## Border Radius
```css
--radius-sm: 8px;      /* Small border radius */
--radius-md: 12px;     /* Medium border radius */
--radius-lg: 16px;     /* Large border radius */
--radius-full: 9999px; /* Full border radius (circular) */
```

## Animation Properties
```css
--animation-timing: 0.3s;
--animation-curve: cubic-bezier(0.4, 0, 0.2, 1);
```

## Component-Specific Styling

### Header
- Background: Semi-transparent dark background with blur effect
- Height: Dynamic based on content
- Position: Fixed at top
- Z-index: 1000

### Navigation Buttons
- Default state: Transparent background
- Hover state: Slight white overlay (rgba(255, 255, 255, 0.1))
- Primary button: Uses --primary-color
- Primary button hover: Uses --primary-dark

### Feature Cards
- Background: Semi-transparent white (rgba(255, 255, 255, 0.05))
- Hover state: Slightly lighter background (rgba(255, 255, 255, 0.08))
- Icon background: Uses --primary-color
- Icon color: White

### Social Links
- Base padding: 0.75rem 1.5rem
- Minimum width: 160px
- Icon size: 20px
- Hover effect: Slight lift and background color change

### Bottom Navigation (Mobile)
- Background: Semi-transparent dark with blur
- Icon size: 24px
- Text size: 0.75rem
- Active state: Uses --primary-color

## Responsive Breakpoints
```css
/* Mobile devices */
@media (max-width: 480px) {
    /* Adjustments for very small screens */
}

/* Tablets and small desktops */
@media (max-width: 768px) {
    /* Adjustments for medium screens */
}
```

## Typography
- Font Family: 'Cairo', sans-serif
- Font Weights: 400 (regular), 600 (semi-bold), 700 (bold)
- Base font size: 16px
- Line height: 1.6

## Usage Guidelines for AI

1. **Color Application**
   - Always use CSS variables instead of hardcoded colors
   - Maintain contrast ratios for accessibility
   - Use opacity for hover states and overlays

2. **Spacing**
   - Use the spacing variables for consistent layout
   - Maintain vertical rhythm using the spacing system

3. **Components**
   - Follow the established component styling patterns
   - Maintain consistent hover and active states
   - Use appropriate border radius based on component size

4. **Responsive Design**
   - Test all components at both breakpoints
   - Ensure mobile-first approach
   - Maintain usability across all screen sizes

5. **Animations**
   - Use the standard animation timing and curve
   - Keep animations subtle and purposeful
   - Ensure animations don't interfere with usability

## Theme Implementation Example

```css
/* Example of proper theme implementation */
.my-component {
    background: var(--background-dark);
    color: var(--text-color);
    padding: var(--spacing-md);
    border-radius: var(--radius-md);
    transition: all var(--animation-timing) var(--animation-curve);
}

.my-component:hover {
    background: var(--background-light);
    transform: translateY(-2px);
}
```

## Accessibility Considerations

1. **Color Contrast**
   - Text on dark backgrounds should maintain WCAG AA compliance
   - Interactive elements should have clear hover states
   - Error states should be clearly visible

2. **Interactive Elements**
   - All interactive elements should have hover states
   - Focus states should be clearly visible
   - Touch targets should be appropriately sized

3. **Text Readability**
   - Maintain sufficient contrast ratios
   - Use appropriate font sizes
   - Ensure proper line height for readability

## Theme Extension Guidelines

When extending the theme:

1. **New Colors**
   - Add to the appropriate color category
   - Include both base and hover states
   - Document the purpose of the new color

2. **New Components**
   - Follow existing component patterns
   - Use established spacing and radius variables
   - Maintain consistent animation patterns

3. **New Breakpoints**
   - Document the purpose of new breakpoints
   - Ensure they don't conflict with existing ones
   - Test thoroughly across all screen sizes 