# Maple AI Business Profile Slideshow

A responsive HTML slideshow presentation optimized for both desktop and mobile viewing.

## Quick Start

1. Place your SVG files in the `input` directory
2. Run the conversion script to generate HTML slides in the `output` directory
3. Open `index.html` in a browser or deploy to GitHub Pages

## Slideshow Settings & Styling Guide

### Container Sizes
```css
.slideshow-container {
    padding: 10px 0;
    height: 100vh;
    display: flex;
    flex-direction: column;
}

.slide-container {
    height: calc(100vh - 300px); /* Adjusts for controls below */
    margin-bottom: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}
```

### Navigation Controls
```css
.controls {
    padding: 20px;
    gap: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 90%;
    margin: 0 auto;
}

.btn {
    padding: 30px 60px;
    font-size: 36px;
    background: rgba(0, 0, 0, 0.8);
    color: white;
    border: 4px solid white;
    border-radius: 16px;
    cursor: pointer;
    min-width: 240px;
}
```

### Slide Counter
```css
.slide-number {
    padding: 12px 24px;
    font-size: 20px;
    background: rgba(0, 0, 0, 0.8);
    color: white;
    border-radius: 16px;
    border: 2px solid white;
}
```

### Checkbox Controls
```css
.checkbox-container {
    font-size: 36px;
    color: white;
    display: flex;
    align-items: center;
    gap: 20px;
}

.custom-checkbox {
    width: 30px;
    height: 30px;
    border: 2px solid white;
}
```

### Mobile Responsiveness
```css
@media (max-width: 768px) {
    .slide-container {
        height: calc(100vh - 300px);
    }

    .controls {
        padding: 20px;
        gap: 20px;
        flex-direction: column;
    }

    .btn {
        padding: 15px 30px;
        font-size: 24px;
        min-width: 100%;
    }

    .checkbox-container {
        font-size: 20px;
        text-align: center;
    }
}
```

### Small Screen Optimization
```css
@media (max-width: 360px) {
    .btn {
        padding: 12px 20px;
        font-size: 18px;
    }

    .checkbox-container {
        font-size: 16px;
    }

    .slide-number {
        padding: 8px 16px;
        font-size: 16px;
    }
}
```

## Features

- Responsive design that works on all screen sizes
- Large, touch-friendly navigation buttons
- Slide counter showing current position
- Optional glossary section toggle
- Fullscreen support
- Dark mode support
- Smooth transitions between slides
- Touch-optimized for mobile devices

## Customization Tips

1. **Adjusting Slide Size**: Modify the `height` property in `.slide-container` to change the vertical space for slides
2. **Button Sizing**: Update `padding` and `font-size` in `.btn` for larger/smaller buttons
3. **Mobile Breakpoints**: Add or modify `@media` queries to adjust layout for different screen sizes
4. **Colors**: Update `background` and `color` properties to match your brand colors
5. **Spacing**: Adjust `gap` and `padding` in `.controls` to change spacing between elements

## Best Practices

1. Keep SVG files optimized and clean for best performance
2. Test on multiple devices and screen sizes
3. Use relative units (vh, %) for better responsiveness
4. Maintain consistent aspect ratios in your slides
5. Consider touch targets of at least 44px for mobile users

## Troubleshooting

- If slides appear too small: Adjust the `height` in `.slide-container`
- If controls overlap: Increase the height subtraction in `calc(100vh - 300px)`
- If buttons are hard to tap on mobile: Increase padding and font size in mobile media queries
- If text is hard to read: Adjust font sizes and contrast ratios

## Development

To run locally:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000`

## GitHub Pages Deployment

1. Push to GitHub repository
2. Enable GitHub Pages in repository settings
3. Select the main branch as source
4. Access via `https://[username].github.io/[repository-name]` 