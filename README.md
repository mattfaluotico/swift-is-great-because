# swift-is-great-because

Just some reasons why Swift is wonderful

## Optionals don't suck

I hated optionals at first. It was a new concept that I didn't think needed to exist, but that changed when I discovered the power behind them.

You can assume certain variables will *never* be nil.

### Safely vs Force unwrapping

When accessing a property of performing a method on an optional value, you have the choice to either safely unwrap for force unwrap to object. The `?` represents the safe unwrap and the `!` represents the forceful. 

Force *unwrapping* will throw an error if the object ends up being nil while a safe unwrap will just not perform the statement.

**Safely unwrapping**

When the view controller doesn't have a navigationController this method is never performed

```
self.navigationController?.setBackgroundColor(.blueColor()); 
```

**Force Unwrapping**

When the view controller doesn't have a navigationController this will throw an error

```
self.navigationController!.setBackgroundColor(.blueColor()); 
```

### if let

Rather than unwrapping your optional each time you want to get or set it's properties, you can unwrap it once with an `if let` statement.

```swift
if let nav = self.navigationController {
  nav.backgroundColor = UIColor.blueColor();
  nav...
}
```

### ?? assignment

Similar to the shorting tertiary assignment in Objective-C, Swift comes with an if-this-is-nil assignment. It will automatically unwrap optionals as well!

```swift
// Assume self.cactus is an optional..

let cactus = self.cactus ?? Cactus.saguaro();
```

This will assign `cactus` to `self.cactus` if self.cactus is not nil, otherwise it will assign `Cactus.saguaro()`  to `cactus`.

## Guard

You know when you need to check 3 or 7 different conditions before you can perform a specific statement? And then, to add to it, those conditions are dependent on one another? You end up with a huge `if` pyramid. That's ugly.

So Swift introduced `guard`.

```swift
example
```

## for loop filtering

How many times is the first statement in your for-loop a conditional?

```swift
for var i in 0...11 {
  if i % 2 == 0 {
    print(i)
  }
}
```

Swift lets you save a line

```swift
for var i in 0...11 where i % 2 == 0{
  print(i)
}
```

## Escaped Keywords

Sometimes a keyword (or reserver words) is actually the most ideal word you can use to describe a function name...

```swift
func findIndexOf element: String, in array: [String]) -> Int { ...
```

This isn't going to work because of the use of the keyword "in".

Luckily, Swift lets you escape keywords with backticks allowing their use in function names

```swift
func findIndexOf element: String, `in` array: [String]) -> Int { ...
```