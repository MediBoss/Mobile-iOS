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


# @IBDesignable

Editing your views after setting up @IBInspectable does not render the changes in real time, only while the app is running. However, you can overcome this issue by adding the <b>@IBDesignable</b> attribute, which tells Xcode that it can render the control directly in Interface Builder.

``` swift
@IBDesignable
class DesignableView: UIView {
    
}

@IBDesignable
class DesignableButton: UIButton {
    
}

@IBDesignable
class DesignableLabel: UILabel {
    
}


```

The last step is to change the class of the view in the utility inspector from UIView/UIButton/UIButton to UIDesignableView/etc...
