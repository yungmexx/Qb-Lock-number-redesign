# qb-lock


![image](https://github.com/yungmexx/Qb-Lock-number-redesign/assets/113365369/beb6f3aa-d15b-4dd2-81c6-a0046d4738e8)
![image](https://github.com/yungmexx/Qb-Lock-number-redesign/assets/113365369/1c959892-5cd9-4854-8edc-391c50f42d34)
![image](https://github.com/yungmexx/Qb-Lock-number-redesign/assets/113365369/6fbef68a-9893-4ca4-bb2f-6eb40c23d6df)




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
