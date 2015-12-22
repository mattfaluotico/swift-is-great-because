# swift-is-great-because

Just some reasons why Swift is wonderful

## Optionals don't suck

I hated optionals at first. It was a new concept that I didn't think needed to exist, but that changed when I discovered the power behind them.

You can assume certain variables will *never* be nil.

### if let

### ?? assignment

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

for var i in 0...11 where i % 2 == 0{
  print(i)
}
