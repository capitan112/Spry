![](https://travis-ci.org/shaps80/Spry.svg?branch=master)

# Spry

Spry is a Swift Playgrounds Unit Testing library based on [Nimble](http://github.com/Quick/Nimble).

<img src="https://github.com/shaps80/Spry/raw/master/playground.png" width=658 height=100%>

The best thing about Spry is that the API matches Nimble perfectly. Which means once you've created your code and tests in a Playground, you can copy them directly into your Xcode project without needing to (re)write them again :)

# Download

There are a couple of ways you can download Spry.

## Template
You can download a Playground including the lastest version of Spry. Consider this a boilerplate template. It includes Spry in the `Sources` folder of the Playground, so you can simply start writing tests alongside your code in the Playground.

[Download Playground](https://github.com/shaps80/Spry/raw/master/Spry-Playground.zip)

## Manual
You can also download or checkout this repo and simply copy the files into your existing Playground manually. Simply copy the entire `Spry` folder into your Playground's `Sources` folder. Easy Peasy!

# Nimble-esque

Spry is a stripped down (Lite) version of Nimble that includes a subset of Nimble's Matchers.

> Note: This is a port of Nimble only, since [Quick](http://github.com/Quick/Quick) doesn't really make sense in the context of a Playground.

The following features are **NOT** supported (since they are a part of Quick):

`describe`  
`context`  
`it`

Spry supports the following features:

<input type="checkbox" disabled checked>`expect`  
<input type="checkbox" disabled checked>`to`  
<input type="checkbox" disabled checked>`toEventually`  
<input type="checkbox" disabled>`failWithMessage`  
<input type="checkbox" disabled checked>`beAKindOf`  
<input type="checkbox" disabled checked>`beAnInstanceOf`  
<input type="checkbox" disabled checked>`beCloseTo`  
<input type="checkbox" disabled checked>`beEmpty`  
<input type="checkbox" disabled checked>`beginWith`  
<input type="checkbox" disabled checked>`beGreaterThan`  
<input type="checkbox" disabled checked>`beGreaterThanOrEqualTo`  
<input type="checkbox" disabled checked>`beIdenticalTo`  
<input type="checkbox" disabled checked>`beLessThan`  
<input type="checkbox" disabled checked>`beLessThanOrEqualTo`  
<input type="checkbox" disabled checked>`beLogical`  
<input type="checkbox" disabled checked>`beNil`  
<input type="checkbox" disabled checked>`beVoid`  
<input type="checkbox" disabled checked>`containElementSatisfying`  
<input type="checkbox" disabled checked>`contain`  
<input type="checkbox" disabled checked>`endWith`  
<input type="checkbox" disabled checked>`equal`  
<input type="checkbox" disabled checked>`haveCount`  
<input type="checkbox" disabled checked>`match`  
<input type="checkbox" disabled checked>`satisfyAnyOf`  
<input type="checkbox" disabled>`async`  
<input type="checkbox" disabled>`matchError`  
<input type="checkbox" disabled>`throwError`  

# Usage

Using Spry is as simple as writing an `expect` case:

```swift
func add<T: ExpressibleByIntegerLiteral>(_ x: T, _ y: T) -> T {
    return x + y
}

// Spry test case
expect(add(4, 5)).to(equal(9))
```

If you're already familiar with Nimble, then you already know how to use Spry.

> For full details on how to write your tests with Spry, I suggest reading over the [Nimble docs](https://github.com/Quick/Nimble/blob/master/README.md). Keeping in mind that not all features are currently included.
