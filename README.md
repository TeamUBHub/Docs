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

