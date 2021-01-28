Init Swift

<p align="center">
  <a href="https://flutter.io/">
    <img src="https://cdn4.iconfinder.com/data/icons/logos-3/504/Swift-2-512.png" alt="Logo" width=72 height=72>
  </a>

  <h3 align="center">Flutter Init Project</h3>

  <p align="center">
    Fork this project then start you project with a lot of stuck prepare
    <br>
    Base project made with much  :heart: . Contains CRUD, patterns, and much more!
    <br>
    <br>
    <a href="https://github.com/PingAK9/init-swift/issues/new">Report bug</a>
    ·
    <a href="https://github.com/PingAK9/init-swift/issues/new">Request feature</a>
  </p>
</p>


# Content
- [Architecting iOS Project](#architecting-ios-project)
- [Conventions](#conventions)
- [Dependencies](#dependencies)
- [Widget](#widget)

- Find more [Awesome iOS](https://github.com/vsouza/awesome-ios)

# Architecting iOS Project

```
├─ Models
  ├─ User.swift
  ├─ Post.swift
├─ Network
├─ Libraries 
├─ Feature
  ├─ Login
    ├─ LoginManager.swift
    ├─ LoginViewController.swift
    ├─ LoginHeaderView.swift
  ├─ Feed
    ├─ FeedViewController.swift
    ├─ FeedTableViewCell.swift 
├─ Application
  ├─ Main
    ├─ AppDelegate.swift
    ├─ MainViewController.swift
    ├─ LaunchScreen.storyboard
  ├─ Config
    ├─ Config.swift
    ├─ Env.swift
  ├─ Common
    ├─ Controls
      ├─ BouncingButton.swift
├─ Utils
  ├─ Extensions
    ├─ UIView+Extensions.swift
    ├─ NSURL+Extensions.swift
    ├─ String+Extensions.swift
    ├─ Date+Extensions.swift
    ├─ NotificationName+Extensions.swift
  ├─ Utils
    ├─ Utils.swift
    ├─ Contants.swift
    ├─ Content.swift
    ├─ Config.swift
├─ Assets
  ├─ Images.xcassets
  ├─ Sounds
    ├─ success.wav
  ├─ Videos
    ├─ intro-onboarding.mp4
```


- **CoreData**: Contains DataModel and Entity Classes.
- **Extension**: Contain One class(default apple class extensions+project class extensions.)
- **Helper**: Contain Third Party classes/Frameworks (eg. SWRevealController) + Bridging classes (eg. Obj C class in Swift based project)
- **Model**: Make a singleton class (eg.AppModel - NSArray,NSDictionary, String etc.) for saving data. The Web Service Response parsing and storing data is also done here.
- **Networking**: The app's networking layer (e.g. classes responsible for interacting with web services)
- **Services**: Contain Web Service processes (eg. Login Verification, HTTP Request/Response)
- **View**: Contain storyboard, LaunchScreen.XIB and View Classes. Make a sub folder Cells - contain UITableViewCell, UICollectionViewCell etc.
- **Controller**: Contain Logic or Code related to UIElements (eg. UIButton’s reference+ clicked action)
- **Modules**: Here we can find each of the application's pieces divided by functionality
  - Module-based folders: Each folder contains all module-specific view controllers, views, delegates and related classes
- **Feature**:
- **Common**:
- **Config**: Config and Env to improve quality
- **Libraries**: Manager third-party libraries, Wrapper it with your functions. It is easy for upgrade, mainten or change library

**Note**: name all your models something like UserModel.swift and PostModel.swift
```
viewControllers as LoginViewController
managers as LoginManager
non-view controllers as FeedController
extensions as +Additions
```

# Conventions
> First establish a naming conventions for all the things: file name, class name, function/variables name, project name, image ...
- Use **Pascal Case** for file, folder and class
  > Start with capital letter i.e. Controller, MyClass, BestAppEver ...
- Use **Camel Case** for methods, properties and variables
  > Start with lowercase letter i.e. setFirstName, useMethod, fullName ...
- Naming images file on state
  > button_blue_normal.png, button_blue_highlight.png
 
 [More by Apple](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html)
 
 
# Dependencies
## Alamofire: Networking
- https://github.com/Alamofire/Alamofire

Alamofire is AFNetworking’s successor but is written in Swift. You might be wondering why there are two different networking libraries in the upper echelon of this list, but I assume it’s due to the fact that networking libraries are just extremely useful for iOS app development. The two libraries share a similar feature set, with the main difference being the language in which they are written.

Other [AFNetworking](https://github.com/AFNetworking/AFNetworking)

## kingfisher: Cache and Load Image
- https://github.com/onevcat/Kingfisher

Similar to SDWebImage, Kingfisher is a library for downloading and caching images that is written purely in Swift. It includes extensions for UIImageView and UIButton, which makes it more obliging. You can also add a placeholder image that should show while the actual image is downloading.

Other [SDWebImage](https://github.com/rs/SDWebImage)

## Toast and snackber
- [Toast-Swift](https://github.com/scalessec/Toast-Swift)

Toast-Swift is a Swift extension that adds toast notifications to the UIView object class. It is intended to be simple, lightweight, and easy to use. Most toast notifications can be triggered with a single line of code.

## SnapKit
- https://github.com/SnapKit/SnapKit

SnapKit is a DSL to make Auto Layout easy on both iOS and OS X.
In fact, SnapKit is a successor of Masonry that happens to be written in Swift. The authors of the library recommend that if you are starting a Swift project go with SnapKit

Other [Masonry](https://github.com/SnapKit/Masonry)

## SwiftyJSON
- https://github.com/SwiftyJSON/SwiftyJSON

SwiftyJSON improves your life when it comes to handling JSON in Swift. Parsing JSON with Swift can be tricky due to type casting issues that make it difficult to deserialize model object, amd it may require a bunch of nested if statements. SwiftyJSON makes all of it quite simple to do. It’s also the second-most popular Swift library.

## MJRefresh
- https://github.com/CoderMJLee/MJRefresh

MJRefresh offers you an easy way to add pull-to-refresh functionality to a UITableView

## CocoaLumberjack: Logger
- https://github.com/CocoaLumberjack/CocoaLumberjack

CocoaLumberjack is a simple but powerful logging framework for all your logging needs. If you want to do more than NSLog or print, CocoaLumberjack can help. You can do remote logging, log to a local file, write to multiple loggers, and create different log levels. Ever had to reproduce an elusive bug, or needed to get a better grasp on some user behavior? CocoaLumberjack is very helpful in these cases.

## Realm: CoreData
- https://github.com/realm/realm-cocoa

Realm is an enticing, cross-platform alternative to Core Data when it comes to persistence. It’s easier to work with than Core Data, as well as faster, and you even get a data browser to explore Realm database files
- [Beginning Realm on iOS](https://www.raywenderlich.com/4146-beginning-realm-on-ios/lessons/1)
- [Intermediate Realm on iOS](https://www.raywenderlich.com/4200-intermediate-realm-on-ios/lessons/1)

## SwiftDate 
- https://github.com/malcommac/SwiftDate
Toolkit to parse, validate, manipulate, compare and display dates, time & timezones in Swift.

Other: [DateHelper](https://github.com/melvitax/DateHelper) - Convenience extension for NSDate in Swift.

## Alert & Action Sheet
- [SCLAlertView-Swift](https://github.com/vikmeup/SCLAlertView-Swift) - Beautiful animated Alert View, written in Swift.

# Widget
## Snackbar
- [Toast-Swift](https://github.com/scalessec/Toast-Swift)
- [BRYXBanner](https://github.com/bryx-inc/BRYXBanner)
- [GSMessages](https://github.com/wxxsw/GSMessages)
- [SwiftyDrop](https://github.com/morizotter/SwiftyDrop)
- [Toaster](https://github.com/devxoul/Toaster)
- [NotificationBanner](https://github.com/Daltron/NotificationBanner)

## Dialog
- [SwiftMessages](https://github.com/SwiftKickMobile/SwiftMessages)
- [CleanyModal](https://github.com/loryhuz/CleanyModal)
- [XLActionController](https://github.com/xmartlabs/XLActionController)
- [PMAlertController](https://github.com/pmusolino/PMAlertController)=

## Badge
- [MIBadgeButton-Swift](https://github.com/mustafaibrahim989/MIBadgeButton-Swift)
- [BadgeHub](https://github.com/jogendra/BadgeHub)]
