### Null Safety

```
var a: String = "abc"
a = null // compilation error
```

```
var b: String? = "abc"
b = null // ok
```
<br />
```
val l = a.length
```

```
val l = b.length // error: variable 'b' can be null
```

Note:
+ Compilation errors are thrown anytime the compiler thinks there COULD be a null reference error