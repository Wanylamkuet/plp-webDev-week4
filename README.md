# SpendWise Dashboard Shell

A clean, responsive personal finance dashboard layout built with semantic HTML5, CSS Grid, Flexbox, and CSS Custom Properties. This project serves as the visual foundation for the SpendWise capstone application.

## What Was Built & How Each Part Works

### 1. Overall Page Layout (`CSS Grid`)
- **`.dashboard-shell`** uses `display: grid` with `grid-template-columns: 250px 1fr` to place the navigation sidebar alongside the main content area without using absolute positioning.
- **`.cards-grid`** uses `repeat(auto-fit, minmax(260px, 1fr))` to automatically arrange the six expense category cards (Rent, Food, Transport, Utilities, Entertainment, and Savings) across available horizontal space.

### 2. Component Alignment (`Flexbox`)
- **Sidebar (`.sidebar` & `.nav-item`)**: Uses vertical and horizontal Flexbox layouts to align the brand logo, navigation links, and billing cycle footer.
- **Header (`.header` & `.header-summary`)**: Uses `justify-content: space-between` and `align-items: center` to separate the page greeting from the remaining budget pill and user avatar.
- **Category Cards (`.card`)**: Uses `flex-direction: column` and `justify-content: space-between` to keep card headers, financial figures, and progress bars neatly aligned.

### 3. Theme System & Dark Mode (`CSS Custom Properties`)
- All brand, accent, surface, border, and text colors are defined inside `:root` at the top of `style.css`.
- **Dark Theme Stretch Goal**: Implemented via `@media (prefers-color-scheme: dark)` by overriding only the `:root` variables.

### 4. Responsive Design (`< 768px`)
- A `@media (max-width: 767px)` query collapses both `.dashboard-shell` and `.cards-grid` into a single-column layout (`1fr`) and converts the sidebar navigation into a horizontal scrollable bar for mobile screens.

### 5. Accessible Micro-interactions
- Each card includes `tabindex="0"` and shares a combined `.card:hover, .card:focus` rule that smoothly elevates the card (`translateY(-4px)`) and deepens its `box-shadow` over `200ms`.
