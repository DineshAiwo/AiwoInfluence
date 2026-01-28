# Services Page - Animation Reference Guide

## 🎬 Complete Animation List

This document provides a comprehensive overview of all CSS animations and effects implemented in the services page.

---

## Hero Section Animations

### 1. **Floating Shapes** (`@keyframes float`)
```css
Duration: 20s
Timing: infinite ease-in-out
Effect: Circular shapes float, rotate, and fade
```
- **Shape 1**: 300px circle, starts at top-left
- **Shape 2**: 200px circle, starts at bottom-right
- **Shape 3**: 150px circle, starts at bottom-center
- Each shape has different animation delays (0s, 5s, 10s)

### 2. **Floating Image** (`@keyframes floatImage`)
```css
Duration: 6s
Timing: infinite ease-in-out
Effect: Hero image gently moves up and down
```
- Moves 20px up and down
- Creates breathing effect

### 3. **Gradient Overlay**
- Animated gradient background
- Colors: `#667eea → #764ba2 → #f093fb`
- Opacity variations for depth

### 4. **Parallax Scrolling**
- JavaScript-powered
- Shapes move at different speeds based on scroll
- Creates depth perception

---

## Service Card Animations

### 5. **Card Fade-In** (`@keyframes fadeInUp`)
```css
Duration: 0.6s
Timing: ease forwards
Effect: Cards fade in from bottom
```
- Staggered delays (0.1s, 0.2s, 0.3s, etc.)
- Initial opacity: 0, translateY: 30px
- Final opacity: 1, translateY: 0

### 6. **Card Hover Lift**
```css
Transform: translateY(-10px) scale(1.02)
Transition: 0.4s cubic-bezier
Effect: Card lifts and slightly enlarges
```

### 7. **Image Zoom & Rotate**
```css
Transform: scale(1.1) rotate(2deg)
Duration: 0.6s
Effect: Image zooms and tilts on hover
```

### 8. **Overlay Fade-In**
- Purple gradient overlay appears on hover
- Opacity: 0 → 1
- Duration: 0.4s

### 9. **Icon Slide-Up**
- Icons in overlay slide up on hover
- Transform: translateY(20px) → translateY(0)

### 10. **Feature List Slide-In** (`@keyframes slideIn`)
```css
Duration: 0.5s per item
Timing: staggered (0.1s, 0.2s, 0.3s)
Effect: List items slide from left
```
- Initial: opacity 0, translateX(-20px)
- Final: opacity 1, translateX(0)

### 11. **Glassmorphism Effect**
- Subtle white gradient overlay
- Appears on hover
- Creates frosted glass effect

---

## Button Animations

### 12. **Button Shimmer** (`::before` pseudo-element)
```css
Effect: Light sweeps across button
Trigger: Hover
```
- White gradient moves left to right
- Creates premium feel

### 13. **Button Hover**
```css
Transform: translateY(-2px)
Shadow: 0 10px 25px rgba(102, 126, 234, 0.4)
Background: Gradient reverses
```

### 14. **Pulse Animation** (`@keyframes pulse`)
```css
Duration: 1.5s
Timing: infinite
Trigger: Focus
Effect: Expanding shadow ring
```

---

## CTA Section Animations

### 15. **Gradient Shift** (`@keyframes gradientShift`)
```css
Duration: 10s
Timing: infinite ease
Effect: Background gradient pulses
```
- Opacity oscillates between 1 and 0.7
- Creates living background effect

### 16. **Button Lift**
- Same as other buttons
- Enhanced shadow on hover

---

## Gallery Animations

### 17. **Image Hover Zoom**
```css
Transform: scale(1.1)
Filter: grayscale(0%)
Duration: 0.5s
```
- Images start at 20% grayscale
- Become full color on hover

### 18. **Gallery Overlay**
- Purple gradient fades in
- Opacity: 0 → 1

### 19. **Heartbeat** (`@keyframes heartbeat`)
```css
Duration: 1s
Timing: infinite ease
Effect: Heart icon pulses
```
- Scale: 1 → 1.2 → 1

### 20. **Info Scale**
- Like count scales up on hover
- Transform: scale(0.8) → scale(1)

---

## Footer Animations

### 21. **Neon Glow** (`@keyframes neonGlow`)
```css
Duration: 2s
Timing: infinite alternate
Effect: Text shadow pulses
```
- Multiple layered shadows
- Purple and pink glow
- Intensity varies

---

## Scroll Animations (AOS)

### 22. **Fade Right**
- Used for: Hero content, left-side images
- Direction: From left to right
- Duration: 800ms

### 23. **Fade Left**
- Used for: Hero image, right-side content
- Direction: From right to left
- Duration: 800ms

### 24. **Fade Up**
- Used for: Service cards, gallery items
- Direction: From bottom to top
- Duration: 800ms

### 25. **Zoom In**
- Used for: CTA section
- Effect: Scales from 0.8 to 1
- Duration: 800ms

---

## Performance Optimizations

### Hardware Acceleration
All animations use GPU-accelerated properties:
- `transform` (instead of `top`, `left`)
- `opacity`
- `filter`

### Will-Change
Applied to frequently animated elements:
```css
will-change: transform, opacity;
```

### Reduced Motion
Respects user preferences:
```css
@media (prefers-reduced-motion: reduce) {
    * {
        animation-duration: 0.01ms !important;
        transition-duration: 0.01ms !important;
    }
}
```

---

## Timing Functions Used

| Function | Usage | Effect |
|----------|-------|--------|
| `ease-in-out` | Floating shapes | Smooth start and end |
| `ease` | Most transitions | Natural motion |
| `cubic-bezier(0.175, 0.885, 0.32, 1.275)` | Card hover | Bouncy effect |
| `linear` | Shimmer effect | Constant speed |

---

## Color Transitions

### Gradient Colors
- Primary: `#667eea` (Purple)
- Secondary: `#764ba2` (Deep Purple)
- Accent: `#f093fb` (Pink)

### Overlay Colors
- Service overlay: `rgba(102, 126, 234, 0.9)` to `rgba(118, 75, 162, 0.9)`
- Gallery overlay: Same gradient at 0.8 opacity

---

## Interactive States

### Hover States
- Cards: Lift + scale + shadow
- Images: Zoom + rotate
- Buttons: Lift + shimmer + shadow
- Gallery: Overlay + zoom

### Focus States
- Buttons: Pulse animation
- Links: Outline with brand color

### Active States
- Buttons: Slight scale down (0.98)
- Links: Color change

---

## Animation Delays

### Service Cards
```
Card 1: 0.1s
Card 2: 0.2s
Card 3: 0.3s
Card 4: 0.4s
Card 5: 0.5s
Card 6: 0.6s
```

### Feature Lists
```
Item 1: 0.1s
Item 2: 0.2s
Item 3: 0.3s
```

### Gallery Items
```
Item 1: 100ms
Item 2: 200ms
Item 3: 300ms
Item 4: 400ms
```

---

## Browser Compatibility

All animations are compatible with:
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

### Fallbacks
- Older browsers: Animations gracefully degrade
- No JavaScript: CSS animations still work
- Reduced motion: Respects user preferences

---

## Testing Checklist

- [ ] Test all hover effects
- [ ] Verify scroll animations trigger
- [ ] Check mobile responsiveness
- [ ] Test in different browsers
- [ ] Verify performance (60fps)
- [ ] Test with reduced motion enabled
- [ ] Check accessibility (keyboard navigation)

---

**Last Updated**: January 28, 2026
