# init-swift

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
 
