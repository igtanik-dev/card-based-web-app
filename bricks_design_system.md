# Bricks Builder Design System 🎨

This document outlines the **Theme Styles**, **Classes**, and **Settings** you need to configure in Bricks Builder to replicate the "Sleek Booking UI" exactly.

---

## 1. Theme Styles (Global Settings)

Go to **Bricks > Settings > Theme Styles**.

### **Typography**
*   **Font Family:** `Outfit` (Add via Google Fonts integration).
*   **Body Text:**
    *   Size: `1rem` (16px)
    *   Color: `#ffffff` (Primary) / `#a0a0a0` (Secondary)
    *   Line Height: `1.5`
*   **Headings (H1, H2, etc.):**
    *   **H1 (Hero):** Size `2rem`, Weight `500`, Line Height `1.1`.
    *   **H2 (Card Titles):** Size `1.5rem`, Weight `500`.
    *   **Section Labels:** Size `0.75rem`, Uppercase, Letter Spacing `1.5px`.

### **Colors (Global Palette)**
Define these in your Bricks Palette for easy reuse:
*   `Dark BG (Main)`: `#0d0d0d` (Body Background)
*   `Card BG`: `#1a1a1a` (Cards, Panels)
*   `Text Primary`: `#ffffff`
*   `Text Secondary`: `#a0a0a0` (Descriptions, Subtitles)
*   `Text Muted`: `#666666` (Footer links, icons)
*   **`Brand Green` (Accent):** `#4cd964` (Marquee, Indicators)
*   **`Border Light`:** `rgba(255, 255, 255, 0.05)` (Subtle Dividers)
*   **`Border Strong`:** `rgba(255, 255, 255, 0.15)` (Header Border)
*   **`Border White`:** `rgba(255, 255, 255, 0.3)` (Input Borders, Placeholders)

---

## 2. Layout & Spacing

*   **Page Width:** For mobile simulation, we used `390px`. On a real site, your "Container" max-width might be `100%` but for this specific mobile-view design, stick to narrow containers or use a wrapper class.
*   **Global Padding:** `24px` (Standard side padding for all sections).
*   **Section Spacing:** `40px` (Space between major blocks).

---

## 3. Component Classes (CSS for Bricks)

Create these generic CSS classes in Bricks to apply to elements.

### **Buttons**
*   **Class:** `.btn-hero`
    *   Padding: `18px`
    *   Radius: `12px`
    *   Background: `#ffffff`
    *   Text Color: `#000000`
    *   Font Weight: `600`
    *   Shadow: `0 10px 20px rgba(255,255,255,0.1)`
*   **Class:** `.btn-outline` (Book Buttons)
    *   Background: `Transparent`
    *   Border: `1px solid rgba(255,255,255,0.2)`
    *   Radius: `12px`
    *   Hover: `Border #fff`, `Background rgba(255,255,255,0.05)`

### **Cards & Containers**
*   **Service Card (`.service-card`)**
    *   Background: `#1a1a1a` (Gradient or Solid)
    *   Border Radius: `24px`
    *   Border: `1px solid rgba(255,255,255,0.05)`
    *   Shadow: `0 20px 40px rgba(0,0,0,0.4)`
*   **Review Card (`.review-card`)**
    *   Background: `rgba(255,255,255,0.03)`
    *   Border Radius: `16px`
    *   Border: `1px solid rgba(255,255,255,0.05)`

### **Inputs & Placeholders**
*   **Image Placeholder (`.hero-img-placeholder`)**
    *   Background: `Radial Gradient (Center, #262626, #000)`
    *   Border: `1px solid rgba(255,255,255,0.3)`
    *   Radius: `4px`
    *   Aspect Ratio: `1/1`

---

## 4. Specific Visual Effects (CSS)

Add these in **Bricks > Page Settings > Custom CSS** or on the specific elements.

**1. Hero Title Gradient**
```css
.hero-title {
    background: linear-gradient(to right, #fff, #bbb);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
}
```

**2. Header Blur/Translucency**
```css
.header-mini {
    background: rgba(13,13,13,0.98); 
    backdrop-filter: blur(10px); /* Optional for glass effect */
}
```

**3. Marquee Animation (If not using Bricks native marquee)**
```css
@keyframes marquee { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
.marquee-track { animation: marquee 20s linear infinite; }
```

---

## 5. Iconography
*   **Library:** FontAwesome 6 (Solid & Brands).
*   **Sizes:** Standard icons `1.2rem` usually.
*   **Colors:** `#666` (Inactive), `#ffffff` (Active/Hover).
