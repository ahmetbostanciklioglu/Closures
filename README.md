# Closures



**Simple closure:**
```
let closure = {
    print("This is a closure and at the same time it is a function")
}
closure()
```


**Closure with parameters:**
```
let closure2 = { (param: String) in
    print("this is a \(param) in the closure2")
}
closure2("parameter")
```

**Closure with params:**
```
let closureWithParameters = { (name: String, id: Int) in
    print("\(name) \(id)")
}
closureWithParameters("Ahmet", 17)
```

**Returns closure:**
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


**Closures are parameters in functions:**
```
let closureAsAParameter = {
    print("closure as a parameter")
}

func closureFunction(closure: () -> Void) {
    print("=======")
    closure()
    print("=======")
}
closureFunction(closure: closureAsAParameter)


var closure5 = {
    print("closure5")
    print("========")
}

func func5(_ closure5: ()->Void) {
    closure5()
}
func5(closure5)


var closure6 = {
    print("closure6")
}
func func6(clos closure6: () -> Void) -> String {
    closure6()
    return "========"
}
print(func6(clos: closure6))


let closure8 = {
    return "closure8"
}
func func8(clos closure8: () -> String) -> String  {
    let const: String =  closure8()
    return const
}
print(func8(clos: closure8))


let closureWithReturn = { () -> String in
    return "closure19"
}
func closure9(param: inout String, _ closure9: ()-> String) -> Void {
    print("========")
    closure9()
    print("========")
    param = closure9()
    
}
var parameters = "closure9"
closure9(param: &parameters, closureWithReturn)
print(parameters)
```
