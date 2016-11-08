 ![Logo](https://roycms.github.io/AlertView/RAlert/logo.png)
 RAlertView
===
AlertView A pop-up framework, Can be simple and convenient to join your project.

[![Shippable](https://img.shields.io/shippable/5444c5ecb904a4b21567b0ff.svg?maxAge=2592000?style=flat-square)](https://github.com/roycms/RAlertView)
[![CocoaPods](https://img.shields.io/badge/pod-0.0.1-red.svg)](http://cocoapods.org/?q=RAlertView)
[![Packagist](https://img.shields.io/packagist/l/doctrine/orm.svg?maxAge=2592000?style=flat-square)](https://github.com/roycms/RAlertView/blob/master/LICENSE)
[![email](https://img.shields.io/badge/%20email%20-%20roycms%40qq.com%20-yellowgreen.svg)](mailto:roycms@qq.com)
[![doc](https://img.shields.io/badge/%E4%B8%AD%E6%96%87-DOC-orange.svg)](https://github.com/roycms/RAlertView/blob/master/README-CN.md)

## Warning content
 ![Warning content](https://roycms.github.io/AlertView/RAlert/RAlert.gif)

## Installation
- Depend on the project ` Masonry `and ` HexColors ` Import  `#import "Masonry.h"` `#import "HexColors.h"`
- Import the main header file：`#import "RAlertView.h"`

## cocoapods 
`  pod 'AlertView' `

## Preview  AlertStyle
```objective-c
typedef NS_ENUM(NSInteger,AlertStyle) {
    SimpleAlert = 0,
    ConfirmAlert,
    CancelAndConfirmAlert,
};
```
![RAlertView Preview](https://roycms.github.io/AlertView/RAlert/AlertStyle.jpg)
## Preview  AlertTheme
```objective-c
typedef NS_ENUM(NSInteger,AlertTheme) {
    YellowAlert = 0,
    GreenAlert,
    BlueAlert,
    Purple1Alert,
    Purple2Alert,
};
```
![RAlertView Preview](https://roycms.github.io/AlertView/RAlert/Theme.jpg)

## Some feature set
* Click on the background and any position hidden pop-up window
```objective-c
alert.isClickBackgroundCloseWindow = YES;
```
* Set bounced content text center
```objective-c
[alert setContentText:@"is ContentText" isAlignmentCenter:YES];
```

## init RAlertView
* initWithStyle AlertStyle
```objective-c
RAlertView *alert = [[RAlertView alloc] initWithStyle:SimpleAlert];
```
* initWithStyle AlertStyle and width
```objective-c
RAlertView *alert = [[RAlertView alloc] initWithStyle:SimpleAlert width:0.8];
```
## SimpleAlert
```objective-c
RAlertView *alert = [[RAlertView alloc] initWithStyle:SimpleAlert];
alert.contentText = @"SimpleAlert \nAlertView A pop-up framework, Can be simple and convenient to join your project";
```
## ConfirmAlert
```objective-c
RAlertView *alert = [[RAlertView alloc] initWithStyle:ConfirmAlert];
alert.theme = Purple1Alert;
alert.headerTitle = @"ConfirmAlert";
alert.contentText = @"AlertView A pop-up framework, Can be simple and convenient to join your project";
alert.confirmButtonText = @"Ok";
alert.confirmButtonBlock = ^(){
    NSLog(@"Click on the Ok");
};
```
## CancelAndConfirmAlert
```objective-c
RAlertView *alert = [[RAlertView alloc] initWithStyle:CancelAndConfirmAlert];
alert.headerTitle = @"CancelAndConfirmAlert";
alert.contentText = @"AlertView A pop-up framework, Can be simple and convenient to join your project";
alert.confirmButtonText = @"Ok";
alert.cancelButtonText = @"Cancel";
alert.confirmButtonBlock = ^(){
    NSLog(@"Click on the Ok");
};
alert.cancelWindowBlock = ^(){
    NSLog(@"Click on the Cancel");
};
```
## 期待
* 如果在使用过程中遇到BUG，希望你能Issues我，谢谢（或者尝试下载最新的框架代码看看BUG修复没有）
* 如果在使用过程中发现功能不够用，希望你能Issues我，我非常想为这个框架增加更多好用的功能，谢谢
* 如果你想为RAlertView输出代码，请拼命Pull Requests我

排版规范参考 https://github.com/sparanoid/chinese-copywriting-guidelines
