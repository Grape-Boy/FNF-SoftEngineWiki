NOTE: [Click here to see the list of Tween Eases.](https://api.haxeflixel.com/flixel/tweens/FlxEase.html)
# Tween Functions for Strum/Receptors
### noteTweenX(tag:String, note:Int, value:Dynamic, duration:Float, ease:String)
Do a tween on a receptor's X position
* `tag` - Once the tween is finished, it will do a callback of `onTweenCompleted(tag)`
* `note` - Opponent's notes are 0, 1, 2 and 3, respectively. Boyfriend's notes are 4, 5, 6, 7 respectively.
* `value` - Target value on the tween end
* `duration` - How much time it will take for the tween to end
* `ease` - The tweening method used, example: `linear`, `circInOut`. Check the link on the note in the first line of this page
### noteTweenY(tag:String, note:Int, value:Dynamic, duration:Float, ease:String)
Do a tween on a receptor's Y position

### noteTweenAngle(tag:String, note:Int, value:Dynamic, duration:Float, ease:String)
Do a tween on a receptor's Angle value

### noteTweenAlpha(tag:String, note:Int, value:Dynamic, duration:Float, ease:String)
Do a tween on a receptor's Alpha value

Works exactly like noteTweenX

# Starting Timer/Tween Functions
### doTweenX(tag:String, vars:String, value:Dynamic, duration:Float, ease:String)
Do a Tween on an object's X value
**Calling this function will cancel another tween that is using the same tag!**
* `tag` - Once the tween is finished, it will do a callback of `onTweenCompleted(tag)`
* `vars` - Variable to tween, example: `boyfriend` for tweening Boyfriend's X position, `boyfriend.scale` for tweening Boyfriend's Scale X
* `value` - Target value on the tween end
* `duration` - How much time it will take for the tween to end
* `ease` - The tweening method used, example: `linear`, `circInOut`. Check the link on the note i've added up here
Example: To do a tween to Boyfriend's Scale X, you should use `doTweenX('bfScaleTweenX', 'boyfriend.scale', 1.5, 1, 'elasticInOut')`, when the tween ends, it will do a callback for `onTweenCompleted('bfScaleTweenX')`
### doTweenY(tag:String, vars:String, value:Dynamic, duration:Float, ease:String)
Do a Tween on an object's Y value

Works exactly like doTweenX

### doTweenAngle(tag:String, vars:String, value:Dynamic, duration:Float, ease:String)
Do a Tween on an object's Angle value

Works exactly like doTweenX

### doTweenAlpha(tag:String, vars:String, value:Dynamic, duration:Float, ease:String)
Do a Tween on an object's Alpha value

Works exactly like doTweenX
### doTweenZoom(tag:String, vars:String, value:Dynamic, duration:Float, ease:String)
Do a Tween on a Camera's Zoom
Works exactly like doTweenX, but `vars` should be either: `camGame`, `camHUD` or `camOther`
### doTweenColor(tag:String, vars:String, targetColor:String, duration:Float, ease:String)
Do a Tween on an object's color
**Calling this function will cancel another tween that is using the same tag!**
* `tag` - Once the tween is finished, it will do a callback of `onTweenCompleted(tag)`
* `vars` - Variable to tween, example: `boyfriend` for tweening Boyfriend's X position, `boyfriend.scale` for tweening Boyfriend's Scale X
* `targetColor` - The color the object will have when the tween ends (Must be in hexadecimal!)
* `duration` - How much time it will take for the tween to end
* `ease` - The tweening method used, example: `linear`, `circInOut`. Check the link on the note i've added up here
Example: To tween Boyfriend's color to Red, you should use `doTweenColor('bfColorTween', 'boyfriend', 'FF0000', 1, 'linear')`, when the tween ends, it will do a callback for `onTweenCompleted('bfColorTween')`
### runTimer(tag:String, time:Float = 1, loops:Int = 1)
Runs a timer with a determined duration and loops count.
**Calling this function will cancel another timer that is using the same tag!**
* `tag` - Once the timer is finished, it will do a callback of `onTimerCompleted(tag, loops, loopsLeft)`
* `time` - Optional value, how much time it takes to finish a loop. Default value is `1`
* `loops` - Optional value, how much loops should it do, if it's set to 0, it will repeat indefinitely. Default value is `1`
_______________________
# Cancelling Timer/Tween Functions
### cancelTween(tag)
Cancels a tween using the tag `tag`, if there even is one.
_______________________
### cancelTimer(tag)
Cancels a timer using the tag `tag`, if there even is one.