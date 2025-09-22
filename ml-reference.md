# EchoML by Getti - Reference

**EchoML** is the **Echo Markup Language**, a declarative DSL for building GUI hierarchies in Roblox Studio.

---

## 🛠 Core Functions

- `Element(GuiObject)`  
  Creates a new GUI element of type `GuiObject`.  
  Returns a function that can accept **properties** and **children**, applying them to the element.  

  Example: <code>local btn = Element("TextButton")({ Text = "Click me" })()</code>

- `AddChildren(element, ...)`  
  Adds one or more child elements to a parent element.  

  Example: <code>AddChildren(frame, label, button)</code>

---

## 🔹 Prebuilt Elements

These are ready-to-use functions or objects with **default styling**:

- `Frame` → vertical container with default background color `Color3.fromRGB(240,240,240)` and no border.
- `ScrollingFrame` → vertical scrollable container, default background, scrollbar thickness 10.
- `ViewportFrame` → viewport container, default background `Color3.fromRGB(200,200,200)`.

- `TextLabel` → transparent background, black text, font `SourceSans`, text size 18.
- `TextButton` → gray background, black bold text, font `SourceSansBold`, text size 18, auto button color enabled.
- `ImageLabel` → transparent background for displaying images.
- `ImageButton` → transparent background for clickable images.

- Layout and visual helpers:
  - `UIListLayout`
  - `UIPadding`
  - `UIGridLayout`
  - `UIStroke`
  - `UIAspectRatioConstraint`
  - `UIGradient`
  - `UICorner`
  - `UIScale`

---

## 🔹 Usage Example (Conceptual)

<code>
local gui = Frame({ Name = "MainFrame" },
    TextLabel({ Text = "Welcome!" }),
    TextButton({ Text = "Click me!" })
)
</code>
