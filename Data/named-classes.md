# List of Named Classes

A reference guide for the reusable layouts, components, and classes defined in this project.

---

### **Layouts**

#### `.bodywith-sidebar`
Defines a main page layout with a left-hand navigation/sidebar (taking up 20% width up to a maximum of 200px) and a main content area filling the remaining space.
*   **Structure:**
    *   `.bodywith-sidebar` (Flex container)
        *   `.bar` (Sidebar container)
        *   `.body` (Main body content area)
            *   `#interior` (Wrapper to add 1rem padding)

#### `.split`
A utility flex container that splits content into horizontal columns of equal width.
*   **Structure:**
    *   `.split` (Flex container with a 10px gap)
        *   `> div` (Direct children elements representing columns; sized using `flex: 1` and `min-width: 0`)

---

### **Components**

#### `.circular-object`
A utility styling used to frame images inside a circle. The container enforces a 1:1 aspect ratio and circular borders, while the inner image is set to fill the frame cleanly without distortion.
*   **Structure:**
    *   `.circular-object` (Circular wrapper box, 10rem diameter by default)
        *   `> img` (Styled with `object-fit: cover` and centered)

#### `.badge-card`
A specialized card component featuring a circular badge (e.g., profile picture) that overlaps the top border. The layout shifts the title to prevent collision with the badge.
*   **Structure:**
    *   `.badge-card` (Relative-positioned card container)
        *   `.card-badge` (Absolute-positioned circular badge, overlapping the top-left edge)
        *   `.card-content` (Flexbox column holding titles and text)
            *   `.card-title` (Pushed 12rem from the left to clear the absolute badge)
            *   `.card-body` (Main text region flowing below the badge footprint)

---

### **Interactables & Items**

#### `.button`
Defines a standard clickable button element.
*   **Behavior:** Uses the Accent Cream color (`#ffe6b8`) and shifts to Accent Cream Hover (`#ffdca0`) on interaction.