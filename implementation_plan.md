# Implementation Plan - Sleek Booking UI (Bricks/WP Ready)

## Goal
Create a standalone HTML/CSS prototype that implements the user's wireframe with a "modern sleek" aesthetic, specifically structured to be easily ported to **WordPress + Bricks Builder**.

## Design Philosophy
- **Aesthetic**: Minimalist Dark Mode. High contrast, subtle borders, "premium" typography.
- **Interactions**: Native CSS Scroll Snap for the "Swipable Deck". This ensures it works perfectly on mobile without heavy JS libraries, making it easy to build in Bricks.
- **Dynamic Data**: The "Cards" will be built as a single repeatable component (Loop Item) for CPT compatibility.

## Proposed Structure

### 1. Header (HeaderMini)
- Simple Flex container.
- Semantic: `<header>`
- Bricks: Section > Container > Block (Flex Row).

### 2. Category Filter (Taxonomy Loop)
- Horizontal scroll container with hidden scrollbars.
- Semantic: `<nav>` or `<div>` list.
- Bricks: Block (Overflow: auto) > Button/Link (Repeater based on Taxonomy terms).

### 3. Featured Deck (CPT Query Loop)
- **Critical Mechanism**: `scroll-snap-type: x mandatory` on the parent, `scroll-snap-align: center` on the card.
- Allows the "Peek" effect naturally (by setting card width < 100%).
- Bricks: Block (Overflow: auto, Snap settings) > Block (Card Item - Query Loop).

## Files
- `index.html`: The markup structure.
- `style.css`: The "sleek" styling variables and layout logic.

## Verification
- I will verify the "peek" logic via CSS math (e.g., Card Width = 85vw or similar).
