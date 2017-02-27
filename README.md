# OverlayController-Swift
![image](https://camo.githubusercontent.com/f5590872a42f5a6af60f42caf56620d05bdb917b/68747470733a2f2f7472617669732d63692e6f72672f736265727265766f6574732f534443416c657274566965772e7376673f6272616e63683d6d6173746572)
  
 This OverlayController is  Convenient to make an overlay. Written in Swift 3.0 !  
 
 Objective-C  version : SnailQuickMaskPopups

## Installation
Available in [CocoaPods](https://cocoapods.org "CocoaPods" )
    
        pod 'OverlayController', '~> 0.0.1'
    
## Usage scenario 
![image](https://github.com/snail-z/OverlayController-Swift/blob/master/Sample/alert%20style.gif)
![image](https://github.com/snail-z/OverlayController-Swift/blob/master/Sample/shared%20style.gif)
![image](https://github.com/snail-z/OverlayController-Swift/blob/master/Sample/qzone%20style.gif)

![image](https://github.com/snail-z/OverlayController-Swift/blob/master/Sample/sidebar%20style.gif)
![image](https://github.com/snail-z/OverlayController-Swift/blob/master/Sample/sina%20style.gif)
 
## Example
``` swift

    var overlayController : OverlayController!
    
    overlayController = OverlayController(aView: customView, overlayStyle: .BlackTranslucent)
    overlayController.present(animated: true)
    
 ```
 *  Properties
``` swift

    open var presentationStyle: PresentationStyle = .Centered
    open var transitionStyle: TransitionStyle = .CrossDissolve
    open var overlayAlpha: CGFloat = 0.5
    open var animateDuration: TimeInterval = 0.25
    open var isAllowOverlayTouch = true
    open var isAllowDrag   = false
    
    /**
     The view disappear in the opposite direction.
     - set default value is false!
     */
    open var isDismissedOppositeDirection = false
    
 ```
 *  Closures
``` objc
    /**
     presentExtra
     
     - parameter willPresent: WillPresent block to be executed before the view is presented.
     - parameter completions: Completion block to be executed after the view is presented.
     */
    overlayController.presentExtra(animated: true, willPresent: { (overlayController: OverlayController) in
        // code...
    }) { (finished: Bool, overlayController: OverlayController) in
        // code...
    }
    
    /**
     dismissExtra
     
     - parameter willDismiss: WillDismiss block to be executed before the view is dismissed.
     - parameter completions: Completion block to be executed after the view is dismissed.
     */
    overlayController.dismissExtra(animated: true, willDismiss: { (overlayController: OverlayController) in
        // code...
    }) { (finished: Bool, overlayController: OverlayController) in
        // code...
    }
    
 ```
 
