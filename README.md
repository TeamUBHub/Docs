# Documentation for Library V3

## Load Library
```lua
local UBhub_Lib = loadstring(game:HttpGet("https://gitlab.com/r_soft/main/-/raw/main/Library/V3.lua"))()
```

## Spawn Window
```lua
local Window = UBhub_Lib:MakeWindow({
    Name = "UB Hub : " .. currentPlaceName,
    SubTitle = _G.currentVersion,
    SaveFolder = "UB Hub | Ant War.lua"
  })
```
## Mini Button
```lua
Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://94513440833543", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(35, 1) },
})
```

## Discord Invite
```lua
Home:AddDiscordInvite({
    Name = "UB Hub",
    Description = "Click here to join our discord. Can open Discord automatically if executor has requests function.",
    Logo = "rbxassetid://94513440833543",
    Invite = "https://discord.gg/pn8xyhuSeV",
})
```

## Tab
```lua
local Home = Window:MakeTab({"Home", "scanface"})
```

## Section
```lua
local Section = Tab1:AddSection({"Section"})
```

## Paragraph
```lua
local Paragraph = Tab1:AddParagraph({"Paragraph", "This is a Paragraph\nSecond Line"})
```
## Dialog
```lua
  local Dialog = Window:Dialog({
    Title = "Dialog",
    Text = "This is a Dialog",
    Options = {
      {"Confirm", function()
        
      end},
      {"Maybe", function()
        
      end},
      {"Cancel", function()
        
      end}
    }
  })
```
## Button
```lua
Tab1:AddButton({"Print", function(Value)
print("Hello World!")
end})
```
## Toggle A
```lua
local Toggle1 = Tab1:AddToggle({
  Name = "Toggle",
  Description = "Example toggle A",
  Default = false 
})
Toggle1:Callback(function(Value)
 
end)
```



## Toggle B
```lua
Tab1:AddToggle({
    Name = "Toggle",
    Default = false,
    Callback = function(value)

    end
})
```



## Sliders
```lua
Tab1:AddSlider({
  Name = "Speed",
  Min = 1,
  Max = 100,
  Increase = 1,
  Default = 16,
  Callback = function(Value)
  
  end
})
```

## Dropdown
```lua
local Dropdown = Tab1:AddDropdown({
  Name = "Players List",
  Description = "Select the <font color='rgb(88, 101, 242)'>Number</font>",
  Options = {"one", "two", "three"},
  Default = "two",
  Flag = "dropdown",
  Callback = function(Value)
    
  end
})
```

