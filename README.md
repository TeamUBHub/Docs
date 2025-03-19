# Documentation for Library V2

## Load GUI Base


```lua
local Module = loadstring(game:HttpGet("https://gitlab.com/r_soft/main/-/raw/main/ScriptStarter.lua"))()
local Library = Module.Library
local SaveManager = Module.SaveManager
local Window = Module.Window
local Testers = Module.Testers
SaveManager:SetLibrary(Library)
SaveManager:SetFolder("UBHub/Westbound")
```

## Set Version
```lua
_G.currentVersion = "Version : 2.0.0"
```

## Tab
```lua
local Tabs = {
    Home = Window:AddTab({ Title = "Home", Icon = "scan-face"}),
    Main = Window:AddTab({ Title = "Main", Icon = "layout-grid"}),
}
```

## Section
```lua
local LPsection = Tabs.Home:AddSection("LocalPlayer")
```

## Paragraph
```lua
Tab:AddParagraph({
    Title = "Paragraph",
    Content = "This is a paragraph.\nSecond line!"
})
```
## Dialog
```lua
Window:Dialog({
    Title = "Title",
    Content = "This is a dialog",
    Buttons = {
        { 
            Title = "Confirm",
            Callback = function()
                print("Confirmed the dialog.")
            end 
        }, {
            Title = "Cancel",
            Callback = function()
                print("Cancelled the dialog.")
            end 
        }
    }
})
```
## Button
```lua
Tab:AddButton({
    Title = "Button",
    Description = "Very important button",
    Callback = function()
        print("Hello, world!")
    end
})
```
## Toggle A
```lua
local Toggle = Tab:AddToggle("MyToggle", 
{
    Title = "Toggle", 
    Description = "Toggle description",
    Default = false
    Callback = function(state)
	if state then
	    print("Toggle On")
	else
	    print("Toggle Off")
        end
    end 
})
```
## Sliders
```lua
local Slider = Tab:AddSlider("Slider", 
{
    Title = "Slider",
    Description = "This is a slider",
    Default = 2,
    Min = 0,
    Max = 5,
    Rounding = 1,
    Callback = function(Value)
        print("Slider was changed:", Value)
    end
})
```

## Dropdown
```lua
local Dropdown = Tab:AddDropdown("Dropdown", {
    Title = "Dropdown",
    Description = "Dropdown description",
    Values = {"one", "two", "three", "four", "five", "six", "seven", "eight", "nine", "ten", "eleven", "twelve", "thirteen", "fourteen"},
    Multi = false,
    Default = 1,
})
```
### Set Dropdown Value
```lua
Dropdown:SetValues(playerNames)
```




