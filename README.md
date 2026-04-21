# Tuff UI
> A free, modern Roblox UI library for building script hubs, admin menus, and settings panels.

![Tuff UI v1] <img width="960" height="710" alt="image" src="https://github.com/user-attachments/assets/4564ff95-b3e5-4ab4-807e-02678229fd7c" />


---

## What is Tuff UI?
Tuff UI is a lightweight Roblox UI library built for exploiters and developers who want a clean, dark-themed menu without building one from scratch. It's free, open source, and easy to script with.

---

## Load It
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/SkipperTuff/TuffUiLibrary/main/Main"))()
```

---

## Quick Start
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/SkipperTuff/TuffUiLibrary/main/Main"))()

local Window = Library:CreateWindow("My Hub")
local Main = Window:AddTab("Main")

Main:AddButton("Click Me", function()
    print("clicked!")
end)
```

---

## Elements

| Element | Method |
|---|---|
| Button | `AddButton(name, callback, desc)` |
| Toggle | `AddToggle(name, options, desc)` |
| Slider | `AddSlider(name, options, desc)` |
| Dropdown | `AddDropdown(name, options, desc)` |
| Input | `AddInput(name, placeholder, callback, desc)` |
| Paragraph | `AddParagraph(title, text)` |
| Notification | `Library:Notify(text)` |

---

## Full Example
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/SkipperTuff/TuffUiLibrary/main/Main"))()

local Window = Library:CreateWindow("Tuff UI Example")
local Main = Window:AddTab("Main")
local Settings = Window:AddTab("Settings")

Library:Notify("Loaded")

Main:AddButton("Button", function()
    print("Button clicked")
end, "basic button")

Main:AddToggle("Toggle", {
    Default = false,
    Callback = function(state)
        print("Toggle:", state)
    end
}, "on / off switch")

Main:AddSlider("Slider", {
    Min = 0,
    Max = 100,
    Default = 50,
    Increment = 1,
    Callback = function(value)
        print("Slider:", value)
    end
}, "number value")

Main:AddDropdown("Dropdown", {
    Options = {"1","2","3","4","5"},
    Default = "1",
    Callback = function(option)
        print("Dropdown:", option)
    end
}, "pick an option")

Settings:AddButton("Destroy UI", function()
    Window:Destroy()
end, "close the ui")
```

---

## Links
- 📄 **Docs:** https://skippertuff.github.io/TuffUDocs/
- 💬 **Discord:** https://discord.com/invite/fgukyz7tPM

---

*Tuff UI is currently in beta. Free to use, edit, and build hubs with.*
