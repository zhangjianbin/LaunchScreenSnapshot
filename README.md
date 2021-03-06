# LaunchScreenSnapshot

[![Twitter](https://img.shields.io/badge/contact-@alexruperez-0FABFF.svg?style=flat)](http://twitter.com/alexruperez)
[![Version](https://img.shields.io/cocoapods/v/LaunchScreenSnapshot.svg?style=flat)](http://cocoapods.org/pods/LaunchScreenSnapshot)
[![License](https://img.shields.io/cocoapods/l/LaunchScreenSnapshot.svg?style=flat)](http://cocoapods.org/pods/LaunchScreenSnapshot)
[![Platform](https://img.shields.io/cocoapods/p/LaunchScreenSnapshot.svg?style=flat)](http://cocoapods.org/pods/LaunchScreenSnapshot)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![Swift Package Manager Compatible](https://img.shields.io/badge/Swift%20Package%20Manager-compatible-4BC51D.svg?style=flat)](https://github.com/apple/swift-package-manager)
[![Build Status](https://travis-ci.org/alexruperez/LaunchScreenSnapshot.svg?branch=master)](https://travis-ci.org/alexruperez/LaunchScreenSnapshot)
[![Code Coverage](https://codecov.io/gh/alexruperez/LaunchScreenSnapshot/branch/master/graph/badge.svg)](https://codecov.io/gh/alexruperez/LaunchScreenSnapshot)
[![codebeat badge](https://codebeat.co/badges/97c6f7e9-baa5-4c73-bb2c-ba31b7ccecd3)](https://codebeat.co/projects/github-com-alexruperez-launchscreensnapshot-master)

*LaunchScreenSnapshot* protects sensitive data in your app snapshot.

![*LaunchScreenSnapshot*](https://raw.githubusercontent.com/alexruperez/LaunchScreenSnapshot/master/LaunchScreenSnapshot.gif)

## Installation

LaunchScreenSnapshot is available through [*CocoaPods*](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'LaunchScreenSnapshot'
```

#### Or you can install it with [*Carthage*](https://github.com/Carthage/Carthage):

```ogdl
github "alexruperez/LaunchScreenSnapshot"
```

#### Or install it with [*Swift Package Manager*](https://swift.org/package-manager/):

```swift
dependencies: [
    .Package(url: "https://github.com/alexruperez/LaunchScreenSnapshot.git")
]
```

## Usage

#### Protect your app snapshot:

```swift
LaunchScreenSnapshot.protect()
```

#### Unprotect your app snapshot:

```swift
LaunchScreenSnapshot.unprotect()
```

### Advanced usage

#### Shared instance:

```swift
let launchScreenSnapshot = LaunchScreenSnapshot.shared
```

#### Custom built:

```swift
let launchScreenSnapshot = LaunchScreenSnapshot(application: UIApplication, notificationCenter: NotificationCenter, bundle: Bundle)
```

#### Provided parameters:

```swift
let restoreAnimationOptions = LaunchScreenSnapshot.Animation(duration: TimeInterval, delay: TimeInterval, dampingRatio: CGFloat, velocity: CGFloat, options: UIViewAnimationOptions)
launchScreenSnapshot.protect(with: UIView?, trigger: LaunchScreenSnapshot.Trigger, animation: restoreAnimationOptions, force: Bool)
```

## Etc.

* Contributions are very welcome.
* Attribution is appreciated (let's spread the word!), but not mandatory.

## Authors

[alexruperez](https://github.com/alexruperez), contact@alexruperez.com

## License

*LaunchScreenSnapshot* is available under the MIT license. See the LICENSE file for more info.
