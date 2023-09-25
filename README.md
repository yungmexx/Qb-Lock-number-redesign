# qb-lock


![image](https://github.com/yungmexx/Qb-Lock-number-redesign/assets/113365369/141003e1-3a5d-45a9-b87c-80bd969469a8)
![image](https://github.com/yungmexx/Qb-Lock-number-redesign/assets/113365369/9a665a20-9aa6-4111-a161-7e2a273a45d7)
![image](https://github.com/yungmexx/Qb-Lock-number-redesign/assets/113365369/25a8ff6b-f23f-4175-a76b-04d9a6abc1ed)





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


## Useful Snippet
for everyone here that wants to add the minigame to other script in a very simple way

```lua

local seconds = math.random(9,12)
local circles = math.random(1,3)
local success = exports['qb-lock']:StartLockPickCircle(circles, seconds, success)
if success then
QBCore.Functions.Notify(" Success", "success")
end
```
