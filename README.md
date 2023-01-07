# Closures
All Closure types



**Simple closure**
```
let closure = {
    print("This is a closure and at the same time it is a function")
}
closure()
```


**Closure with parameters**
```
let closure2 = { (param: String) in
    print("this is a \(param) in the closure2")
}
closure2("parameter")
```

**Closure with params**
```
let closureWithParameters = { (name: String, id: Int) in
    print("\(name) \(id)")
}
closureWithParameters("Ahmet", 17)
```

**Returns closure**
```
let closureWithParamAndReturn = { (param: String) -> String in
    return "Closure with returning \(param)"
}
let closureWithReturningObject = closureWithParamAndReturn("parameter")
print(closureWithReturningObject)

let closureWithouthParamAndWithReturns = { () -> Bool in
    print("Closure without param and with returns")
    return true
}
closureWithouthParamAndWithReturns()

```
    
    
    
