# Sleek Booking UI Prototype - status: Ready

**Project Location:** `/Users/gorkem/.gemini/antigravity/scratch/sleek-booking-ui`

This prototype is a standalone, mobile-first booking interface designed for integration with WordPress + Bricks Builder. It simulates an iPhone 12 layout (390x844) and features a modern, dark-themed aesthetic.

## 📂 Files
- **`index.html`**: The main structure. Contains the header, marquee, category filter, service cards, footer, and the modal popups.
- **`style.css`**: All styling logic. Handles the iPhone simulation, dark mode gradients, horizontal scrolling (snap), and responsive layout adaptation.

## ✨ Key Features
1.  **iPhone 12 Simulation**: Fixed 390x844px container centered on the screen.
2.  **Sleek Header**: Includes logo and a clickable map location with a status dot.
3.  **Promo Marquee**: Animated "First Visit Discount" banner.
4.  **Dominant Service Cards**:
    *   Dynamic height (fits screen without scroll).
    *   Image shrinking logic (guarantees CTA button visibility).
    *   Horizontal Scroll Snap (Deck effect).
5.  **Expanded Modal**:
    *   Clicking a card opens a detailed view.
    *   **Image Slider**: Horizontal scrolling gallery for social proof.
    *   **Lightbox**: Clicking a gallery image zooms it to full screen.
6.  **Compact Footer**: Minimalist bottom bar matching the header.

## 🚀 How to Resume/Edit
1.  **Open the Folder**: Navigate to `/Users/gorkem/.gemini/antigravity/scratch/sleek-booking-ui` in your file explorer.
2.  **Run**: Double-click `index.html` to open it in any web browser.
3.  **Edit**: Open the folder in VS Code (or any text editor) to make changes to `index.html` or `style.css`.

## 🛠 Integration Notes (for later)
To move this to Bricks Builder:
- Copy the HTML structure of the **Card** into a Bricks "Query Loop".
- Copy the CSS from `style.css` into Bricks' global CSS or page CSS.
- Use Bricks' "Popup" element to recreate the Modal logic, pasting the inner HTML content.
