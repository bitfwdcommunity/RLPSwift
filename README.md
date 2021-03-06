# RLPSwift
[![Swift 5.3](https://img.shields.io/badge/Swift-5.3-orange.svg?style=flat)](https://developer.apple.com/swift/)
[![Version](https://img.shields.io/cocoapods/v/RLPSwift.svg?stlyle=flat)](https://cocoapods.org/pods/RLPSwift)
[![Travis CI](https://travis-ci.org/bitfwdcommunity/RLPSwift.svg?branch=master)](https://travis-ci.org/bitfwdcommunity/RLPSwift)
[![codecov.io](https://codecov.io/gh/bitfwdcommunity/RLPSwift/branch/master/graph/badge.svg)](https://codecov.io/gh/bitfwdcommunity/RLPSwift/branch/master)

This is a basic Swift implementation of Recursive Length Prefix Encoding, a serialisation method for encoding arbitrarily structured binary data (byte arrays).

You can read more about it here:
* [Ethereum Wiki - RLP](https://github.com/ethereum/wiki/wiki/RLP)
* [Ethereum Yellowpaper](https://ethereum.github.io/yellowpaper/paper.pdf) (Appendix B)

## Interface

```swift
// Encoding Data
RLP.encode(_ data: Data) -> Data

// Encoding String
RLP.encode(_ string: String, with encoding: String.Encoding = .ascii) throws -> Data

// Encoding nested array of Data
RLP.encode(nestedArrayOfData array: [Any]) throws -> Data

// Encoding nested array of String
RLP.encode(nestedArrayOfString array: [Any], encodeStringsWith encoding: String.Encoding = .ascii) throws -> Data
```

## Installation

### Cocoapods

RLPSwift is available through [CocoaPods](http://cocoapods.org).

To install RLPSwift via cocoapods, add the following line to your Podfile:

```ruby
pod 'RLPSwift'
```

Then run `pod install`.


### Swift Package Manager

RLPSwift is available through [Swift Package Manager](https://swift.org/package-manager/).

Once you have your Swift package set up, adding RLPSwift as a dependency is as easy as adding it to the `dependencies` value of your `Package.swift`.

```swift
dependencies: [
  .package(url: "https://github.com/bitfwdcommunity/RLPSwift.git", from: "0.0.4")
]
```

## License

RLPSwift is released under an [MIT](https://tldrlegal.com/license/mit-license) license. See [LICENSE](LICENSE) for more information.
