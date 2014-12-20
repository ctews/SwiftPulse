# SwiftPulse

This is an iOS component for creating a single pulsing animation. It's a clone from [**PulsingHalo**](https://github.com/shu223/PulsingHalo) - so basically all the credits go to **@shu223**.

I just needed the single pulse animation (left one of the image) and decided to port it to Swift with some minor changes of the interfaces.

![PulsingHalo](https://camo.githubusercontent.com/ddec8ff304ce4e553636bec650c053eefc0069f1/687474703a2f2f662e636c2e6c792f6974656d732f3251305830353270326d3337316d3077324f30432f68616c6f6769662e676966)

## How to use

1. Add LFTPulseAnimation to your project.
2. Init LFTPulseAnimation (e.g. with its custom constructor) and add it to the view

```swift
pulseEffect = LFTPulseAnimation(repeatCount: Float.infinity, radius:20, position:imageView.center)
view.layer.insertSublayer(self.pulseEffect, below: imageView.layer)
```

# Customization

##radius
Use the radius property to set the max size of the pulse effect.

```swift
pulseEffect.radius = 60
```

##color
This is is basically a subclass of CALayer so you can access the _backgroundColor_ attribute of CALayer and set it like you are used to it.

##animation duration
Use ```self.animationDuration``` to set the duration of one animation cycle. Use the ```self.pulseInterval``` property to add an interval to the duration.

##animation repeat count
Initialize using ```LFTPulseAnimation(repeatCount: Float.infinity, radius:20, position:iv.center)``` to set the repeat count or use the ```repeatCount``` property

##more properties
For more adjustment just look in the code, it's very easy to understand and should be seld documenting.


## Issues & PRs
If someone is interested in porting the multiple pulse effect before I will do it just let me know or do a Pull Request ;)

### Additional Info
I used the [Async](https://github.com/duemunk/Async) library which adds sugar for GCD in Swift. So if you wonder about the ```Async.background``` it's just a wrapped GCD call. :)

# Special Thanks
Special thanks to @shu223 for [PulsingHalo](https://github.com/shu223/PulsingHalo)!


