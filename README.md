# Simple linter for Lua

Screenshot:

![image](https://user-images.githubusercontent.com/52250786/186773416-38a37abc-e13c-498e-9b9b-997fe4b73643.png)

Before:

```lua
function average(...)
   result = 0
   local arg = {...}
   for i,v in ipairs(arg) do
      result = result + v
   end
   return result/#arg
end

print("The average is",average(10,5,3,4,5,6))
```

After:

```lua
function average(...)
    result = 0
    local arg = {...}

    for i, v in ipairs(arg) do
        result = result + v
    end

    return result / #arg
end

print("The average is", average(10, 5, 3, 4, 5, 6))
```


