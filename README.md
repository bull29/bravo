# bravo
welcome! notable documentation is outlined below

## hooks
```lua
hook.Clean( string event ) -- Clears all (lua) functions associated with an event
hook.SearchCode( string code ) -- Traverses through EVERY single hook function added through lua and displays if it found any. Useful for finding those pesky print statements. Warning: Resource intensive
hook.OnCount( string event, number iterations, function func ) -- Executes a function x amount of times on a hook. The function itself returns a getter and setter( n ) to alter the current iteration its' at
hook.RunOnce( string event, function func ) -- Runs any function just once on a hook. Alternative to hook.Add, practically equivalent to hook.OnCount( _, 1, _ ). Can also be called directly on a string.
```
## panel
```lua
panel:GetHorizontalPos() -- returns the panel's x position
panel:GetVerticalPos() -- returns the panel's y position
panel:SetHorizontalPos( number n ) -- sets the panel's y position
panel:SetVerticalPos( number n ) -- sets the panel's x position

```
## color

```lua
Color() + <number or Color> -- Returns an increment of a color based on a single value or the rgb of another color
Color() - <number or Color> -- Returns a decrement of a color based on a single value or the rgb of another color
-Color() -- Returns the contrasting color aka 'opposite' ( Prefix - )
```

## misc
```lua
ExecuteScriptOnEvent( string hookevent ) do return end -- Executes the current file which this function is called in on a hook NOTE: MUST BE CALLED EXACTLY IN THE FORMAT SHOWN with do return end right after
print() -- Note: Not activated by default. NFOServers doesn't show print statements in console, only serverlogs. With this override, it does.
```
