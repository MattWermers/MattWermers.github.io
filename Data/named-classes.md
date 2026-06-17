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

#### `.flex-object`
A utility layout class that splits content into horizontal columns of equal width.
*   **Structure:**
    *   `.flex-object` (Flex container with dynamic `--direction` and `--gap` parameter overrides)

---

### **Components**

#### `.circular-object`
A utility styling used to frame images inside a circle. The container enforces a 1:1 aspect ratio and circular borders, while the inner image is set to fill the frame cleanly without distortion.
*   **Structure:**
    *   `.circular-object` (Circular wrapper box, 10rem diameter by default)
        *   `> img` (Styled with `object-fit: cover` and centered)

#### `.badge-card`
A specialized card component featuring a circular badge (e.g., profile picture) that overlaps the top border.
*   **Structure:**
    *   `.badge-card` (Relative-positioned card container)
        *   `.card-badge` (Base container for circular badge size)
        *   `.card-badge-absolute` (Modifier: Positions badge absolutely on the top border)
        *   `.card-badge-float` (Modifier: Floats badge on left side inside text box, allowing circular text wrap via `shape-outside`)
        *   `.card-content` (Flexbox column holding titles and text)
            *   `.card-title` (Pushed horizontally to clear the absolute badge, centered on top border)
            *   `.card-body` (Main text region)

#### `.content-card`
A standard content card component styled similarly to the `.badge-card`, but designed for cards that do not have an image badge. Its header title overlaps the top border on the left side, matching the default horizontal position where the badge would sit.
*   **Structure:**
    *   `.content-card` (Relative-positioned card container)
        *   `.card-content` (Padded top to clear the title)
            *   `.card-title` (Absolutely positioned on top border, aligned to the left at `left: 2rem`)
            *   `.card-body` (Main text region)

---

### **Interactables & Items**

#### `.button`
Defines a standard clickable button element.
*   **Behavior:** Uses CSS variables for customized colors on hover and normal state, allowing infinite theme variants.