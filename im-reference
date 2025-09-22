# EchoIM by Getti - Reference

**EchoIM** is the **Echo Interface Manager**, a Roblox GUI engine for managing **styles** and **events** using selectors similar to CSS.

---

## 🛠 Instance API

- `on(selector, listenerTable, callbackFunc)`  
  Bind event listeners to GUI elements matching a selector.

- `style(selector, propertyTable)`  
  Apply a set of properties (styles) to elements matching a selector.

- `init()`  
  Initialize EchoIM.

- `new(parent)`  
  Create a new GUI manager instance with a parent ScreenGui.  
  Returns: `self`

---

## 🔹 Values / Parameters

- `selector` → `{ kind = "name" | "class" | "attr" | "uid" | "cb", payload = value }`  
- `listenerTable` → e.g. `{ "MouseEnter", "MouseLeave", ... }`  
- `callbackFunc` → function executed when the event triggers, returns true/false  
- `propertyTable` → `{ BackgroundColor3 = Color3.fromRGB(255, 255, 255), ... }`  
- `parent` → `Instance.new("ScreenGui")`  
- `self` → `Instance.new("ScreenGui")`

---

## ✨ Extra / Advanced Usage

Example of precise input detection:

<code>
on(attrSelector("card", true), listeners("InputBegan"), function(element, input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 then
        print(string.format("button %s pressed", element:GetAttribute("uid")))
    end
end)
</code>

---

## 🔹 Readability Utilities

- `nameSelector(name)` → `{ kind = "name", payload = name }`  
- `classSelector(class)` → `{ kind = "class", payload = class }`  
- `attrSelector(key, value)` → `{ kind = "attr", payload = { key = key, value = value } }`  
- `cbSelector(cb)` → `{ kind = "cb", payload = cb }`  
- `uidSelector(uid)` → `{ kind = "uid", payload = uid }`  
- `selector(kind, payload)` → `{ kind = kind, payload = payload }`  
- `listeners(...)` → `{ ... }` (convert multiple arguments to a table)
