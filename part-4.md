# Part Four

## Currying
* A Curried Function is a function that only takes a single parameter at a time.

## Currying and Refactoring
* Parameter order is important to fuly leverage curring.

## Common Functional Functions
### Map
```
map = (f, array) => {
    let newArray = []
    for (let i = 0; i < array.length; i++) newArray[i] = f(array[i])
    return newArray
}
```

### Filter
```
filter = (pred, array) => {
    let newArray = []
    for(let i = 0; i < array.length; i++)
        if(pred(array[i])) newArray[newArray.length] = array[i]
    return newArray
}
```

### Reduce
```
reduce = (f, start, array) => {
    let acc = start
    for(let i = 0; i < array.length; i++) acc = f(array[i], acc)
    return acc
}
```
