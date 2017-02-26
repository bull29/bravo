# bravo
welcome! notable documentation is outlined below



# misc
```lua
ExecuteScriptOnEvent( string hookevent ) do return end -- Executes the current file which this function is called in on a hook NOTE: MUST BE CALLED EXACTLY IN THE FORMAT SHOWN with do return end right after
print() -- By default, NFOServers' hosting doesn't show print statements in console. 
```
# hooks

```lua
hook.Clean( string event ) -- Clears all (lua) functions associated with an event
hook.SearchCode( string code ) -- Traverses through EVERY single hook function added through lua and displays if it found any. Useful for finding those pesky print statements. Warning: Resource intensive 
hook.RunOnce( string event, function func ) -- Runs any function just once on a hook. Alternative to hook.Add
	-- Alternatively; can be called directly on a string
	("HUDPaint"):RunOnce( function func )
```
# panel
```lua
panel:GetHorizontalPos() -- returns the panel's x position
panel:GetVerticalPos() -- returns the panel's y position

panel:SetHorizontalPos( number n ) -- sets the panel's y position
panel:SetVerticalPos( number n ) -- sets the panel's x position

```
# color

```lua
Color() + <number or Color> -- Returns an increment of a color based on a single value or the rgb of another color
Color() - <number or Color> -- Returns a decrement of a color based on a single value or the rgb of another color
-Color() -- Returns the contrasting color aka 'opposite' ( Prefix - )
```
