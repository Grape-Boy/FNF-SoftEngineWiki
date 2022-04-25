# Character Functions
### characterPlayAnim(character:String, anim:String, forced:Bool = false)
* `character` - Can be `boyfriend`, `dad` or `gf`
* `anim` - Animation name to be played
* `forced` - Can be either `true` or `false`, if set to `true`, it will force the animation to reset if the current animation is the same as the animation to play

### characterDance(character:String)
Makes character do the idle dance
* `character` - Can be `boyfriend`, `dad` or `gf`

### getCharacterX(type:String)
Gets the general X position of a character from the type `type`
* `type` - Can be `boyfriend`, `dad` or `gf`

### setCharacterX(type:String)
Sets the general X position of a character from the type `type`, this will also move all precached characters from the same type into the position you want
* `type` - Can be `boyfriend`, `dad` or `gf`

### getCharacterY(type:String)
Gets the general Y position of a character from the type `type`
* `type` - Can be `boyfriend`, `dad` or `gf`

### setCharacterY(type:String)
Sets the general Y position of a character from the type `type`, this will also move all precached characters from the same type into the position you want
* `type` - Can be `boyfriend`, `dad` or `gf`
_______________________
# Score/Accuracy Functions
### addScore(value:Int = 0)
Adds `value` to the current song's score and recalculates rating

### setScore(value:Int = 0)
Set the current song's score to `value` and recalculates rating

### addMisses(value:Int = 0)
Adds `value` to the current song's misses total and recalculates rating

### setScore(value:Int = 0)
Set the current song's misses total to `value` and recalculates rating

### addHits(value:Int = 0)
Adds `value` to the current song's notes hit total and recalculates rating

### setHits(value:Int = 0)
Set the current song's notes hit total to `value` and recalculates rating

### setRatingPercent(value:Float)
Sets the rating percent in case you want to do your own rating calculation.
* `value` - Should go from `0` to `1` but can actually be whatever value you want, but it's kinda stupid to get out of the base values.

### setRatingString(value:String)
Sets the rating name to `value` in case you want to do your own rating calculation.
_______________________
# Key Press Functions
### keyJustPressed(name:String)
Get if the key `name` just got pressed on the current frame.

Keys: `'left'`, `'down'`, `'up'`, `'right'`, `'accept'`, `'back'`, `'pause'`, `'reset'`, `'space'`

### keyPressed(name:String)
Get if the key `name` is being held on the current frame.

Keys: `'left'`, `'down'`, `'up'`, `'right'`, `'space'`

### keyReleased(name:String)
Get if the key `name` was released on the current frame.

Keys: `'left'`, `'down'`, `'up'`, `'right'`, `'space'`
_______________________
# Mouse Click functions
### mouseClicked(name:String)
Get if the mouse button `name` just got pressed on the current frame. leave 'name' blank for left mouse

Buttons: `'left'`, `'right'`, `'middle'`

### mousePressed(name:String)
Get if the mouse button `name` is being held on the current frame.

Buttons: `'left'`, `'right'`, `'middle'`

### mouseReleased(name:String)
Get if the mouse button `name` was released on the current frame.

Buttons: `'left'`, `'right'`, `'middle'`
_______________________
# Mouse Position Functions
### getMouseX(camera:String)
Returns the relative mouse X position on a specific camera
* `camera` - Can be either `game`, `hud` or `other`

### getMouseY(camera:String)
Returns the relative mouse Y position on a specific camera
* `camera` - Can be either `game`, `hud` or `other`
_______________________
# Other Functions
### triggerEvent(name:String, arg1:String, arg2:String)
Triggers an event without you having to chart them.
* `name` - Event name on Chart Editor
* `arg1` - Value 1 on Chart Editor
* `arg2` - Value 2 on Chart Editor

### addLuaScript(path:String)
Loads another .lua script. 
* `path` - Path to LUA relative to the base folder

### getColorFromHex(color:String)
Get the color decimal ID from an Hexadecimal value (`color`).

Example: To get orange, you should use `getColorFromHex('FF7800')` or `getColorFromHex('0xFFFF7800')`

### getSongPosition()
Returns the current song position. Shortcut to `getPropertyClass('Conductor', 'songPosition')`
___
# Camera Functions
### cameraShake(camera:String, intensity:Float, duration:Float)
* `camera` - "game", "hud" or "other"
* `intensity` - How far away should it shake, recommended value is `0.05`
* `duration` - Time duration for it to shake

### cameraSetTarget(target:String)
Makes the camera focus on a specific target
* `target` - Target can be either `boyfriend` or `dad`


### cameraFlash(camera:String, color:String, duration:Float,forced:Bool)
* `camera` - "game", "hud" or "other"
* `color` - color of flash
* `duration` - Time duration for it to flash
* `forced` - restarts flash or not

### cameraFade(camera:String, color:String, duration:Float,forced:Bool)
* `camera` - "game", "hud" or "other"
* `color` - color of fade
* `duration` - Time duration for it to fade
* `forced` - restarts fade or not

____________________
# Debug Functions
### debugPrint(text1, text2, text3, text4, text5)
* Prints a debug message on the top-left corner of the screen

* All values are optional

* You can have up to 5 values to be printed.

Example: `debugPrint("Current boyfriend character: ", getProperty("boyfriend.curCharacter"));`

This will print the following message: `Current boyfriend character: bf`

### close(printMessage:Bool)
Stops your script in the next 100 miliseconds.
* `printMessage` - Wether you want a warning to show on the top-left corner of the screen or not