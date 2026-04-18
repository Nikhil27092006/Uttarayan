# UTTARAYAN - Interactive 3D Restaurant Website Specification

## 1. Project Overview

**Project Name:** UTTARAYAN - Premium Indian Vegetarian Restaurant
**Project Type:** Interactive 3D Web Experience
**Core Functionality:** Immersive scroll-driven 3D experience showcasing authentic Indian vegetarian cuisine with a transforming Tandoor oven as the centerpiece
**Target Users:** Food enthusiasts, restaurant visitors, Indian cuisine lovers

---

## 2. Visual & Rendering Specification

### Scene Setup
- **Camera:** Perspective camera with smooth scroll-linked movement
- **Lighting:**
  - Warm ambient light (intensity: 0.4, color: #FFD700)
  - Primary directional light from top-right (intensity: 1.2, color: #FFA500)
  - Accent point lights for dish highlights (warm white)
  - Volumetric-style glow effects for festival feel
- **Environment:**
  - Dark royal background (#1a0a0a) with subtle gradient
  - Floating decorative elements (marigold flowers, spice particles)
  - Subtle fog for depth (density: 0.02)

### Color Palette - Royal Red/Gold Theme
- **Primary:** Deep Maroon (#8B0000), Royal Crimson (#DC143C)
- **Secondary:** Rich Gold (#FFD700), Amber (#FFBF00)
- **Accent:** Saffron Orange (#FF8C00), Cream (#FFF8DC)
- **Background:** Dark Burgundy (#1a0808), Deep Brown (#2d1515)
- **Text:** Gold (#FFD700), Cream (#FFFDD0)

### Materials & Effects
- **Tandoor Oven:**
  - Terracotta/clay material with procedural texture
  - Emissive glow inside (warm orange/red)
  - Metallic gold accents for decorative elements
  - Heat distortion shader effect
- **Food Dishes:**
  - PBR materials with subsurface scattering for breads
  - Glossy ceramic plates
  - Glowing spice particles
- **Decorative Elements:**
  - Marigold petals with translucency
  - Floating gold dust particles
  - Soft bloom on emissive elements

### Post-Processing Effects
- **Bloom:** High intensity on fire/glow elements (threshold: 0.6, strength: 1.5)
- **Vignette:** Subtle dark edges for focus
- **Color Grading:** Warm tones, slight saturation boost
- **Grain:** Very subtle film grain for richness

---

## 3. 3D Assets Specification

### Primary 3D Model: Tandoor Oven (Scroll-Transforming)
The central Tandoor oven transforms through 4 distinct states as user scrolls:

1. **State 1 - Hero (Scroll 0-25%):** Full Tandoor oven with flames, traditional clay design
   - Animated fire particles inside
   - Rotating slowly on Y-axis
   - Golden decorative rings visible

2. **State 2 - Transformation (Scroll 25-50%):** Oven morphs into cooking scene
   - Opens up to reveal naan bread baking
   - Flames intensify
   - Smoke particles emerge
   - Morphs into dome shape

3. **State 3 - Showcase (Scroll 50-75%):** Transforms to serving platter
   - Oven folds into plate shape
   - Various dishes appear (dals, paneer, rice)
   - Steam rises from food
   - Gold accents float around

4. **State 4 - Finale (Scroll 75-100%):** Full menu celebration
   - Transforms into decorative diya/lamp
   - Multiple dish icons orbit around
   - Festival/celebration aesthetic
   - "Welcome to UTTARAYAN" text appears

### Secondary 3D Elements
- **Floating Spice Bowls:** Small 3D bowls with animated spices
- **Naan Bread:** 3D breads that flip/bounce on scroll
- **Decorative Diyas:** Small floating lamps
- **Leaf Platters:** Banana leaf with food items

---

## 4. Animation Specification

### ScrollTrigger Animations (GSAP)

#### Section 1: Hero (0-25vh)
- Logo "UTTARAYAN" fades in with letter-by-letter animation
- Tagline "Pure Vegetarian Royal Experience" slides up
- 3D Tandoor oven rises from below
- Particle burst effect on arrival
- Scroll indicator pulses

#### Section 2: Our Story (25-50vh)
- Historical text reveals with parallax
- Traditional pattern border animates in
- Tandoor transforms (State 1 → State 2)
- Spice illustrations float across

#### Section 3: Menu Showcase (50-75vh)
- Dish cards fly in from sides
- Tandoor transforms (State 2 → State 3)
- Food items rotate into view
- Price tags animate with bounce

#### Section 4: Reservations (75-100vh)
- Contact form slides in
- Tandoor transforms (State 3 → State 4)
- Final celebration animation
- Call-to-action buttons pulse

### Motion Fonts & Text
- **Primary Font:** Playfair Display (elegant serif for headings)
- **Secondary Font:** Cormorant Garamond (body text)
- **Accent Font:** Dancing Script (decorative elements)
- **Text Animations:**
  - Staggered letter reveals
  - Gradient text fills on scroll
  - Text that follows cursor
  - Floating/suspended text effects

---

## 5. Interaction Specification

### User Controls
- **Mouse/Touch:**
  - Scroll to navigate and transform 3D model
  - Hover on dishes for info tooltips
  - Click to expand dish details
  - Mouse parallax on background elements
- **Scroll:**
  - Smooth scroll with GSAP ScrollSmoother
  - Progress indicator on side
  - Section snap points (optional)

### Interactive Elements
- **Dish Cards:** Hover to see ingredients, origin
- **Menu Items:** Click to view full details
- **Reservation Button:** Opens modal
- **Social Links:** Hover animations

---

## 6. Menu Sections & Dishes

### North Indian Specialties
- Dal Makhani (creamy black lentil)
- Paneer Tikka Masala
- Garlic Naan (fresh from tandoor)
- Shahi Paneer
-veg Kolhapuri

### South Indian Delights
- Masala Dosa
- Idli Sambar
- Vada Sambar
- Pongal
- Filter Coffee

### Street Food Favorites
- Chole Bhature
- Poha with Jalebi
- Lassi (mango/rose)
- Pani Puri
- Samosa

---

## 7. Technical Implementation

### Libraries Used
- **Three.js:** 3D rendering, Tandoor oven model
- **GSAP:** Animations, ScrollTrigger
- **GSAP ScrollSmoother:** Smooth scrolling
- **Custom Shaders:** Fire, glow, morph effects

### Performance Targets
- 60 FPS on modern devices
- < 3s initial load
- Lazy loading for heavy assets
- Progressive enhancement

---

## 8. Acceptance Criteria

1. ✓ 3D Tandoor oven renders and responds to scroll
2. ✓ 4 distinct transformation states as user scrolls
3. ✓ All GSAP ScrollTrigger animations fire correctly
4. ✓ Motion fonts animate on scroll
5. ✓ All menu sections display correctly
6. ✓ Royal Red/Gold theme consistent throughout
7. ✓ Works on desktop browsers (Chrome, Firefox, Safari)
8. ✓ Smooth 60fps performance
9. ✓ Responsive layout adapts to screen sizes
10. ✓ All interactive elements respond to hover/click