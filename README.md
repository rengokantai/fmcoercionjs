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
