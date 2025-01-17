# What is SlayerzUI?
SlayerzUI was the first user interface I created and was continuously developed and improved until 2022 when it was discontinued.

![Example]()
# Document Library
**Load Library**
```lua
local SlayerzLibrary = loadstring(game:HttpGet("https://github.com/x2neptunereal/SlayerzUI/blob/main/Source/Library.lua"))()
```
**Creating a Window**
```lua
local Window = SlayerzLibrary:Window(
    "SlayerzUI", -- Name Hub <string>
    "This ui made by Slayerz - API", -- Description in script <string>
    "rbxassetid://15110884615", -- Image Id <string>
    Color3.fromRGB(255, 0, 0) -- Color in UI <color3>
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
    "- Section 1 -", -- Section Name <string>
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
