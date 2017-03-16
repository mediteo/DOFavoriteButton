# DOFavoriteButton
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![Version](https://img.shields.io/cocoapods/v/DOFavoriteButton.svg?style=flat)](http://cocoapods.org/pods/DOFavoriteButton)
[![Platform](https://img.shields.io/cocoapods/p/DOFavoriteButton.svg?style=flat)](http://cocoapods.org/pods/DOFavoriteButton)
[![License](https://img.shields.io/cocoapods/l/DOFavoriteButton.svg?style=flat)](https://github.com/okmr-d/DOFavoriteButton/blob/master/LICENSE)

Cute Animated Button written in Swift.
It could be just right for favorite buttons!
![Demo](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/demo.gif)

## Requirements
* iOS 7.0+
* Swift 3.0

## Installation

#### CocoaPods
Add the following line to your `Podfile`:
```
pod 'DOFavoriteButton', :git => 'https://github.com/mediteo/DOFavoriteButton.git', :branch => 'swift3.0'
```

#### Manual
Just drag DOFavoriteButton.swift to your project.

## How to use
#### 1. Add a flat icon image
![Flat Icon Image](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/flatIconImage.png)

#### 2. Create a button
##### ・By coding
```swift
let starButton = DOFavoriteButton(frame: CGRect(x: x, y: y, width: 44, height: 44), image: UIImage(named: "star"))
self.view.addSubview(button)
```

##### ・By using Storyboard or XIB
1. Add Button object and set Custom Class `DOFavoriteButton`  
![via Storyboard](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/storyboard.png)

2. Connect Outlet  
![connect outlet](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/connect.png)

#### 3. Add tapped function
```swift
button.addTarget(self, action: #selector(ViewController.tapped(_:)), for: UIControlEvents.touchUpInside)
```
```swift
func tapped(sender: DOFavoriteButton) {
    if sender.isSelected {
        // deselect
        sender.deselect()
    } else {
        // select with animation
        sender.select()
    }
}
```

## Customize
You can change button color & animation duration:
```swift
button.imageColorOff = UIColor.brownColor()
button.imageColorOn = UIColor.redColor()
button.circleColor = UIColor.greenColor()
button.lineColor = UIColor.blueColor()
button.duration = 3.0 // default: 1.0
```
Result:  
![Customize](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/changeColor.gif)

## DEMO
There is a demo project added to this repository, so you can see how it works.

## Credit/Inspiration
DOFavoriteButton was inspired by [Twitter's iOS App](https://itunes.apple.com/us/app/twitter/id333903271).

## License
This software is released under the MIT License.
