---
name: Modern Technical Narrative
colors:
  surface: '#f7f9fb'
  surface-dim: '#d8dadc'
  surface-bright: '#f7f9fb'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f4f6'
  surface-container: '#eceef0'
  surface-container-high: '#e6e8ea'
  surface-container-highest: '#e0e3e5'
  on-surface: '#191c1e'
  on-surface-variant: '#44474f'
  inverse-surface: '#2d3133'
  inverse-on-surface: '#eff1f3'
  outline: '#75777f'
  outline-variant: '#c5c6d0'
  surface-tint: '#495e8a'
  primary: '#00020a'
  on-primary: '#ffffff'
  primary-container: '#001b44'
  on-primary-container: '#7084b3'
  inverse-primary: '#b1c6f9'
  secondary: '#0453cd'
  on-secondary: '#ffffff'
  secondary-container: '#356ee7'
  on-secondary-container: '#fefcff'
  tertiary: '#000205'
  on-tertiary: '#ffffff'
  tertiary-container: '#001f30'
  on-tertiary-container: '#008dc9'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#d8e2ff'
  primary-fixed-dim: '#b1c6f9'
  on-primary-fixed: '#001a42'
  on-primary-fixed-variant: '#314671'
  secondary-fixed: '#dae2ff'
  secondary-fixed-dim: '#b2c5ff'
  on-secondary-fixed: '#001848'
  on-secondary-fixed-variant: '#0040a2'
  tertiary-fixed: '#c9e6ff'
  tertiary-fixed-dim: '#89ceff'
  on-tertiary-fixed: '#001e2f'
  on-tertiary-fixed-variant: '#004c6e'
  background: '#f7f9fb'
  on-background: '#191c1e'
  surface-variant: '#e0e3e5'
typography:
  display-lg:
    fontFamily: Montserrat
    fontSize: 56px
    fontWeight: '600'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Montserrat
    fontSize: 36px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Montserrat
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Montserrat
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Montserrat
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Montserrat
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.5'
  body-md-italic:
    fontFamily: Montserrat
    fontSize: 16px
    fontWeight: '500'
    lineHeight: '1.5'
  label-md:
    fontFamily: Space Grotesk
    fontSize: 14px
    fontWeight: '500'
    lineHeight: '1'
    letterSpacing: 0.05em
  caption:
    fontFamily: Montserrat
    fontSize: 12px
    fontWeight: '400'
    lineHeight: '1.4'
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 12px
  md: 24px
  lg: 48px
  xl: 80px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 64px
---

## Brand & Style
The design system balances technical precision with a confident, modern aesthetic. It targets a professional audience that values clarity, structural integrity, and innovation. The visual style is **Corporate Modern** with a slight **Technical** edge, characterized by clean lines, ample whitespace, and high-quality geometric typography. It evokes a sense of reliability and forward-thinking momentum.

## Colors
The palette is rooted in a structured hierarchy of blues. **Navy** serves as the primary anchor for text and deep backgrounds, providing a sense of authority. **Royal** acts as the primary action color, while **Sky** provides energetic accents and secondary UI states. **Mist** is the foundational neutral for surfaces. **Spark** is used sparingly as a high-contrast functional accent for critical highlights or notifications.

## Typography
This design system utilizes **Montserrat** as its primary typographic workhorse to convey confidence and modernity. 
- **Headings and Emphasis:** Use Montserrat Semibold (600) to establish a strong visual hierarchy.
- **Body Text:** Use Montserrat Regular (400) for optimal readability and a clean, professional feel.
- **Italics:** Use Montserrat Medium Italic (500) to ensure emphasized text maintains sufficient visual weight and character.
- **Technical Accents:** **Space Grotesk** is retained for labels, data points, and small caps to inject a geometric, technical flavor into the interface.

## Layout & Spacing
The layout follows a **Fluid Grid** philosophy based on an 8px square rhythm.
- **Desktop:** 12-column grid with 24px gutters and 64px side margins.
- **Tablet:** 8-column grid with 24px gutters and 32px side margins.
- **Mobile:** 4-column grid with 16px gutters and 16px side margins.
Spacing between sections should leverage the `lg` (48px) and `xl` (80px) tokens to maintain a sense of "breathable" minimalism.

## Elevation & Depth
Depth is communicated through **Tonal Layers** and **Ambient Shadows**. Surfaces at higher elevations use subtle, highly diffused shadows with a slight Navy (#001B44) tint to maintain color harmony.
- **Level 0 (Base):** Mist (#F8FAFC) background.
- **Level 1 (Cards):** White surface with a 1px Navy outline at 5% opacity.
- **Level 2 (Popovers):** White surface with a 12% opacity Navy shadow, 16px blur, 4px Y-offset.
- **Level 3 (Modals):** White surface with a 20% opacity Navy shadow, 32px blur, 8px Y-offset.

## Shapes
The shape language is **Soft** and professional. This design system uses a consistent 4px (0.25rem) base radius for standard components like buttons and inputs. Larger containers and cards utilize the `rounded-lg` (8px) token. This subtle rounding softens the technical geometry without appearing too casual or "bubbly."

## Components
- **Buttons:** Primary buttons use Royal background with White Montserrat Semibold text. Secondary buttons use a Navy outline with 1.5px stroke width.
- **Inputs:** Use Mist background with a 1px border. On focus, the border transitions to Royal with a 2px outer "halo" in Sky at 20% opacity.
- **Cards:** Use Level 1 elevation with 8px corner radius. Padding is strictly set to 24px (md) for internal content.
- **Chips:** Utilize Space Grotesk labels for a technical look. Backgrounds are low-opacity tints of the primary colors (e.g., Sky at 10% opacity).
- **Lists:** Clean dividers using 1px Mist-dark (approx 10% darker than base Mist) with 16px vertical spacing between items.
- **Data Display:** Tables and charts should prioritize Space Grotesk for numerical values to emphasize the technical nature of the data.