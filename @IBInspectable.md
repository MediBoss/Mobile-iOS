# @IBInspectable

Adding @IBInspectable attribute to a property in your class will expose that property to the Attributes Inspector tab of Xcode. 
This will lead to a convenient way of modifying that property without having to type it manually in the user-defined runtime attributes section.

### Set up

The first step to do is to extend the UIView class and add a property(or many) with the @IBInspectable attribute.

```swift
extension UIView {

  @IBInspectable
  var cornerRadius: CGFloat {

     get {
     
        return layer.cornerRadius
     }
     
     set {
     
        layer.cornerRadius = newValue
     }
  }

}
```
When you select any UIView element on Storyboard and go to the inspector, you should see a settings for the cornerRadius



##### Source : https://spin.atomicobject.com/2017/07/18/swift-interface-builder/
