![DynamicColor](http://yannickloriot.com/resources/dynamiccolor-header.png)

[![Supported Plateforms](https://cocoapod-badges.herokuapp.com/p/DynamicColor/badge.svg)](http://cocoadocs.org/docsets/DynamicColor/) [![Version](https://cocoapod-badges.herokuapp.com/v/DynamicColor/badge.svg)](http://cocoadocs.org/docsets/DynamicColor/) [![Build Status](https://travis-ci.org/yannickl/DynamicColor.png?branch=master)](https://travis-ci.org/yannickl/DynamicColor)

DynamicColor provides powerfull methods to manipulate colors in an easy way.

<p align="center">
  <img src="http://yannickloriot.com/resources/dynamiccolor-sample-screenshot.png" alt="example screenshot" width="300" />
</p>

## Usage

#### Darken & Lighten

These two create a new color by adjusting the lightness of the receiver. You have to use a value between 0 and 1.

<p align="center">
  <img src="http://yannickloriot.com/resources/dynamiccolor-darkenlighten.png" alt="lighten and darken color" width="280"/>
</p>

```swift
   let originalColor = UIColor(hex: 0xc0392b)
   
   let lighterColor = originalColor.lighterColor()
   // equivalent to
   // lighterColor = originalColor.lightenColor(0.2)

   let darkerColor = originalColor.darkerColor()
   // equivalent to
   // darkerColor = originalColor.darkenColor(0.2)
```

#### Saturate, Desaturate & Grayscale

These will adjust the saturation of the color object, much like `darkenColor` and `lightenColor` adjusted the lightness. Again, you need to use a value between 0 and 1.

<p align="center">
  <img src="http://yannickloriot.com/resources/dynamiccolor-saturateddesaturatedgrayscale.png" alt="saturate, desaturate and grayscale color" width="373"/>
</p>

```swift
let originalColor = UIColor(hex: 0xc0392b)
   
let saturatedColor = originalColor.saturatedColor()
// equivalent to
// saturatedColor = originalColor.saturateColor(0.2)

let desaturatedColor = originalColor.desaturatedColor()
// equivalent to
// desaturatedColor = originalColor.desaturateColor(0.2)
   
let grayscaleColor = originalColor.grayscaledColor()
```

#### Adjust-hue & Complement

These adjust the hue value of the color in the same way like the others do. Again, it takes a value between 0 and 1 to update the value.

<p align="center">
  <img src="http://yannickloriot.com/resources/dynamiccolor-adjustedhuecomplement.png" alt="ajusted-hue and complement color" width="280"/>
</p>

```swift
let originalColor = UIColor(hex: 0xc0392b)
   
let adjustHueColor = originalColor.adjustedHueColor(45 / 360)

let complementColor = originalColor.complementColor()
````

#### Tint & Shade

A tint is the mixture of a color with white and a shade is the mixture of a color with black. Again, it takes a value between 0 and 1 to update the value.

<p align="center">
<img src="http://yannickloriot.com/resources/dynamiccolor-tintshade.png" alt="tint and shade color" width="280"/>
</p>

```swift
let originalColor = UIColor(hex: 0xc0392b)

let tintColor = originalColor.tintColor()
// equivalent to
// tintColor = originalColor.tintColor(amount: 0.2)

let shadeColor = originalColor.shadeColor()
// equivalent to
// shadeColor = originalColor.shadeColor(amount: 0.2)
```

#### Invert

This can invert the color object. The red, green, and blue values are inverted, while the opacity is left alone.

<p align="center">
  <img src="http://yannickloriot.com/resources/dynamiccolor-invert.png" alt="invert color" width="187"/>
</p>

```swift
let originalColor = UIColor(hex: 0xc0392b)
   
let invertColor = originalColor.invertColor()
```

#### Mix

This can mix a given color with the receiver. It takes the average of each of the RGB components, optionally weighted by the given percentage (value between 0 and 1).

<p align="center">
<img src="http://yannickloriot.com/resources/dynamiccolor-mix.png" alt="mix color" width="187"/>
</p>

```swift
let originalColor = UIColor(hex: 0xc0392b)

let mixColor = originalColor.mixColor(UIColor.blueColor())
// equivalent to
// mixColor = originalColor.mixColor(UIColor.blueColor(), weight: 0.5)
```

To go further, take a look at the example project. 

## Installation

#### CocoaPods

Install CocoaPods if not already available:

``` bash
$ [sudo] gem install cocoapods
$ pod setup
```
Go to the directory of your Xcode project, and Create and Edit your Podfile and add _DynamicColor_:

``` bash
$ cd /path/to/MyProject
$ touch Podfile
$ edit Podfile
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'

use_frameworks!
pod 'DynamicColor', '~> 1.0.0'
```

Install into your project:

``` bash
$ pod install
```

Open your project in Xcode from the .xcworkspace file (not the usual project file):

``` bash
$ open MyProject.xcworkspace
```

You can now `import DynamicColor` framework into your files.

#### Manually

[Download](https://github.com/YannickL/DynamicColor/archive/master.zip) the project and copy the `DynamicColor` folder into your project to use it in.
    
## Contact

Yannick Loriot
 - [https://twitter.com/yannickloriot](https://twitter.com/yannickloriot)
 - [contact@yannickloriot.com](mailto:contact@yannickloriot.com)


## License (MIT)

Copyright (c) 2015-present - Yannick Loriot

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
