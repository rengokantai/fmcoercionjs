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


## Implicit vs explicit coercion
### Explicit Coercion: Strings & Numbers
### Explicit Coercion: Booleans
```
var baz = Boolean(foo);
baz=!!foo;
```
using tilde
```
if(~foo.indexOf("f")){
  alert("found")
}
```


### Implicit Coercion: The Bad Parts
```
"0" ==null
"0"==undefined
"0"==false
"0"==0
```

### Coercion Resources and Surprises
```
parseInt("08");  //0
parseInt(1/0,19); //18
```


### Coercion Resources and Surprises
```
String("abc") instanceof String //false
(new String("abc")) instanceof String;
String("abc") == (new String("abc"));
```
```
Array(5).join("wat"-1)+" Batman";
// NaNNaNNaNNaN Batman!
```
