# fmcoercionjs
## Coercion
### ToString
```
String(null) = "null"
String(0) = "0"
String(-0)="0"
```

toString
```
[,,,,].toString=",,,"
[].toString() = ""
[1,2,3].toString()="1,2,3"
[null,undefined].toString()=","
```
### ToNumber
```
"" 0
"0" 0
"-0" -0
"  009  " 9
"3.14" 3.14
"0." 0
".0" 0
"." NaN
"0xaf" 175
false 0
true 1
null 0
undefined NaN
```
First use```valueOf()```, then```toString()```
###### other examples
```
[""] 0
["0"] 0
["-0"] -0
[null] 0
[undefined] 0
[1,2,3] NaN
[[[]]] 0
```

### ToBoolean
Falsy|truthy
---|---
0 -0 +0 |
null |
NaN |
false |
undefined | 

Means
- Truthy, if you legitimately do a boolean coercion on it, it become a true value
