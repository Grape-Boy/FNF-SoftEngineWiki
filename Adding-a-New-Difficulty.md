***For adding a new Difficulty, you can either use the Source Code or a pre-built version of Psych/Soft Engine***

*On this Example, we will be adding a new difficulty called "Crazy", all charts for this difficulty should end with "-crazy".*

# Files needed
You will need the difficulty image for the Story mode menu, and you're also gonna have to do the Crazy difficulty chart to all songs.
Here's my Crazy difficulty image for an example:

![](https://i.imgur.com/mvaseyY.png)

# Using a Pre-Built Version
Inside of your `mods` folder's `images` folder or in your mod's `images` folder, create a new folder named `menudifficulties`.

Now, place your difficulty's image file inside of it.

After that, launch the game and go to the `Week Editor` by pressing `8` in the `Main Menu`. Load the `week` you want to add your new difficulty to and click the `Other` tab in the frame at the bottom right.

It should look like this:

![bandicam 2022-04-25 20-11-38-654](https://user-images.githubusercontent.com/96194070/165149278-dfc3985b-8756-4c62-9f69-c9d7a7cece20.jpg)

## Adding the Difficulty
Next, in the `Difficulties:` text input, write "`Easy, Normal, Hard, Crazy`" without the quotes (and with your difficulty's name replacing `Crazy` if it doesn't have the same name)

![bandicam 2022-04-25 20-11-59-255](https://user-images.githubusercontent.com/96194070/165151182-8a079f13-97ab-4c94-9233-7c78d3082ce6.jpg)

## One or More Difficulties
You can also make your week have a different amount of difficulties by writing only the names of the difficulties you want the week to have:

![bandicam 2022-04-25 20-18-51-410](https://user-images.githubusercontent.com/96194070/165151612-4eac9674-1203-438b-98ba-a6873cb82665.jpg)

# Using Source

This is probably the easiest part.
Our difficulty will be called `Crazy`.
Open CoolUtil.hx inside `source/`, at `line 19`, you will see this array:

![bandicam 2022-04-25 16-05-21-712](https://user-images.githubusercontent.com/96194070/165108736-2ea1de0c-a317-4af7-b59b-a6631f044fa0.jpg)

So... add your new difficulty to it, like this.

![bandicam 2022-04-25 16-06-19-748](https://user-images.githubusercontent.com/96194070/165108969-672c91ab-ed1a-4ea6-95e1-15cd4da10d44.jpg)

Put the image inside `assets/preload/images/menudifficulties/` with it being named `crazy.png` and we're ready to go, now compile! If you've done everything alright, it should be in and working properly!

# The Finished Product
When you're finally done adding your new difficulty, it should look like this:

![](https://i.imgur.com/MDzP1PF.png)
![](https://i.imgur.com/qHY7beU.png)

# Enjoy the Extra Difficulty!

I made a Bopeebo chart with Crazy difficulty to test it out:

* [githubusercontent link](https://raw.githubusercontent.com/Grape-Boy/FNF-SoftEngine/main/docs/bopeebo-crazy.json)

* [pastebin link](https://pastebin.com/BeAP4q73)