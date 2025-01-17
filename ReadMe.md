# What is SlayerzUI?
SlayerzUI was the first user interface I created and was continuously developed and improved until 2022 when it was discontinued.

![Example](https://github.com/x2neptunereal/SlayerzUI/blob/main/Example.png)
# Document Library
**Setup Library**
```lua
local SlayerzLibrary = loadstring(
    game:HttpGet(
        "https://raw.githubusercontent.com/x2neptunereal/SlayerzUI/main/Source/Library.lua"
    )
)()
```
**Creating a Window**
```lua
local Window = SlayerzLibrary:Window(
    "SlayerzUI", -- Name Hub <string>
    "This ui made by Slayerz - API", -- Description <string>
    "rbxassetid://15110884615", -- Logo Image <string>
    Color3.fromRGB(255, 0, 0) -- UI Color <color3>
)
```
**Creating a Tab**
```lua
local Tab1 = Window:Tab(
    "Tab 1" -- Tab Name <string>
)
```
**Creating a Section**
```lua
local Section = Tab1:Section(
    "- Section -", -- Section Name <string>
    "Left" -- Left / Right <string>
)
```
**Creating a Text Label**
```lua
local Label = Section:Label(
    "This is Label" -- Text <string>
)
```
**Update a Text Label**
```lua
Label:Change(
    "This is new Text" -- New Text <string>
)
```
**Creating a Button**
```lua
Section:Button(
    "Button", -- Button Name <string>
    function() -- Callback Function <function>
        print("Click")
    end
)
```
**Creating a Toggle**
```lua
local Toggle = Section:Toggle(
    "Toggle", -- Toggle Name <string>
    false, -- Default <boolean>
    function(value) -- Callback Function <function> ( return "value" boolean )
        print("Toggle - "..tostring(value))
    end
)
```
**Update a Toggle**
```lua
Toggle:Update(
    true -- New Toggle Value <boolean>
)
```
**Creating a Text Box**
```lua
Section:Textbox(
    "Text Box", -- Text Box Name <string>
    "Value ?", -- Holder Text <string>
    function(value) -- Callback Function <function> ( return "value" string )
        print("Input - "..value)
    end
)
```
**Creating a Dropdown**
```lua
local Dropdown = Section:Dropdown(
    "Dropdown", -- Dropdown Name <string>
    {"ABC","XYZ","1","2"}, -- Data <tabel>
    {"Select Dropdown"}, -- Holder Text <tabel>
    function(value) -- Callback Function <function> ( return "value" index in tabel )
        print("Select - "..value)
    end
)
```
**Add items in Dropdown**
```lua
Dropdown:Add(
    "New item" -- New Item <string>
)
```
**Clear Dropdown items**
```lua
Dropdown:Clear() -- <void>
```
**Creating a Silder**
```lua
Section:Slider(
    "Slider", -- Slider Name <string>
    1, -- Min <number>
    100, -- Max <number>
    25, -- Default <number>
    function(value) -- Callback Function <function> ( return "value" number )
        print("Slider to - "..tostring(value))
    end)
```
**Setup Mobile Toggle**
```lua
local SlayerzMobileToggle = loadstring(
    game:HttpGet(
        "https://raw.githubusercontent.com/x2neptunereal/SlayerzUI/main/Source/MobileToggle.lua"
    )
)()
MobileToggle:Create(
    "rbxassetid://15110884615" -- Logo Image <string>
)
```
**Setup Notification**
```lua
local SlayerzNotify = loadstring(
    game:HttpGet(
        "https://raw.githubusercontent.com/x2neptunereal/SlayerzUI/main/Source/Notification.lua"
    )
)()
```
**Creating a Notification**
```lua
SlayerzNotify:Notify(
    "Slayerz UI", -- Topic <string>
    "This is Notification for Slayerz UI Library", -- Description <string>
    "rbxassetid://15110884615", -- Logo Image <string>
    Color3.fromRGB(255, 0, 0), -- Notify Color <color3>
    5 -- Duration <number>
)
```
