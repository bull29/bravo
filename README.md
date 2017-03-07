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
panel:RecurseChildren( function func ) -- Runs a function( panel ) on a panel and every single child recursively 
panel:pDock( number padding ) -- 'Fake' Docks a panel by using panel.SetSize and panel.SetPos - Takes into account DFrames
```
## color

```lua
Color() + <number or Color> -- Returns an increment of a color based on a single value or the rgb of another color
Color() - <number or Color> -- Returns a decrement of a color based on a single value or the rgb of another color
-Color() -- Returns the contrasting color aka 'opposite' ( Prefix -; example -Color( 255, 0, 0 ))
Color:Approach( target, amount ) -- Returns an increment of a color approaching another color
Color:Lerp( target, factor ) -- Returns a lerp'd increment 
```

## strings
```lua
-- Disabled by default
-<String> -- Returns the reversed string
<String>^ num -- Returns string.rep( num )
<String> % var -- Same as <String>:find( tostring( var ) )
<String> + <String> -- concat
```

## util
```lua
util.PoolNetworkStrings( ... ) -- util.AddNetworkString all those pesky strings at once
```
## misc
```lua
ExecuteScriptOnEvent( string hookevent ) do return end -- Executes the current file which this function is called in on a hook NOTE: MUST BE CALLED EXACTLY IN THE FORMAT SHOWN with do return end right after
print() -- Note: Not activated by default. NFOServers doesn't show print statements in console, only serverlogs. With this override, it does.
_void() -- Ever needed a global function which does absolutely nothing for an arbitrary reason? 
```
