# qb-lock


![image](https://github.com/yungmexx/Qb-Lock-number-redesign/assets/113365369/eeae6ea5-cdfe-4383-80e0-d645457d2e86)
![image](https://github.com/yungmexx/Qb-Lock-number-redesign/assets/113365369/1c959892-5cd9-4854-8edc-391c50f42d34)
![Uploading image.png…]()


# Template
```lua

exports['qb-lock']:StartLockPickCircle(amount, time, function(success)

```
# Example useage
```lua

RegisterCommand("lpgame", function()
	local time = math.random(7,10)
	local circles = math.random(2,4)
	local success = exports['qb-lock']:StartLockPickCircle(circles, time, success)
	print(success)
	if success then
		print("WIN")
	else
		print("FAIL")
	end
end)

```

# Amount of time to spin and amount of time to trigger are currently held within the js I am trying to export it to lua
# Amount and Time now work, but functioning success now doesn't go over to the export.
# Fixed the Lockpick now ready for use, enjoy!

## Useful Snippet
for everyone here that wants to add the minigame to other script in a very simple way

```lua

local seconds = math.random(9,12)
local circles = math.random(1,3)
local success = exports['qb-lock']:StartLockPickCircle(circles, seconds, success)
if success then
QBCore.Functions.Notify("Tex is awesome", "success")
end
```
