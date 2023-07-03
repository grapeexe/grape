
# grape.cc🍇 UI Lib

A "how to" use this UI lib.

## Features

 - Tabs
 - TextButtons
 - TextLabels
 - TextBox
 - Toggles
 - Dropdowns
 - Value changer
## Docs

Connecting to the UI lib source
```
local grape = loadstring(game:HttpGet("https://raw.github.com/grapeexe/grape/main/ui/src"))()
```

Creating the UI lib
```
-- // Args -> 1: Title
local lib = grape:Create(
    "Grape" -- // 1: Title
)
```

Creating a tab
```
-- // Args -> 1: Name
local tab = lib.NewTab(
    "A tab" -- // 1: Name
)
```

Creating & updating a text label
```
-- // Args -> 1: Text
local label = tab.NewLabel(
    "Hello" -- // 1: Text
)
label.Update(
    "Welcome" -- // 1: Text
)
```

Creating a text button
```
-- // Args -> 1: Text 2: Suggestion 3: Callback
tab.NewButton(
    "Button", -- // 1: Text
    "This button does something", -- // 2: Suggestion
    function() print("HI") end -- // 3: Callback
)
```

Creating a toggle button
```
-- // Args -> 1: Text 2: Suggestion 3: Enabled 4: Callback
local toggle = tab.NewToggle(
    "Toggle button", -- // 1: Text
    "This button toggles", -- // 2: Suggestion
    false, -- // 3: Enabled
    function(bool) print(bool) end -- // 4: Callback
)
toggle.Update(
    "new toggle" -- // 1: Text
)
toggle.toggle() -- // enables / disables
```

Creating & modifying a text box
```
-- // Args -> 1: Text 2: Suggestion 3: Stock 4: Callback
tab.NewTextbox(
    "Textbox", -- // 1: Text
    "Strange box", -- // 2: Suggestion
    "good", -- // 3: Stock
    function(t) print(t) end -- // 4: Callback
)
```

Creating & updating a dropdown
```
-- // Args -> 1: Text 2: Suggestion 3: Items 4: Callback
local dropdown = tab.NewDropdown(
    "Dropdown", -- // 1: Text
    "pick something", -- // 2: Suggestion
    {"1","2","3"}, -- // 3: Items
    function(t) print(t) end -- // 4: Callback
)
dropdown.Update(
    {"hi","bye"} -- // 1: Items
)
```

Creating a new value
```
-- // Args -> 1: Text 2: Suggestion 3: Incremence 4: Min 5: Max 6: Stock 7: Callback
tab.NewValue(
    "value", -- // 1: Text
    "make value", -- // 2: Suggestion
    10, -- // 3: Incremence
    0, -- // 4: Min
    100, -- // 5: Max
    10, -- // 6: Stock
    function(t) print(t) end  -- // 7: Callback
)
```
