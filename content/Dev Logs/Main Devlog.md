---
title: Main Devlog
---
# Week 14
## April 14/15, 2026
### Week 14 Progress Report
#### Week 14 Goals
- Static Assets
- Video Assets
- In Game Sound
- Tweak Game Stuff to Make Feel Better
	- Make sure current puzzles work
I got a good amount of stuff done, my game is feeling almost there, minus a few things, mainly rewrite on script and some on screen indicators for learning controls in the beginning, though I think those things will be fairly straightforwards. I'm going to try and get those done tomorrow when this is due. I want to get a build out to people this weekend to make sure things are good. I've got a few people who want to play it which is good, as well as some people who have not played it yet, which will be interesting to see about. I felt alright on how much time I spent working this week, but with how much other stuff I have to do it also feels like I spent a lot of time on those things and not on this but realistically I think I'm still in a good spot. I'm like maybe a bit worried about the website since my brain doesn't work well with html and css, but I think it'll be all good. I think the setup I have right now will be simple enough to get things on the page and looking good. I've been playing pretty much all of the puzzles to test things out, so I know they all work which is good, it's just if there's things about the puzzles that are weird and people can't figure out. People have also played these puzzles before though, so I don't think it will be too much of an issue.
### Game Build
I tried building the game and playin through it a bit just to make sure all the systems work, and everything's looking good. I still want to add a few more things, but I think it's looking good for being able to export. 
### Website Instantiation
I've got a rough website outline create based on n-o-d-e.net. It's fairly basic, but I think it fits the cyberpunk aesthetic I'm going for. I want to get more into cool website making, but I don't think this is the project to get very into it. It's simple, but I think it will be good for having things put together and looking decent for documentation. 
### Static/Video Assets
Static images are good for the website, maybe for the video in how I have it planned out. I think the video below will be a good replacement intro for the start of the video. Waking up, then going over to the terminal, where most of the video will take place. I might rerecord though, depending on how I will do the rest of the video. I might need to actually just straight up record the whole thing in the terminal and have a separate script, but well see.
![[Screen Recording 2026-04-15 182434.mov]]
![[Screenshot_2026-04-15_150117.png]]
![[Screenshot_2026-04-15_150441.png]]![[Screenshot_2026-04-15_173452.png]]![[Screenshot_2026-04-15_174124.png]]![[Screenshot_2026-04-15_183649.png]]
### On Screen Indications
I want to add indicators on screen for the first puzzle to try and get people used to the controls. I'm thinking just a few guided icons on screen of the joy sticks pointed in certain directions that the player has to match. I'm doing this mostly because players usually don't know how to do the joysticks in opposite direction. They get how to point the joysticks in one direction of course, but the opposite directions to make the puzzles roll is a bit of a new concept, though once they know how to do it, it's generally used.
### Screen Shake
I've got a screen shake for the camera that I can activate from a global. It really only need to be accessed from one script, but it's a global that's actually set up correctly, so it's only capable of adding "trauma" to the screen shake. The other globals I have set up are fine, but this one uses signals, so I'd say it's a bit more safe and correct in its setup.
### Sound
I've edited and added a lot of sounds. There's probably still some more, but I want to go through everything first and see if there are empty feeling points of sound. Had a problem where no sounds would play when the game restarted, but that was just a thing I had where I was muting the audio bus for everything, which took way too long to find. 
### Particles
I adde some particles to when the player starts the puzzle, as well as a sound, so it now looks like the black hole device is starting up. I may also make it spark a bit more with the unstableness of the device too, especially on the last one.
## April 13, 2026
### Sound Stuff
I've got the ambient start screen sound in, a kinda low, deep sound that loops. I also have a global script that has a function that fades the sound out when the game is started. It can also fade out any other AudioStreamPlayer in the game as well, with customizable time.
## April 12, 2026
### WHAT STILL NEEDS TO BE DONE
#### Juice (Audio/Visuals)
Game is very quiet right now, besides the sounds from the movers on the puzzles and the dialogue. Sounded fine before that, but now there's some sounds, everything else is so quiet. Other things feel static as well, specifically the camera/terminal. With the chamber falling apart, could definitely get some screen shake in there. Chris also mentioned having more connection of the black hole device to the puzzles, so I think there's room for juice there.
##### Audio
- Global script to control fading for sounds????
- Start screen ambient sounds
- Test chamber ambient sounds
	- Fluorescent lights
	- Pipe sounds?
	- Terminal Sounds
- Terminal boot up and boot down sounds
- Shutter opening
- Black hole device power up sounds 
	- Probably around the time of the shutter opening
- Chamber falling apart
	- Probably can happen after doing terminal visit
	- Also for when the chamber falls apart with animation at end
- Sounds for puzzle mechanics
	- Portal
	- Gate
##### Visual
- Screen shake
	- Probably can be function on camera that global script controls
- Visual power up of device?
	- Possibly some kind of shader effect at bottom of screen with sound mentioned above
- 2D puzzle nodes floatiness
- Some kind of flashing carrot for the dialogue on the terminal screen.
#### Dialogue
Please rewrite the script. It can be better. And now you don't even have to worry about rerecording stuff. So there's no excuse....... I think tutorial for portals might be done through this. I didn't really want to, but they're very abstract in having to get the ball in them, then line them up visually; I think that's going to be very hard to communicate visually. While I don't think it's impossible I'm not sure I have to time to get that down.
#### Puzzles
Tweak em. Make sure they work. They do work, but def wanna make sure they feel good.
### Dialogue Speech
I've been saying I'm going to record voiceover for the dialogue, but at this point it's really not something that deserves that much time. I want the speech to add to the surrealism and creepiness of everything, but recording, editing, making sure a bunch of dialogue audio is too much time that could be spent on other things. When researching, I found an add-on that does kind of Animal Crossing speech, not just that style but more about the sounds that correlate to the text. I implemented it with the dialogue system I wrote and it works great, even simplifies some of the code I had written. The add-on even controls how the text is revealed on screen, which is a bit better than the one I had I think. It plays audio files dependent on the letters of words so it even sounds like a voice but kinda not. I also made it have a randomized pitch, so it's a robotic, almost real sounding voice, which I think still serves the purpose I wanted without the large time that it would've taken to record all the voice and make sure it fit. Even though this deprecates a system I had made, I'm very happy with this switch. It works very well and does what I need it to. It's not a vital component of the game, so I don't need that fine grain control of a hand made system, but it's also written in the same language the game is written in, so it's still very easy to manipulate when I need it to. The only change that I still need to make is edit all the JSON files, which is literally just removing things from it, they don't even need to be structured differently. Just turning the array of arrays with objects into an array of strings. Great simplification with great results.
## April 11, 2026
### Da Website
Made a repo for the website. Not much else tbh. Was going to start more on it, but def needs more design first. I think I'm going to use colors from the color palette I use for the game's dither shader, but the palette itself is actually kinda big, since it has multiple shades for each color.
## April 10, 2026
### Week 14 Goals
- Static Assets
- Video Assets
- In Game Sound
- Tweak Game Stuff to Make Feel Better
	- Make sure current puzzles work
# Week 13
## April 8, 2026
### Week 13 Progress Report
#### Week 13 Goals
- Storyboard Video
- Draft Video Script
- Audio/Visual Effects that need to be added
- Planning on how I want website to look

Do think I took a bit of a break from capstone stuff, but still got a decent amount done. Thought this shader was gonna take longer which is nice I have it done now, I pretty much just have to do sound stuff now. Wish I had some more visual idea for my site, but I don't see too many issues with figuring that out. I have some good visual style to go off of from the game, so I think it'll be good.
### Shaderssss(Finally)
I took the mask I had showcased in my presentation the other day and added on the light distortion shader. I got the shader off of godotshaders.com but modified it a good amount to work with this mask I made, that I also modified a bit to make it elliptical. It doesn't currently intensify yet, but the different parameters on it are exposed, so I can just change it with the state machine.
![[20260409-0524-24.1091549.mp4]]
### Website Prelim
#### Pages(Names Subject to Change)
##### Game/In-Game
Talks about what the game is in the way it exists when someone plays it. What do you do in it, what does it look like, how does it play, etc. Most of the classic stuff you would find on a page for a game, be it Steam or itch.io. I see this being the main page, since it works for both people who are interested in the game and my work on the project. Other pages feel more specialized towards people who are interested in the project as a whole rather than jus the game. Also just showing the game presents a good base for looking at the other pages; feels good to say first here's what I did and then having that context people can choose to see how and why I did it.

Download for game here?!?!?!?!?!?!? Don't know if Github Pages allows that or if there's security issues. Frankly, I just don't want to also make a itch.io page right now. But maybe...... I will have assets for it.....
##### "Meta" Game
This is stuff like design philosophy, why did I make the choices I made, actually explicitly talk about what's in my elevator pitch, etc. This could probably also include some stuff about technical aspects, but that'll probably fit better in process. I have more personal connection to the reason I made the game so I think it's good to talk about here. I also want to talk about the mindset I chose in designing and developing the game, such as subtractive game design or how I designed systems. Stuff like that applies to the whole process, so I think it'd be good to include it separately. Putting it before Process could be good since it just gives a bit more context to those steps; I don't have to explain ever time that I make a system why I chose for it to be component based, I can just say here that I utilized Godot's Node and Resource system to make component based systems and then that applies to all the times I made those systems and changed them.
##### Process
This is talking about the iterations of the projects. There's of course the technical parts that changed over time, but also the design of the game and how that changes, which also kind of ties into the previous page I talked about. I think process would be good to talk about the whole game at each iterative step, instead of separating out each aspect of the game(ex. audio, controls, gameplay) and doing iterations for each of those. I don't think there's any one aspect of the game that deserves its own iterative process and it just makes more sense for me working on it solo. Everything was worked on in tandem, so not separating aspects also matches what my actual process looked like.
##### Creator
Short page about me. Not really worth talking about what I did on the project in too much detail since that's pretty much just the whole website. This could be altered to a more general info page on other things about the project, since I also want to include credits for some of the aspects of the code I used from other people; pretty much most of the overlay shader code. I need to check the licenses for the code; I know I am allowed to use them, but I also think that the code I used also might be technically usable without crediting, but either way I still want to include that.
## April 7, 2026
### Storyboard
![[IMG_2107.jpg]]
![[IMG_2108.jpg]]
## April 2, 2026
### Week 13 Goals
- Storyboard Video
- Draft Video Script
- Audio/Visual Effects that need to be added
- Planning on how I want website to look
# Week 12
## April 1, 2026
### Week 12 Progress Report
#### Week 10/11 Goals
- Testing at all steps
- Full controller implementation
	- Big thing here is the 2D stuff with controller. I've got a good idea of how the puzzles will work in 2D after talking with some people on what they think would make this very mouse heavy system work with a controller
- Finish Up 3D and 2D Assets
- Dialogue system setups; would love to finish this if I have the time
	- Probably JSON based
	- Doesn't need to be too complicated; it's just one way text to player with TTS
- Write dialogue for 2D stuff
- Get sounds mostly implemented
- Make transition between states more fluid
	- Right now starting and finishing puzzles is very sudden
- Planning out juice and other Audio/Visual elements I want to add in to help match this world and environment to the narrative beats I have formed.
	- Also really want to get a good amount done on this, but lower on priority list

Happy with the work I got done this week, even though I had to spend a lot of the first part of it on another paper. Spent a lot of my waking hours during the week working on this, and though I wish I had been able to spread it out more, it was still good work done. Everything's pretty much at the point of being done, except for juice and audio stuff. Think I can make things feel better overall, but it's all at a good point currently.
### Major Bug Fix
There was a major bug I've had forever that made it so the movers on the paths could combine. I have spent so long looking at that bug. It was a less than sign that needed to be a greater than sign. Something I thought I'd changed many a time..... But it's fixed!
### 3D Modelin Finishes
I remodeled the terminal to fit in the room a bit better and make it a bit less blocky to add a bit more organic shape to the test chamber, but can't have too much, cause then it'll be too human! I also added a door to the chamber since I wanted to make the player feel like there's an escape, even though there isn't...
![[Screenshot 2026-04-02 at 9.11.08 AM.png]]
### Camera Lock
I got the camera to lock to a specific location when doing the 3D puzzles. I used an addon for Godot called Phantom Camera. I've used it in the past for 2D games, but it also has great applications in 3D. It's great for making a really juicy camera, but it's also great for interpolating positions for camera, which is just what I needed to make a locking camera that also returns to the player after they finish the 3D puzzles.
## March 30, 2026
### Implementing Game End
I have the 3 different "Stages" of the chamber falling apart in the engine now. The last two stages are technically the same, but the last one has an animation player for the falling apart animations. When the player starts the last puzzle, the puzzle begins to morph, which I turned up the intensity of since I don't need it to be solvable. After about 15 seconds, the animations of the chamber start to play, and when the last part of the animation plays, a piece of rubble flying at the player, the game goes black and after a few seconds returns to the start screen. There's some glitching in the geometry but that's just from me testing the final part of the chamber falling apart. The logic for when the chamber geometry switches just follows the state machine that controls when and what puzzles are loaded.
![[Screen Recording 2026-04-01 at 10.41.54 AM-1.mov]]
### Game End
So now that I have the test chamber falling apart, it game me a solid idea for how to end the game. I was already planning to end the game on the final 3D puzzle, but I wasn't quite sure how to end it, but I think this falling apart will work well for it. These parts of the chamber are cut out in Blender are now separate objects meaning they can actually move around. Since the whole anxiety part of the game is the black hole in the player's chest growing as the game progresses, I was going to have some black hole light bending shaders around the players screen, but I think to actually end the game I'm going to make the last 3D puzzle kind of a bit more of a cinematic thing, where the player can move around the morphing puzzle but it's more of just a false control, as the puzzle begins to more and then eventually the shader gets more intense and the parts of the chamber falling apart start to maybe float and then get thrown at the player, leading the screen to black. Maybe not as ambiguous as I originally wanted, but I think it still can be. I will also mention that the last puzzle is currently not solvable because of bugs and I promise that this is not a way for me to not fix the bugs. I did already want the last puzzle to not be solvable, but I think that this just works well enough to end the game and it happens to coincide with a bug that already makes the last puzzle not finishable, the bug being the portals not working when the puzzle is morphing.
### Breaking Apart Chamber
I'm breaking apart the test chamber currently in Blender. I've pretty much copied what I had before and am just cutting out part of the walks and rotating them away from their positions to look like the structure is falling apart. I think there's only going to be two stages of the test chamber, one where it's not falling apart and one where it is. woahhhhhhh so much variation. Anyways, I think it also gave me a solid idea for how to end the game.
### Sound Stuff
Made the sound for the balls moving on the tracks. I recorded a few takes of me sharpening a kitchen knife on a whetstone and then edited it to loop and mixed some of the background noise out so it could fit better in the game. I made it so that the pitch of the noise shifts as the speed of the mover changes to make it feel better. I also happened to fix a bug during this too, which caused the movers to quickly loose speed if the path they are on switches direction, which I don't want to happen. I didn't really notice it before, but hearing the sound stop quickly made me notice it a lot, but it was a pretty easy fix of using absolute value of speed. This took me way to long to do and frankly it's not even where I want it to be yet which sucks.
### Start Screen
I rendered out an animation of a black hole for the start screen. It's the same black hole in Blender I use in the 2D part of the game, but I changed the color, made it a bit higher fidelity, and added some stars in the background to make it more spacey.
## March 25, 2026
### Week 12 Goals
- Actually finish 3D assets
	- Test chamber falling
		- Get it to switch out those assets as the game progresses
	- Need to finish some stuff in the room the player is in; modeling and texturing
		- Texturing will probably just be with noise textures again
- Sound 
	- Recorded voice stuff
	- Environmental Sounds
- Start screen
	- Don't think I'm going to do saves for such a short game so it'll just be a place in between opening the game and playing
- Various bug fixes
- Juice
# Week 10/11
## March 24, 2026
### Week 10/11 Progress Report
#### Week 10/11 Goals
- Testing at all steps
- Full controller implementation
	- Big thing here is the 2D stuff with controller. I've got a good idea of how the puzzles will work in 2D after talking with some people on what they think would make this very mouse heavy system work with a controller
- Finish Up 3D and 2D Assets
- Dialogue system setups; would love to finish this if I have the time
	- Probably JSON based
	- Doesn't need to be too complicated; it's just one way text to player with TTS
- Write dialogue for 2D stuff
- Get sounds mostly implemented
- Make transition between states more fluid
	- Right now starting and finishing puzzles is very sudden
- Planning out juice and other Audio/Visual elements I want to add in to help match this world and environment to the narrative beats I have formed.
	- Also really want to get a good amount done on this, but lower on priority list

I was a bit worried over break about how much I had, but I got a good amount of things done, namely the dialogue system and controller stuff. I do wish there was a bit more done, but I'm still happy with what I have. I've still got a good amount left to do, but I still see a path for everything which is great. I do wish I had managed my time better, but break was a bit rough for that. Been spending a lot of time doing work out of the house and I think I better get back to doing work from home these next few weeks to make sure I can get the things I need to get done. Got some good feedback on everything as I worked on things; I made sure visuals, controls, and dialogue all worked with people as I worked on them. I think I expected dialogue to be a bit more rough to do, but I'd say it was one of my more smooth sailing things. The animation stuff was strangely annoying for how simple it was, but I did kind of expect it to be weird since importing Blender to Godot is already strange.
### Visual Works
I worked on making the test chamber look a bit better. The textures of the chamber are pretty flat right now with just flat colors and other values to determine if the materials are rough or metallic. I added some noise textures to the normal map channel of the wall materials, which is similar to what I did with the floor. I wanted the walls to not have the same look as the floor, so I structured the noise to look almost like brushed concrete. It took a bit to hone in the look of it to make sure it wasn't too busy on the screen, but I got it to a good point where it makes things a bit more interesting but not something you focus on a whole lot. I also added some noise textures to some of the more metal components of the shutter and button to make them look a bit more interesting. Adding this noise works well with the shader and the lighting I have going; definitely a good move without having to add too much actual detail in textures.
### Transition States
I don't think the transition state of the terminal has to be too much, probably will just do a fade in and out on the camera. For the 3D puzzles I animated the shutter as well as the button to make things feel better since I've just had the visibility turn on and off so far. It was my first time bringing animation from Blender to Godot, and I don't think I did it the best way, but since they are just simple position and scale animations, how I have them implemented works for their purpose.
## March 24, 2026
### Black Hole Shader for 2D
Made a lil black hole shader to make a gif of to put in the 2D view. I still need to render it out but I'm working on my laptop currently and don't want to spend the time to render a full gif out to try in the 2D view rn. Dis what the still looks like in it.
![[Screenshot 2026-03-24 at 12.09.50 PM.png]] Going to render it fully out later.
## March 19, 2026
On a plane rn, can't really take up the space I usually do with my controller and note pad and stuff, so I'm working on the 3D models in the test chamber. Original sketches, I had a bed and a terminal as the main objects in the room. I had made a terminal, but I think I'm going to redo it since it was made very quickly and also has some messed up geometry that is visible in engine. I had made a bed for original test renders of the project, but it's definitely too big, and I also think that it had far too much geometry to be in the game. Still this new bed will probably have the most geometry in the game, since for some reason I wanted to do a cloth sim(it's easier than modeling it, that's why). I won't be able to walk around in the scene to feel everything since I don't wanna pull my controller out of my bag in this cramped space, but thing's should at least be correct proportionally, so placement and scale should be the only things I really need to move. I'll probably also look into doing the shutter for the test chamber as well. I've never done animation in Godot so that'll be fun. I think I should just be able to animate in Blender, which I do know how to do, then import into Godot, but I definitely need to look into that workflow.
## March 17, 2026
### Tutorialization Side Note From Today
While writing that first draft, I was thinking about tutorializing the portals. I don't really want to do it through the dialogue, since it's supposed to be an unintended effect of the black hole. Means there needs to be more visual stuff. So how can I make it visually known that you put a ball in one side and then you have to line them up and come out the other side???? IDK. Maybe I make there be an effect that's like something winding up the closer you get the portals visually. They already kind of look like the solve points so I think players might put the balls in them, but we shall see.
### Audio Visual Stuff I Want To Add(Not Current Priority)
- Shader around player screen to mimic light distortion of black whole
	- Probably some particles as well to play with that distortion
	- I would like this to get more intense over time, but not enough to really mess with the player a whole lot
- Test Chamber breaking apart as player progresses
	- Probably mostly breaking up the mesh of the test chamber, maybe like wires hanging from the ceiling. Particles and stuff for sparking
	- Think I can just make things fall apart when the player is in the 2D terminal/when the shutters are closed
- Making the 2D puzzle nodes kinda float around in space. Not too much, just giving them some kinda life
- Black hole visualization in the terminal view
	- Was going to make a gif of a stylized black hole in Blender and put it below the logo in the terminal screen.
- Was thinking of making a small window at the top of the room that the player is in that has lights coming through it.
	- Nothing much but I don't want to focus on it if there's other stuff.
	- Would just be a rectangular cutout that's just an emissive texture, but I want light to "come through" the window and look like it's refracting off of fog or dust or something in the room.
## March 16, 2026
### Dialogue Script - First Draft
#### Tutorial State
Hello there! We are so happy of your acquisition to the Mattel-Toyota-Lockheed Martin family!

As part of the MTL family, you will be contributing to only the forefront of advancement of the human condition!

You have been requisitioned to the [Funny Name] Memorial Research & Development Department.

You will be participating in the testing of an exciting new technology. A black hole powered gravity manipulation device!

In testing today, you will use this device's rotation capabilities to solve a series of puzzles.

The puzzles are constructed out of a set of tracks that have a set of spheres that can freely move along them.

You will rotate these puzzles in 3D space to guide the spheres into certain boxes on the puzzle. The box the sphere goes in does not matter.

We will begin with a calibration test. This will be to make sure the device is working correctly and you are able to use it properly.

This first test will be comprised of a single sphere along a twisting, but non branching track.

The device gets quantum entangled when used, so we'll need you to return to the terminal after each test puzzle to reset the device.

You've already done a bit of untangling right after you opened this terminal, so we're sure you'll be great at it!

Now let's get to work! We'll catch up after you visit the terminal next!
#### State 1
Wow! You're a natural! We really are lucky to have you in the Mattel-Toyota-Lockheed Martin family!

All the results from the calibration test look great and you're a natural at this gravity manipulation, so let's continue!

We'll be adding a second sphere and more tracks to this next puzzle, but no sweat! We know you've got this! Good luck!
#### State 2
You're work is exceptional, please stay forever! HA HA. 

We're going to change up the next puzzle a bit, but with your skills, we know you'll succeed with flying colors!

This next puzzle is going to be split in two parts to test the devices capabilities with multiple objects. 

It's like two puzzles at once. It'll be so fun!

Now get on out there and show us what you've got!
#### State 3
You're simply amazing!

We're seeing a bit more entanglement on the device, but nothing we can't tackle together!

We'll keep an eye on the device, and you keep on doing what you're so good at!

We're gonna run another un-split puzzle again and make sure everything's alright. 

We'll make sure to patch up anything that pops up from the increased entanglement, if anything happens at all!
#### State 4
Uh oh! Looks like some unexpected stuff popped up on that one! Those spheres were blocked on specific tracks!

Sorry we didn't catch that before our last chat ended. We hope out color coded solution suited the problem well!

The device's entanglement still looks elevated, but we aren't worried after that last test! 

We are going to continue with the puzzles now! We are going to try another split puzzle!

We expect you'll run into these blocked tracks again, but we don't expect anything else to go wrong! You'll do great!
#### State 5
Oops! It happened again. Seems like some teleportation points appeared on the puzzle. We didn't expect that!

Seems like the entanglement of the device has gone up a bit as well. We'll try to keep it in check, but who's to say what can happen!

Let's move on to our last test of today's trial. We'll try that last puzzle one more time and call it a day!

Before our last puzzle we, again, want to extend to you our warmest of welcomes to the MTL family. We're so glad you're here!

You're contributions will not go unnoticed! Now let's get this last puzzle under our belt!
### Dialogue Implemented
yayyyy it work. Plays dialogue after the 2D puzzle is completed, and lets the player click through the phrase groups.
![[2026-03-16 15-36-19.mov]]
## March 15, 2026
### Dialogue With Audio Test
Recorded a test snip for dialogue just to prove it works. I'm currently trying to twork on implementing that whole system in line with the 2D puzzles and terminal so I just want to make sure it works before doing all that. Sounds like dog butt, but who cares.
![[DialogueAudioTest1.mov]]
### 2D Visuals
Worked on some UI updating for the 2D puzzles, making things look a bit cleaner, adding space for dialogue stuff, constraining puzzle 2d node movement so they stay only in their box. Green thing is the placeholder cursor and where it says "E To Continue" is just testing the text box for dialogue.
![[Screenshot 2026-03-16 at 12.02.41 PM.png]]
## March 13, 2026
### Controllerizing Everything
Started to make everything function on controller. The first big thing was making it so you can walk around and interact with a controller, which wasn't too difficult. I had to change the walking code a bit to work with a controller, but it was more about changing where the code is pulling input from and changing some sensitivity in the camera controlling and actual translation in movement. I also implemented a cursor for the 2D puzzles that can grab nodes and move them around. So technically the game is playable on controller now, but there's definitely more things I need to do to make it feel a lot better. Right now when you do the 3D puzzles, you move around since the controls for moving the puzzle and the player are the same. I can fix this by disabling the players controls when the puzzle is loaded, but I also think I want to have a fixed camera the player looks through when they solve the 3D puzzle so they don't load a 3D puzzle and then were at a weird angle and solving the 3D puzzle is weird. I also want to make the 2D puzzle controls a lot better, since moving a cursor with a controller joystick is a bit tedious. I did make a global autoload that anything can access to see if puzzles are loaded. Many things need to know about this and connecting a bunch of signals would be a lot for that, so I think a global for this will be ok, especially since I need to call it from a specific Global class. But most of the work needed to be put into this is for 2D puzzles. I think the design I have right now will work well, but will be good to have it in sooner to test. The plan right now is to have this cursor you can move around and when you select a node, it highlights all of the connected nodes' path connections. Then I want to make it so you can use the controller bumpers to kinda "tab" through each of those nodes to move then if the player wants to. This comes from player testing where people told me they solved the 2D puzzles by moving nodes that are connected, but far apart, towards each other. I do something similar when solving the puzzles, so I think it would be a good course of action.
## March 12, 2026
### Dialogue Audio
I've been wanting to do TTS for the dialogue for a while now, but after looking into it, I think that doing recorded voice over that's manipulated will be better. I'll have more control over the tone of everything and then I also don't have to worry about another system failing. I would love for the text to appear as the dialogue audio continues and I think I can still accomplish this with recorded dialogue. I think using a JSON files will still be a good route of action. I can copy the same script that's spoke and then use markers in the JSON files to control how quickly text is revealed or breaks in between text. Might be a bit tedious, but I know systems like this exist, so I'm hoping the only trouble will be having to go through the audio files and correctly getting words to appear along with the audio. I'll have to try it out, but I think I should be able to look at waveform in Ableton and see how long phrases and breaks are. I think as longs as I keep a consistent cadence in mind when recording, that should work pretty well.

I made tha thing. It reads the JSON files and prints text sequentially. I don't have audio to test it with yet, but I think it'll work alright, as long as I transcribe the timing of things correctly. The function just creates a series of tweens for each chunk of phrases or breaks, so it should be pretty easy to create something that lets players click to the next set of phrases on each page.
![[Screen Recording 2026-03-12 at 9.05.30 PM.mov]]
### Week 10/11 Goals
- Testing at all steps
- Full controller implementation
	- Big thing here is the 2D stuff with controller. I've got a good idea of how the puzzles will work in 2D after talking with some people on what they think would make this very mouse heavy system work with a controller
- Finish Up 3D and 2D Assets
- Dialogue system setups; would love to finish this if I have the time
	- Probably JSON based
	- Doesn't need to be too complicated; it's just one way text to player with TTS
- Write dialogue for 2D stuff
- Get sounds mostly implemented
- Make transition between states more fluid
	- Right now starting and finishing puzzles is very sudden
- Planning out juice and other Audio/Visual elements I want to add in to help match this world and environment to the narrative beats I have formed.
	- Also really want to get a good amount done on this, but lower on priority list
# Week 9
## March 11, 2026
### Week 9 Progress Report
#### Week 9  Goals
- Work on test feedback
	- Primarily visual distinction and tutorialization
- Tweaking mechanics as they are rearranged
	- I don't think there will be other mechanics added in
- Adding in more 3D stuff into level; might be parallel to working on visual distinction

I think I got a good amount of things done for this week. The visuals are definitely a great addition into the game, making it feel more complete, as well as giving a lot more clarity to the puzzles themselves. I think that the test feedback was implemented well, though I do wish I had more time to test those things that were added in. I got some feedback on these visual improvements, but they were largely from people just seeing the game as I worked on the buggy mess it made as I added the new meshes in. I spent a good amount of time on it this week, but there were a few times that I was just stuck on things for an uncomfortably long amount of time.  This is kinda just a side effect I've mentioned before of bringing in new things to already created systems. Luckily I have a brilliant mind(ruined by higher education) that's able to write a very larger majority of my code without generative AI, and can understand all of it since if I do need to get code from some other source, I make sure to understand whatever I put into my game.(I'm not even sure if there's really any code written by AI in the game, it's largely been unhelpful with things, maybe giving me some kind of direction in where I need things. Good ol Godot forums are always great though.)
### Mentor Review
#### Danny Rankin
I went back to Danny's office hours to get some more feedback after the visual changes I made for everything and get any other feedback he had to offer from his experience. Got some great reinforcement on feedback I've gotten from him and others, being that he thinks this is a good technical proof; there's a box around everything and now I need to fill it up. He could tell most of the time has been spent on mechanics, which he thinks is good, but warned me about underestimating how much time these other things will take. Now that I'm in this spot of having mechanics put up, I'm definitely going into full swing of filling the box up with juice, more visuals, dialogue, and what not. With only a few weeks left, he recommended getting simple, but effective things together to help telegraph this necessary things I want to get across; don't hold back on things but definitely do not overdo. He knows I'm going to have dialogue added in for the final game, and also warned me those systems can be finicky, so don't wait till last second on that. Also, in testing he mentioned how the lines on the back wall interrupted the "lock in" of the game. With visual improvements, he thinks it's much better, but would still like to see something that would make the lines disappear when the player is solving the puzzle. The stationary lines on the back wall just clash too much with the moving lines of the puzzle.

#### Nathan Keyt
Nathan, like Danny, wants to see more of that box filled in. They're very interested in what things can be done to push the points of things falling apart; the whole anxiety thing of the game. They like the structure of the technical side of the puzzles as well, they just think that they'll benefit even more with these other details that fit into this narrative I'm creating. They had some problems with the controls, not really grasping them till part way through the testing. They thought that having a puzzle to just focus on the controls would be very beneficial for players, not having to learn both puzzle mechanics and a new control scheme. Luckily, they do think that the controls become intuitive after use, the problem is just there isn't enough focus on that new skill. They were big proponent of restructuring how the mechanics are introduced, mostly thinking that the split puzzles were easier than the connected puzzles. I'll definitely want to play around with this and see how that different introduction of mechanics works for players.

### Mechanic Reorganizing
I reorganized the puzzles to how people felt the difficulty increase is better. It luckily still works with the narrative beats I have set, which is nice. I've also created a simple tutorial puzzle to help people get used to the controls first. It's a basic single track/single mover puzzle. The singular track follows a similar cube shape like the other puzzles, but it doesn't have any branches on it. Just a track you can either make progress on or lose progress on. Haven't had time to test these changes out, but I plan on doing this in the upcoming days.
### Implementing Models
Man that sucked. Was easy to make gates and movers work, but getting the solve points and portals to align was way harder than I thought. Rotating them to face the correct way based on the points of the paths was just strangely hard. It legitimately took me just 2 hours to figure it out. It was just unnecessarily hard. Then something I thought I had done fixed it? IDK. But once I got it working for the solve points it was fairly easy to get it working on the puzzles. Since the portal meshes are instantiated through code, that was kinda annoying, but I didn't have to figure out how to align the meshes, I just had to make sure the meshes were set up to work with the code I had already written.

I'm here from the future to say that the code to keep the solve points and portals oriented correctly is actually not fixed. The models do face the right way, but they rotate around the axis that is made up by the path. I couldn't see this happening with the portal meshes since they are circular and them rotating isn't visible with their radialness. I had a fix that sometimes worked for the solve points, which are cubes, but I couldn't figure out why they sometimes worked. I currently just have them rotating, since I don't think it's necessarily out of theme for them to be rotating weirdly. They aren't physically connected to the paths so it kinda makes sense. Might keep it like that for now, or make the meshes radially symmetrical. I spent another hour or so trying to figure out how to get them to not rotate and I still could not make progress. Pretty annoying.

I've also got the color coding working on everything, so when you set the color of the movers' emission texture, it also sets that same emission to the corresponding gate.

![[Screen Recording 2026-03-11 at 10.34.40 PM-1-1.mov]]
## March 10, 2026
### Next Steps
I'm going to get those models implemented next, for sure. For other improvements, I'm going to try out tutorializing the controls. I'm going to try out a few different puzzles for the tutorials; they'll all have one mover and then I'm going to play around with the form of the paths on the puzzle. Originally I was thinking of just having a single track where the player has to move the mover from one side to the other, but that might be jarring with the rest of the game being puzzles in cube shapes. So I'm also going to try a puzzle thats a simple cube shape puzzle, as well as a mix of both: a cube shaped puzzle but its just a singular non-branching track. I'm then going to reorder the mechanic introduction of the puzzles, but that shouldn't need any editing to the puzzles themselves. That should be a good point to test again and compare with some of the testers from last week.
### Implementing Improvements
Mostly worked on the modeling of the different objects that will represent the different parts of the puzzle. They currently aren't hooked up to the puzzle parts yet, but I've figured out the scaling, so attaching these new meshes to the mesh nodes I already have in the game shouldn't be too bad. The orientation of some of them matter, so I'll probably have to check the orientation of the path to match the correct orientation. Although I do know that the node that all of these extend from has parameters to lock rotation in certain axes, so that might work for me. I'll have to check that against the morphing ability too, to see if that rotation lock would still work when the puzzle paths move around. These are definitely still prototypes, but I'm hoping the shape and emission shaders they have will work well. Everything should have a distinct enough shape and emission shader pattern on them to help players know what is what, but that's what testing is for, of course.

Next step is to get them attached and test out how the colors/shapes work; if they work in the new lighting and what not. I am trying out a new shader, since the old one actually didn't allow for yellow at all, it just dithered green and red together to make a weird color. Since I'm using yellow as a color and it's also a primary color(so dithering to make it doesn't really make yellow), I want to try out yellow being included in the color palette.

New Shader:
![[Screenshot 2026-03-11 at 10.30.49 PM.png]]
![[Screenshot 2026-03-11 at 10.31.29 PM.png]]
### More Improvements(Plan)
Before I keep going with these improvements, I kinda want to condense down what I have from testing to have more concrete goals. I know what people have problems with, and I want to identify those specific things, identify possible solutions that people presented, and also see what other solutions are at hand for those things.

#### Gates
Gates are hard to see, both in their shape and color. Some people also thought they were solve points on the puzzle sometimes. Simple fix would be make bigger and maybe give them emission effects, but I do think that all these different objects in the game should have different silhouettes/3D models. Big thing these need to communicate visually is the mover that can go through them, which is currently done by color. I think that color is fine(maybe look at color blind options), but I don't want it to be the color of the whole thing. Maybe the mover has some stripes of glowing color on it and the corresponding gate has the same color stripe on it. Would probably be an emission texture.

#### Movers
Movers are hard to see when towards the back of the puzzle. Probably could be bigger, but I could also just make them a bit bigger as they are towards the back of the puzzle. Just increase their scale by a bit through code checking how far back they are on the puzzle. I think that giving them the color coding stripes for the gates would also be helpful, but some puzzles don't have gates. Unless they just had a white stripe on them when there weren't any gates.

#### Solve Points
Again, I want them to not be a basic box cause it looks bad, and then it'll have more visual distinction from everything else. Multiple players also wanted the solve points to give some kind of response if there was a mover inside of it, which definitely makes sense. People were also, in general, getting confused if a ball was in a solve point, especially if there were more things on the puzzle like gates and portals. The only way to really tell if you have a ball in a solve point is if you remember getting one in or if you happen to see the glitch that lets you see through the meshes of the puzzle(another bug I'm not sure how to fix at the moment).

#### Portals
Really they have the same problems as the other things, but they are also the exact same shape as the solve points and in the old lighting were almost indistinguishable from solve points; really really not good. But they're portals so I think they could have a cool effect on them. Would also probably be good to give them some visual if they have a ball inside of them. Some good juice options for these I think.

#### Puzzle Paths
I think that I've for the most part solved the problem of depth perception on the paths. With the setup of new lights, the different parts of the puzzle have different lighting on them, which I think helps with distinction on what part of the path is up front and whats towards the back. Definitely want to test with people to see how it feels, but either way I think it's at least a step in the right direction.

![[IMG_1999.jpg]]
## March 9, 2026
### Visual Improvements
Started working on the visual improvements for the 3D parts of the game. By improvements, I mean for distinction between things, just making the game look better for the sake of the game feeling better. The biggest thing that really made the game not look better distinction wise is probably the lighting, so I tried out a new setup of spotlights in the scene to give things more of a depth. In the second image you can also see some other colored objects on the puzzle paths to show the colors coming through a bit better. They are still a bit dark, so I think that I want to make them glow. I also would love for them to be some kind of vertex shader to make a cool effect, or maybe just a particle effect. The objects on the path definitely still need more visual distinction but I think that this lighting change is a good start. I got rid of the light in the center of the puzzle and added a red light just below the bottom right of the view seen below. there was a light already to the top left of this view, so I changed it around a bit. And I kinda lied about getting rid of the light in the middle of the puzzle. There's one there but I changed it a bit and now it has its shadows set to negative, so where it would've cast light before, it casts shadow. I did that to give more shadow on the paths on the back of the puzzle to help with depth perception.
![[Screenshot 2026-03-10 at 10.48.49 AM.png]]
![[Screenshot 2026-03-10 at 10.56.45 AM.png]]
## Week 9  Goals
- Work on test feedback
	- Primarily visual distinction and tutorialization
- Tweaking mechanics as they are rearranged
	- I don't think there will be other mechanics added in
- Adding in more 3D stuff into level; might be parallel to working on visual distinction
# Week 8
## March 4
### Week 8 Progress Report
#### Week 8 Goals
- Testinggggggggggggg
- More Sound
- Mechanic Refinement
- Refining Visuals of Test Chamber

I don't think all of my goals for week 8 were necessarily met because of how many bugs I had to fix adding puzzles to this new progression state machine, but I was able to hit an acceptable amount of them as I progressed. I think results from testing also put me in a pretty good spot, so I'm not very worried at all about what I missed. There was certainly mechanic refinement and some refining of visuals in the test chamber as I had to fix bugs and changed some visual elements to work in the new area. What was missed in goals, though, was mentioned in feedback from players. I got great feedback on what people want to see for visual refinement in the game, how I can move around mechanics to make the game more understandable, and I even got feedback on how to implement the sound I want the puzzle movers to make as they move around the puzzle. I definitely put in the time I wanted to this week, but I do wish some other things were done. I am very happy still with the amount of bugs that were fixed that most likely don't need to be worried about anymore, and I'm very happy with the feedback I got from the many hours of testing I did. I think the project is currently in a good spot, and I've got a lot of great feedback on how I can keep continuing on the many aspects of the game.
### Testing
Below are the rough notes that I took when observing these individuals while playtesting the game, as well as through discussion afterwards.
#### First Player(Plays Video Games; Not Game Designer)

First 2d ok

First 3d shouldn’t have two goals perhaps 

Couldn’t press e on the things

Gates are hard to see; and colors on followers hard to see; second puzzle

Second puzzle seems easier

Trying to keep on in the solve point and move the other one

Trouble with depth perception but feels its part of challenge(hard part)

Only got to play through first 2 sets of puzzles

#### Second Player(Danny)

Grid in background makes paths hard to see

Overall needs better visual clarity

Feedback on how to make sound: either waveform analysis or just do more dynamic sound

Pulled out a glass jug and metal pipe to make sound of ball moving

Some way to reverse morphing?


#### Third Player(Game Developer)

Balls tiny

Solved puzzle without trying (balls fell into same solve point)

Nodes should disconnect

Mostly visual problems

Indicating solve point with visuals

Tutorial puzzle 

Code making followers not stay together that’s broken has cool quantum ball teleport feel

Wants more 3d puzzles in between 2d puzzles

Gets “surprisingly intuitive”

Likes split puzzles first to understand mechanics

Physics feels a bit slippy, wants to balance ball more

  

#### Fourth Player(Game Developer)

“I like dis”  - after opening the first 3d puzzles

Rotation feels slow

Balls hard to see

Depth test change on for material

Light in the puzzle confusing(on second puzzle)

Wants to see what gate does on second puzzle

Not thinking through

Second puzzle not difficult increase

Focused on pink ball mostly

Just one ball for first puzzle, teach control scheme then do puzzles

First split puzzle easier than gate puzzle

Hardest part is controls, losing control on ball faster

Likes idea of 4 th 3d puzzles, again wants more control scheme teaching 

Starting to grasp controls at puzzle 4

Visual updates will be really good

Wants to see different lighting on puzzle and different distinction

On morph puzzle ball doesn’t move when it should (known bug of ball not moving when on path that is moving)

Portal not working when morphed effect?

Likes weirdness

Likes play with perspective(portals)

Wants more aesthetics(upping polish will make things feel better)

Readjust early puzzles around to get better, maybe split first.

Likes flow going back and forth one 2d then one 3d

Rotation tied to how messed up the morph gets

Timer on last puzzle?

Likes ending on 3d puzzle and not 2d
#### Fifth Player(Plays Some Games; Mostly The Sims and Stardew Valley)

Balls are small

“I don’t know how to get him over there”

Doesn’t like balls don’t lock

Visual indication for mover in solve point

“I’m gonna kill myself”

Prefers 2d puzzle(“like those iPad games”)

Hard to pay attention to 2 balls at once

Wants first puzzle to be just one ball to learn controls better “would make me not want to shoot myself dead”

Not many times when it doesn’t move the way she thinks it would

“I’m gonna shoot myself”

“I don’t want to go back to the crystal room”

“I hate my life”

“Your game doesn’t suck but…… I don’t like this puzzle”- on 4th 3d puzzle

Confused on explaining of portals; need to figure out good way of portals

Really loves 2d puzzles “like those iPhone games you get on instagram reels”

“If you meet someone who likes iPhone games, they’re not gonna like this”

Didn’t like ball not moving when morphing

Doesn’t explicitly say she wants more visual clarity, but definitely wants more visual distinctions

Last 3d puzzle “is not normal”

#### Summary and Game Future
Overall, felt like I got some very good feedback on this run of tests. I had the same amount of testers this time around, but I got to spend a lot more time with testers this time around and overall just got better quality feedback. 2/5 testers were apart of testing last round, though they also have only experienced my game in that last test round. The other 3 have been adjacent to the game, having some minor testing in the past, but haven't experienced all 3 of 2D, 3D, and visuals. Every one I tested with plays games to some extent, though at different levels and different kinds of games. I'd say most of the players play games that are adjacent to this game project, though most of them also don't play mostly puzzle indie games. 

A lot of the feedback I got from the 5 playtesters were fairly similar, which I think is good but also scary. I want to make sure I have all the things worked out in the game, but having very similar feedback from everyone, that's also things I know I need to do, makes me worried something was overlooked, or everyone was too kind about it. Realistically, probably a good thing and not something I should worry about too much. The biggest parts of feedback, I'd say, between the group had to do with the puzzle ordering and the visual indication/fidelity of the 3D puzzles. 

For puzzle ordering, most of the consistent feedback was in the beginning and end of the puzzle progression. Everyone felt that the first puzzle should be a puzzle that's used to teach the control scheme of the game, not necessarily introducing anything about moving multiple movers around the puzzle. This feedback either came as direct communication of wanting more tutorial puzzle as well as multiple testers saying they wanted the first puzzle to only have one mover. One person who told me the first puzzle should just be one mover had told me recently that a puzzle with one mover already feels like a puzzle, even if there isn't a balance of movement between two of them. From feedback for a tutorial puzzle, it seems players either want a singular path they have to rotate to get a mover from one end to the other or a simple cube shaped puzzle that gets players used to rotating a puzzle how they want to rotate(this matches more with how the puzzles are already cube shaped). All players found it hard to get used to the control scheme while also having to learn how to balance the movement of two movers on the first puzzle. Multiple expressed how they only got used to the controls a few puzzles in. As for the end of puzzle progression, a few players had expressed how they either felt how the end was very hard, or needed to be crazier(not necessarily harder). Most of the puzzle reordering was how people wanted more of a ease in to the puzzle mechanics, from a tutorial of the puzzle controller. Some also felt that the gates should come after the puzzles are split, but feedback suggested that the split puzzles, with gates and portals was a good difficulty level for where it was placed in progression. Definitely happy with this feedback, since I was worried about how I could tutorialze the beginning of the game. Having consistent feedback on that is reassuring on how I can do that.

The other large consensus of feedback was on the visual aspects of the game(also extends to other juice elements, but for now just visuals of puzzle matter). I've been testing the 3D puzzles in a scene that was basically a blank Godot world, with just some fog to add depth perception; no shaders or models around the puzzle. This new main scene adds a lot: those shaders and 3D models, as well as more dynamic lighting. It doesn't work great right now. Before testing, I knew there were some problems with seeing the rails, so increased their size a bit, which I do think helped, but a lot of other issues arose, mostly with lighting and the shader. With increasing the rail size, I didn't increase the puzzle mover size, which made the mover ball kind of disappear into the rails when at the back of the puzzle. Had to tell people where the mover was multiple times when testing. This was one of the visual issues that I didn't know about, which is good. There were also issues in the color coding of things. The gates I added were color coded to the puzzle mover sphere colors and the portals are the exact cube shape as the solve points of the puzzle, just gray, which didn't show up very well. Most of this is due to lighting, though I do want to have other physical indicators in the models to show what things are. The lighting of the puzzle area made all the colors really dull and hard to tell apart, especially at distance. When the portals were introduced, the yellow light inside of the puzzle cube just made the portals look like solve points which was super confusing. 

That light inside of the puzzle also causes other problems as well. This light makes the paths towards the back of the puzzle very bright and the ones closer are in shadow. I'm surprised I didn't get more complaints about that, it really tripped me up sitting off to the side of the screen. The whole depth perception was off for me, but some people did complain about it. I think the big issue with that, is that in basically any visuals, as well as with real life in fog, things get darker/loose saturation as they become further, but that's the opposite with this central lighting feature in the puzzle chamber. Definitely needs to be a relighting of the whole area, making sure things are visible. Will also do this with modeling and texturing of the objects on the puzzle.

Honestly, this felt like most of the feedback, was between these two. Everyone had great response to 3D and 2D puzzles(except for player 5 who I think the game didn't fully match up with what they usually play). I had I think 3 or maybe 4 of the players tell me they thought the mechanics felt good and that bringing the visual distinction up, as well as other juice factors, would bring the game to the next level. I definitely want to keep exploring how I can play with the mechanics to make them better, but having consistently good response to the puzzles is very pleasing. I definitely want to start working on the visual and juice of the game more, as we approach the last few weeks of capstone and this makes me feel great about moving more towards that. I'm definitely not going to stop working on mechanics at all, but those systems and implementations seem fairly concrete at the moment. Very happy with this feedback, and I think there's much to work on with what I've got. There wasn't anything that made me worried about having to trash parts of my game and there was much constructiveness in the feedback, which will be great for launching forward.

### Before Testing
Had to do some more fixes on my testing material just to make sure things would go smoothly, I hadn't had the time to fully go through everything since I had to solve all the puzzles to test everything in order. To get through things to test more easily, I added a debug tool that lets me send the puzzle finished signal from the editor, so if I needed to skip a puzzle, I could hit that and get through.

I also had to finish up my 2D test puzzles, cause I hadn't finished them the day before. It took me maybe an 30 min to an hour to get together some 2D puzzles together that felt like a good progression. I still haven't decided how I want to end the game, so for the last puzzle I made it hard instead of just completely impossible. Even if I eventually go for the end puzzle being impossible, it'll still give me more of a scale to test with. The last puzzle I had set up was also before the last 3D puzzle, so having it impossible to complete wouldn't be very useful for testing the progression of the mechanics.
## March 3
### Moreeeeeeeee Tessssttttt PReppppppp
Making some more puzzles to test today. Naturally, integrating my puzzles together, there are some bugs with things that show up as I go along, mostly in the puzzle effects. Fixing the gates the other day was part of that process and there are even more things to fix today! The portals were having a weird issue where they weren't teleporting correctly and was a bug that I had put off to fix later, which was (lucky for me) today. Like many bugs that you test and test and test and can't find the solution to forever, the solution to this bug was I was setting a variable on the path the mover is teleporting to, not the one it was teleporting from. So the fix was just removing a variable reference. Took so long to figure that out. 

I've also started integrating the morph effect with other effects, like puzzles and gates, which is running into a few more bugs. Gates, portals, and puzzle solve points are all represented physically on the puzzle, but only gates and solve points are PathFollow3Ds and portals are just meshes that the path with the effect spawn in. The problem with the PathFollow3D inherited nodes is that when the paths morph, the followers' progress is kept constant and their progress ratio is altered as the path length changes. So when I have a gate at the half way mark of a 1 meter long path, when that path changes length, the gate stays at .5 meters no matter how long the path is. I want the ratio to stay constant. Fairly easy fix in tracking what the original ratio is, then changing it to the original value if the ratio is changed. For the portal, the mesh is spawned in at an end point of the path it's on, and when the paths morph, the portal stays in that original position. This just means the mesh has to have its position changed as the path morphs, following that endpoint.

Of course the morph ability also has some more issues once actually in the game scene. The scene I've been testing in has the puzzle centered around the origin, but in the game scene, the puzzle is about 9 units away from the origin of the world. This messed things up since most of the code I wrote for the morph effect was working in positions relative to the world origin and not the puzzle container. This made the paths morph out of the visible area of the playspace, definitely not an intended effect. Once I made everything more consistent in positioning, that fixed the paths moving outside the bounds I wanted it to act inside of. Once that positioning was fixed, there was still an issue with how I indexed the path points, so when the puzzles morphed, the intersection points didn't move together. That was fixable by doing the position indexing not through localization functions, and just adding positions manually to make them "local".
## March 2
### Gates!
Finally got gates working. They are supposed to only let in the allowed puzzle mover. I was trying to set it up so the gate just applied an inverse square law force to the mover as it got closer to it. This was supposed to make it stop before the mover got to the gate, and kinda bounce away from it. I had the code set up for it, but it seemingly didn't work. I had tried to debug it for a while and couldn't figure out what was going wrong, but luckily had a realization yesterday that the code of the gates was running before the code that determined the acceleration of the movers, so the acceleration change from the gate code was basically being ignored. I did maybe not great of a fix, but it works. I have code that runs path effects after the movers' gravity code is ran, mainly for the time dilation paths, but in that code I now also check if there is a gate on the path, and if there is, I just run the code there. There's still a slight problem with the gates, but I think it could be fixed by fixing the code that keeps the movers separated. Movers are supposed to exert that same inverse square law force on each other when they get close, sometimes they like to not and will move on top of each other. When they do this while going through the path, there's clearly some force that happens, because it ends up pushing the movers through the gate with that force. Kinda annoying, but I think I can fix the mover code, them not staying apart has been kind of a consistent issue for me.
### Test Prep
I'm makin puzzles. To test them. I started on the 3D puzzles, making the first two puzzles in the sequence of 3D puzzles. I'm trying to follow the beat structure I had set up a while ago with what mechanics I have. I'm mostly testing the sequentialness of the mechanics, but I also do want to know how these new mechanics feel. Now that I have things in the full shader part of the game, I also want to know about how things work visually with the puzzles. I don't have visuals finalized yet, but there's definitely insights I can get on how things look with the shader.
# Week 7
## February 27, 2026
### UX/UH Testing 2
- Having progression system done, I really want to look at the sequentialness of the puzzles
	- How they work going after one another
	- Difficulty Progression
- I can also more grasp what the time to complete will look like based on how fast people are able to finish puzzles
	- I still don't have a great grasp on the difficulty of the puzzles, especially after changing mechanics up after last test period
### Week 8 Goals
- Testinggggggggggggg
- More Sound
- Mechanic Refinement
- Refining Visuals of Test Chamber
### Week 7 Progress Report
#### Week 7 Goals
- Refine Mechanics
- Level Progression System
	- How I can load 2D and 3D puzzles
- Player Interaction on Items
	- Would be pretty easy and good to test level progression with
- Sounds/Music start

I'm happy with the progression system for the levels finally being in place, it really makes it all feel like it's more cohesive. It's also great for me, cause it was something I was dreading doing. I don't really like pulling systems together like that, and I know it's necessary, but I just like making the systems more. Being something I didn't want to do, it means that I feel like I've hoisted myself up to the next tier of making the game. Pulling everything together was something I was unsure of, but now I've gotten over that, there are things I can go back to for the game that I know how to do and how to iterate on. I do wish I had spent other time on things this week, especially on the puzzle effects, but this was very necessary and it just happened to take up most of the time. I chose to do some sound stuff just to get it started, since I hadn't really had much for it yet. Now it's started and another thing for me to work on if I need a break from code and such.
### Audio
I messed around today to try out some sounds I could use for the game. I made a lil synth in Ableton that sounds a bit dark and crunchy, and I think it would be good as an ambient drone for when the game starts up, maybe just going back and forth between two notes. I think I'll have a fairly basic start screen that can be used to load games and what not, and I don't think it'll have much music; maybe just that kinda drone synth. For sounds in game, I was gonna have some ambient sounds of the test chamber: maybe some thing AC fan noise, noises for the terminal, stuff like that. I also wanna have kinda a metallic scraping noise for when the movers move along the path. I was messing around with some procedural audio generation in Godot, but it's a bit funky, and IDK if it's time well spent to try and find a way to generate the waveform of metal scraping. There's some mix of sine waves to do that, and I ain't the one who's gonna figure that out. I think if I can find some resources on how to match those waveforms in code, or able to generate a waveform off of an inharmonic spectrum of that sound. Most stuff that's fairly easy to generate are basic musical instrument sounds, of course able to get very basic synth sounds. An alternative to straight generative audio is using premade sounds, or making my own and mixing them to be more dynamic in engine. This is probably the best way to do the movers on the puzzles, but I would love to get the generative audio working. It's cool in concept, but I haven't been able to grasp it fully.
### Controllers and State Machine Finish
I've got the whole progression state machine system working now, being able to go from puzzle to puzzle as you progress the game. Nothing happens when you run out of puzzles at the moment, but I have room for where I know that will go with the state machines. Having all of these different things hooking up that weren't before did have its challenges, certainly in parts where it was cyclically doing things or just not doing what I wanted it to. A lot of those problems were just simple logic problems, which were easy to solve, but tracing to the point where things were failing was definitely tedious. I was worried that I'd have to kind of hard code things to make them work correctly, but I think what I have feels good structure wise, it's just that some things are connected in a few lines of signals(eg. The 3D puzzle fires a finish signal to the controller, the controller fires to the state machine, and the state machine fire to the interactable the player has to interact to start the puzzle). It does make sense to have this chain of signals I think, since all these different things need to do things when these signals are fired, and also hooking them all up to the same finish signal would be a bit weird in accessing all of those things, when the interactable doesn't really need to know about the puzzle at all; it just needs that signal to make it not interactable.
![[progressionsystemtest.mp4]]
## February 26, 2026
### Controllers and State Machine cont.
Connecting these various systems is usually where things fall apart, and frankly also something I don't have as much experience in. I know that usually connecting these distinct systems in Godot is usually done through an event bus using global systems to transport information, though this is a small enough scale where individual signal connections and export variables should be viable in transporting that information. Everything is pretty condensed in where they live on the scene tree, and it helps that not a whole lot of stuff is being dynamically created that I have to control.

Now that I need to also know when puzzles are completed, that's another one of those things that needs to be tweaked from an older script to make this new progression system work. These are going to be done with some fairly simple checks: for 3D puzzles I need to check if the puzzle movers are in the correct place, for 2D puzzles, I need to make sure all the nodes are untangled. 3D puzzles should be able to be done with position checks, and I already check if node connections are crossing individually for the 2D puzzles, so I just need to consolidate that check to them all. There's also the consideration that the 2D puzzles are not the only thing accessed by the terminal interaction. When the player interacts with the terminal, they will complete the 2D puzzles and then be given information through the terminal too, so that interaction with the terminal more acts as just switching from the 3D scene to 2D. 

The 2D and 3D parts of the game are also accessed alternating, so that means that only one can be interacted with at a time, which means they have to be able to tell the other they can be accessed. Since I don't necessarily want to do that directly, I have it set up so that the state machines for the 2D and 3D puzzles can tell each other when the puzzle controller they talk to can be interacted with. I don't have it set up in high fidelity yet, but I will have some more visual elements for when something is interactable. The terminal has an on screen when interactable; the shutter to the 3D puzzles are gonna have a button that lights up when interactable. Then opposite of that, when you finish the 2D section, you'll exit back to 3D and the terminal will go dark; for 3D , the shutter will close and the button won't be active.
## February 25, 2026
### Connecting Controllers and State Machine
Started to connect all the separate things I've got to connect for this. It's definitely been a bit annoying, since most of the code I've been writing has been for singular systems, so I was staying within like 2 or 3 scripts at once for those. Now I'm traversing different scripts for different systems, making sure everything connects correctly. It's also altering scripts I already have to make things work, which isn't a one-sided thing. Kinda everything has to be at least tweaked in some way.
## February 24, 2026 
### Puzzle Controllers
Had to restructure the controllers for the 2D and 3D puzzles to make sure they could interact with the state machines. The main thing about this was that I didn't have the controllers integrated in the actual scene the player can walk around in. This wasn't too hard for the 3D puzzle controller since it already exists in 3D space I can just kinda place it into the scene and change the code a bit. The 2D puzzle controller needed a bit more work on it, since it exists in 2D space, and needs to be usable in the 3D scene. It's still not terribly difficult to integrate it into 3D luckily. It needs to be on a separate canvas layer, which is luckily for independent rendering of 2D scenes, layering it on your base rendering or other canvas layers. I also had to restructure the scene tree for it as well, since the 2D scene has its own shader overlayed on it, separate of the 3D scene. The shader for the 3D scene also lives in a canvas layer, so it basically just has to be hidden when the 2D puzzle canvas layer is shown. Node wise, not too much change, since I had known I would need a way to load the 2D puzzle data at some point, and should work once integrated with the state machine.
## February 22, 2026
### Level Progression
For level progression, I'm going to use a finite state machine to control what puzzles are loaded after puzzles are finished. Usually state machines are used to control some more complex behavior, but they still work great for this, since it lets me track what puzzle is loaded and what puzzle is loaded after that puzzle is completed. This will also make loading and saving a lot easier, since I can just make it so when you save during a puzzle, it just loads the puzzle at the beginning through the state machine. I have the bones of the state machine right now; the actual state machine and the states that hold the puzzle information. As of writing this, I don't have the means to test it since I don't have the interactions in the world to actually call the puzzles to be loaded. For the 2D puzzles, this will be interacting with the terminal in the test chamber; for the 3D puzzles, this will be done by interacting with a button to open the shutters of the test chamber window to reveal the 3D puzzle.
#### Interactions
I can use some of the same techniques I used for the portals for the interactions. It's not any big part of the portal code, just how with the portals, they detect if they are overlapping on the screen by checking if they are within a certain distance from each other in the screen space. If I use this same technique, and instead check if the interactables are within a certain area in the center of the screen, as well as if the player is close enough to interact. 

Having this level progression and some interactables is making me want some more organization within the code, since I feel this is where some bad spaghetti code can start to come into play, now that I'm no longer working in only the context of the puzzles separately. Now I'm connecting interactability with level progression and then that informs level loading. A big tool that Godot provides for reducing circular referencing is signals, which allows me to signal to other nodes and scripts when certain requirements are met. In those signals I can also pass through arguments for functions that are called when signals are emitted. Overall just streamlines what other nodes know about each other, rather than referencing whole nodes just to access singular properties.
## February 19, 2026
### Week 7 Goals
- Refine Mechanics
- Level Progression System
	- How I can load 2D and 3D puzzles
- Player Interaction on Items
	- Would be pretty easy and good to test level progression with
- Sounds/Music start
# Week 6
## February 18, 2026
### Week 6 Progress Report
#### Week 5 Goals
- Explore other mechanics that can flesh out one of the possible branches of difficulty the base mechanics of the game can take on
	- I want to get wacky with it, really letting the themes of the game come through and integrate with the narrative
- Developing the rough form of the narrative to help inform puzzle progression and other mechanics
- More 3D asset generation

Definitely didn't get the 3D model generation I wanted to get done, butI'm happy with the other ability work and tweaks that I made. I'm starting to feel like the stuff I have isn't just a pile of things, even if it hasn't been a pile of things from the start, just things that couldn't go together yet. I feel like I've got a good motivation to work after I've got these new mechanics down, so I'm excited to get the puzzles feeling better and putting things together.
### 2D Assets
Created a more full 2D scene for the game. Definitely not how I want it to look in final, but a better feel for how it'll be in the game. Used a concept for made a few weeks ago for how the layout is.
![[Screen Recording 2026-02-18 at 11.12.16 PM.mov]]
### Newwwwww Portals
I worked on the portals yet again. After testing and getting feedback on portals, they were just not it, so they were changed to something that feels better and has more opportunities to matter in terms of gameplay. The basic idea is that the portals still teleport like normal, but to make a mover teleport, the mover need to be sitting in a portal and then the portal pairs have to line up visually. Maybe a bit confusing in words, just look at the video and it'll make sense(maybe). Definitely some fun juice options for this.
![[Screen Recording 2026-02-18 at 11.14.38 PM.mov]]
The portals work by looking at where the portals are in the camera screen space and just checking if they are close to each other, then teleporting the mover if they are close.
### Control Tweaks
I changed up the controls a bit to make them feel a bit better. I kept how the rotation works using the joysticks, and added some capability of finer movement. Before, the rotation speed of the puzzle was either nothing or full speed, which didn't feel great, especially with a game where you kinda need some fine control of movement. Pretty much just makes it easier to do finer movement with the current controls. Not a huge thing, but I think it's overall a great improvement for the game.
### Morph Ability cont. 2
After yesterdays advancements, there were still some bugs with the paths moving, and the meshes didn't line up with the paths like they need to. The main bugs of the ability were with the bounds in which the points were allowed to move;  where in space and how far from their original location. Those were pretty easy to fix up after doing some testing on some logic in the code.

The other bigger unresolved issue was that the meshes were not lining up with the paths. It looked kinda cool but it wasn't anything that made sense. You can also see how the paths were acting weird in the video below.
![[Screen Recording 2026-02-17 at 9.05.00 PM.mov]]
I had to change how I drew the path mesh, which wasn't too big of a hassle, but I wish I had just done it earlier cause I wanted to do it this way I did it not, but I was too lazy to do it earlier. After fixing the mesh and path behavior issues, it feels pretty good, even with a puzzle not designed for it.
![[Screen Recording 2026-02-18 at 11.18.31 PM.mov]]
## February 17, 2026
### Morph Ability cont.
Now that I could collect the points I wanted to move, I had to figure a way out how to move those said points. It was kinda of annoying cause of how Path3Ds and Curve3Ds work in Godot; the points inside of the curve that is stored on the paths are just really weird to access since you have to know the index of the points to access them since you can't just get the array of points on the curve. I'm constantly flipping the points in the curve arrays to make sure that the paths are pointing downwards, so I need to know when the points are being flipped, which I just tracked through the point tracking dictionary. The dictionary that stores all the points eventually became a dictionary of arrays that were full of dictionaries that had arrays inside of them. A very optimized system of variables. Anyways, it let me track all of the necessary information. 

To move the points, I used Godot's built in Tween system, which is basically just allows interpolation of any property or property through method argument, which is the one I used. I have an "engine" that knows how many points are moving at once and caps it at a certain number. It randomly chooses points from the dictionary of points that are stored and sets a new destination for that point in space with some bounds. I want to make the lines not overlap as they move, but that's not set up currently. A Tween is created for each point that needs to be moved, and that tween uses a method that takes the point in as input, which then the method interpolates that original point to the new point over time, while also looking at the dictionary to update the separate points on the paths that are connected to the currently moving point.
## February 16, 2026
### Morph Ability
Made the ability resource for the morph ability that can be applied to the puzzles. Decided to just have the points of the path move randomly for now instead of having any specific movement of the paths, like in some kind of tesseract. Working on this, I made a system to collect the points of the puzzle paths and also collect the separate paths that intersect at those points. Wanted to get started on this before it was too late since I knew this one was gonna be a bit complex to make. 
## February 15, 2026
### Work Cont.
Fixed the rest of the mover code that was supposed to determine where movers would go at intersections. It doesn't account for if there's an effect at an intersection, so if a path has an effect at a point, then the mover code wont tell the effect its on it if its at the intersection but on a different path. I don't have any point effects at intersections right now or any plans to add any that need to be, so it's not the end of the world. Can also just check for movers through the path or effect if I need to.
## February 13, 2026
### Reworking Code That Moves Movers
There have been known bugs with the movers' code for a while now, but it hasn't been too much of an issue, but with the new planned mechanics, I can foresee the bugs getting in the way, so I want to fix them now while I'm not also thinking of fixing them specifically in context of the mechanic I'm trying to add. When movers are at intersections, the logic of what path they switched to was a bit messed up, making the movers lock up sometimes or just acting in unpredictable ways at times it would be nice to know how they would behave. There was some logic that I had written that didn't really make since, but I knew what I could replace it with to have better behavior of the movers.

There's still code that is supposed to keep the movers separated on tracks, but I think that fixing the unpredictability of the movers could help with that. There's also probably some edge cases I haven't recognized yet that could help fix that function.
### New Mechanic Progress
I started work on the mover specific gates I can place on the puzzles. They're pretty simple, just a thing placed on the puzzle path and has a single mover assigned to be able to go through. There isn't any visual indicator for what mover can go through currently, though I'm going to assign their meshes the same color right now. Definitely want some other more stylized visual to show give indication of relation.
## February 12, 2026
### New Mechanic Technical Plan
Wrote down how I think they can be implemented into the current structure of the code to help me make them more smoothly, hopefully everything makes enough sense from my mind palace.
#### New Portals(PointEffect)
- Should be able to scavenge code for how movers teleport to different locations on the puzzle. Still a bit buggy.
- To check for the line up of portals, can probably compare the vector of the camera to the vector between the points of the two portal locations
- The code does't currently check if there's another portal to teleport to on the other path, it's technically just a one way teleport that happens to have two portals at each others teleport spot. Will need to check other portal location and if it's the right pair.
#### Rails Falling Off(PathEffect)
- I know when a path mover leaves a path for another path, so I can set up a signal on that to trigger a path to fall
	- This comes from the code that moves the movers along the path, which can be a bit buggy at intersections. When a mover reaches an intersection of path points, the path that the portal is actually on at that point is a bit unpredictable.
#### Separated Puzzle
- Make a puzzle that's separated...........
#### Axis Lock(Puzzle Rotation Code)
- Check for what face of puzzle and what orthogonal angle from face is closest and rotate the puzzle to that.
#### Tether(PuzzleEffect)
- Check distance between movers in the puzzle local space
- For movement constraint, can kill movement if the distance reaches a certain threshold
- Other effects, the effect can occur when a similar threshold is met
#### Gates for Certain Movers(Attachable Scene)
- This could fit under the PointEffect component category, but I think it would make more sense as a separate scene I can attach to a path.
	- Making it a scene and not a resource lets me physically attach it to a Path3D as a PathFollower3D, which can then be placed anywhere along a path instead of at an endpoint. 
	- Making it a scene also lets me attach the movers I want to be able to go through it directly through an export variable. I also have export variables on the component resources, but making it a scene lets me actually reference the mover's scene in the export variable rather than as its NodePath which is just how the resource can find the follower in the scene tree. 
		- Kinda complicated but making it a scene just simplifies the effect
- The gate would kill movement for any mover not allowed through and not effect the mover that is allowed to pass.
	- Gate could also make the follower bounce off or something. More of a juice thing, but either way does something to make sure the mover doesn't pass through.
#### Path Morphing(PuzzleEffect)
- I have most of an idea of how to achieve this effect, but there are some things I know I need, but don't have a clear understanding of how I can do it at the moment. I have an inkling but not much more.
- Something has to determine the behavior of how the paths morph around each other. 
	- If that movement is random, there needs to be some kind of algorithm that knows the locations of the paths and moves the paths in semi-random ways.
	- If the paths were to move in a predictable way, there would need to be some kind of (probably) parameterized function to move the points around. My calc 3 knowledge makes me think this but I may be wrong. I'm sure there's math on how you can do the 3D representation of a tesseract.
- There are some commonalities on how either of these work
	- The location and orientation of paths needs to be known, which can most likely be accomplished through the endpoints of the paths.
	- This would be indexing all of the endpoints of paths and what endpoints intersect
	- Problem with endpoints is that with the PuzzlePaths of the puzzle, they have a base physical location in space and then the actual line is defined by the Curve3D attached to it, which is just two points in the local space of the Path, with one point always being at (0,0,0) which is the same as the base physical location of the path. I'm not sure if any code relies on that point staying at (0,0,0), so I either have to keep a point at (0,0,0) and move the base location of the path as well as the other point at the same time, which sounds like a pain of math, orrrrrrrr I could keep the paths position stationary and just move the path endpoints of the curve separately, in context of the whole puzzle space.
	- Either way, kind of a lot, but I am confident I could figure out either of those systems. It's just they're both complicated and feel weird to do.
### Week 6 Goals
- Implement new mechanics and refactor other ones to new mechanics
- More 3D asset creation
- 2D assets and shader refining 
# Week 5
## February 11, 2026
### Week 5 Progress Report
#### Week 5 Goals
- Explore other mechanics that can flesh out one of the possible branches of difficulty the base mechanics of the game can take on
	- I want to get wacky with it, really letting the themes of the game come through and integrate with the narrative
- Developing the rough form of the narrative to help inform puzzle progression and other mechanics
- More 3D asset generation

Though I did do everything mentioned in the goals, I do wish there was more time spent on everything. I got sick for the first half of the week, which definitely knocked me out from working on a lot of things, but I still tried to work on more design elements, which I was able to do without sitting in front of a computer for a long time. I'm happy with the work I got done on the mechanics. I think that the brainstorm and figuring out what I wanted and from that what worked and what didn't in theory was really helpful. Developing the narrative and fitting mechanics to that was helpful and I think it's gonna help me a lot with how I'll proceed in the next week with new mechanics. Reworking the mechanics definitely integrated a lot of feedback, a lot of the new ideas for mechanics were developed while conducting tests last week.
### 3D Things
I felt the part of the test chamber the player is in feels a bit too flat so I played around with how adding a noise texture to the ground could help make it feel a bit better. I also added a terminal in to the room to make it feel that much more homey. I definitely want to play around with more texturing as well to work with the dithering since without much variation in the texturing it looks a bit blobby.
![[Screenshot 2026-02-11 at 9.15.23 PM.png]]
### Outside Mentor Review
For my other mentor, I talked to a good friend who recently graduated with a computer science degree and is very well acquainted with the Godot engine, making his own world terrain generation, system to climb on enemies as you fight them, and other fun, complex system. I wanted to get his input on my code architecture, making sure I keep things as streamlined as possible for adding new things in through code, mostly the mechanics for the puzzles. I have a pretty good knowledge of good code architecture from other comp sci classes, so I've tried to keep the components for everything fairly in line. After explaining how I set up the components for everything and showing him the code and tools I created for adding components, he said the architecture was pretty good, but in some places, was a bit cyclically referencing; sometimes a puzzle path references a path ability but the ability also references the path. In a better architecture, the ability shouldn't really know the path exists, but he said that since the scope of the ability and path was so small that it wasn't too much to worry about. He said to just be careful about where that happens and know the architecture of everything well enough to be able to know that cyclical reference isn't going to effect anything outside of that, or mess anything else up, which in this case, I was pretty certain when creating it would not.
### Mechanics Future Organization 
#### Mechanics That Stick Out(What Beat They Could Fit)
- Portals that work when lined up - Beat #2
- Rails fall off as movers move off of them - Beat #3
- Portals between separated parts of puzzles - Beat #2
- Axis lock to face - Beat #1(Base Mechanic)
- Tether movers together for movement reduction or some other effect - Beat #2
- Gates for certain movers to pass through - Beat #2
- Puzzle paths morphing into other shapes - Beat #3
#### Currently Made Mechanics(as of writing)
- Basic rotation
- Shift between 2 puzzles
- Portals
	- Probably deprecate in favor of other puzzle system
- Time dilation paths
Basic rotation, shifting, and time dilation would be good for Beat #1. Portals don't have the kind of meaning/importance to the puzzles right now that I would want them to to keep them in the game.

#### Possible Progression of Mechanics(in terms of narrative) 
This is more of a layout of how these mechanics could work in order, for the sake of thinking about what works well together and what could be meaningful to the puzzles. This isn't necessarily the order of what I want mechanics to be added in, just where I think the mechanics should be in the progression based on current mechanics. The purpose of this is to help out with subtractive design; finding the things that effect the player and the game and eliminating the things that aren't meaningful or create a less meaningful experience in the presence of a more meaningful mechanic
##### Beat #1
- Basic rotation
- Shifting
- Time dilation paths
- Axis lock
##### Beat #2
- Portals
- Separated puzzles(connected by portals)
- Tethering movers
- Gates for certain movers
##### Beat #3
- Rails falling off as movers move along paths
- Paths morphing 

##### Notes On This Progression
- Adding these other mechanics, I think that shifting between puzzles might be too much, especially with either of the mechanics I placed in Beat #3. I think that if I were to do the paths falling off, I would make puzzles that had more of a correct path to complete, and having to figure out exact pathing for two puzzles at once, one of which you couldn't see, then that would be reallyyyyyyy difficult. For the paths morphing, I think that since there's so much visually changing it would just be near impossible to actually complete that puzzle or it would just have people doing random things to solve the puzzle. Overall, I think I want to keep everything mostly visual feedback and I think that shifting would throw many wrenches in many cogs when adding more mechanics.
- I like the time dilation paths and I think they had a good response in testing, but I'm worried they could become more inconsequential through progression. That could benefit the game though, since I want players to kind of shift priorities around in their head on how to solve puzzles
- After testing, the portals just didn't feel like they were it. They were on the puzzle but it didn't feel like you needed to use them. I'd had ideas originally to separate puzzles and use portals to connect them and I had some people separately tell me that portals could be used that way, so I think it could work well. When Danny first saw the portals, he had said he liked the idea of portals having to line up to let movers go through, which I really like the concept of.
- Separating paths on puzzles could be nice and give a similar effect to shifted puzzles without the visual disconnect, but I definitely think they could work best if paired with portals. Maybe separating puzzles could be a good Beat #1 addition and adding portals in Beat #2
- I've said it a few times, but originally I only had tethering as a movement constraint mechanic in my notes and when I was annotating this progression I added that maybe there could be other effects. I do think that movement constraining is a good mechanic for that, but I can't think of too many effects the tethering could do that would make sense in context of people knowing what a tether does between two things. Maybe the tether could make gravity flip or something if the movers were close enough, but I think have a visual connection between two movers to represent a tether would make more sense with movement constraining. Anyways, tethering could maybe cause another effect to happen
- Have certain gates only specific movers can go through is another idea I quite like that constrains how the player can solve the puzzle. I know I said for Beat #2 I wanted less physical manipulation for the puzzle, but I think that the concept of making the player adapt how they solve the puzzle to the new mechanics in Beat #2 definitely fits with the effect the gates would have adding them to the puzzles.
## February 9, 2026
### Narrative
#### Beginning
- Player "wakes up"
- Fades in from black(or some other transition), player standing next to bed in test chamber.
- Shutter for test chamber window is closed
- Terminal is flashing as the only dynamic lighting in room to attract player
![[IMG_1889.jpg]]
##### Information for Player
- Corporate Spiel
- Player has been assigned to test experimental black hole-powered gravitational device
- Compensation will follow test completion
- Begin with calibration test(tutorial puzzle)
- Please return to terminal after calibration test is complete
	- Info on untangle puzzle will be given after player returns
#### Between Beginning and End of Game(3 Beats)
##### Beat 1
- Introduce a few 'known' mechanics under pretense of testing material
- Everything seems operating normally
- 3D puzzle mechanics not too difficult, no subversion on things taught
- 2D puzzles are not complex; feels like a simple, necessary task
##### Beat 2
- Unexpected effects begin to occur
	- Maybe effects that don't alter puzzles much physically, but make players have to adapt how they solve them
- 2D puzzles add more nodes but aren't too much more complex than in Beat 1
- Some audible/visual effects from black hole
	- Since I came up with this concept I've wanted to have some kind of light bending shader at the bottom of the screen, like a black hole bending light. could look cool in dither shader.
##### Beat 3
- Apparent that device is becoming overwhelmingly unstable
- Starts to physically effect chamber and puzzles
- Player can't just adapt too solve 3D; starts using different systems maybe
- 2D starts to be more complex; maybe they even retangle themselves as player solves them
#### End
I haven't really decided how I want the game to come to a close yet. I don't really want the player to explicitly survive the experience, as in through visuals or text it's clearly shown the player survives the ordeal. I'm kind of leaning towards a more vague ending where while the player is solving a 2D or 3D puzzle, the screen just goes black after the roof collapses or something. I think I could be ok if I ended it more implying that the player doesn't survive, for sake of showing that giving your soul to a corporate entity and now taking care of yourself will be your downfall, but I also don't want it too be too dark of an ending, even if it does have psychological horror elements throughout the game.
## February 7, 2026
### Mechanic Brainstorm
Gathered potential mechanics that could work well with the base puzzle mechanic that exists currently. Includes potential mechanics that were discussed during testing as well.
- Switch to instead of controlling rotation of puzzle, you control gravity
- Portals that work when they are lined up visually
- Rails that disappear after puzzle movers move across them
- Portal between puzzles that are shifted
- Have puzzles be separated in space and make it so only portals can go between them
- Rotating paths that change what paths they are connected to
- Invisible paths
- Axis lock to nearest face
	- Not much of a mechanic; more of a quality of life to be able to more exactly control the puzzle more efficiently(maybe, Danny recommended before he found you could rotate the puzzle in a roll motion in front of the camera)
- Draw a specific shape on the paths with one of the puzzle movers
- Line up the paths to make a certain shape
	- There's some instances in The Witness where you have to do things like this
- When the puzzle is solved, the orientation that the paths are in determines the node layout and connections seen in the 2D puzzles
- Reverse the controls on the controller
	- Would be something for when the device the player is testing becomes unstable and messes up controls but kinda feels too on the nose
- Movers can fall off of the puzzles at certain points
	- Don't know if it's really something I want to be able to happen
- Movers connected by tether and can't get too far apart
	- This could also just be a proximity thing that allows for some other effect if the movers are close enough
- Gates on paths that are only for certain movers
	- Could give more control of how players can solve the puzzles
- The paths of a puzzle can morph their length and orientation allowing for puzzles to morph into different shapes
	- Kinda first had the idea of turning shifted puzzles into like a tesseract kinda thing where the shifted puzzle starts as the inner cube and then shifts around like the gif below![[1686b99449a18084.gif]]
## February 5, 2026
### Week 5 Goals
- Explore other mechanics that can flesh out one of the possible branches of difficulty the base mechanics of the game can take on
	- I want to get wacky with it, really letting the themes of the game come through and integrate with the narrative
- Developing the rough form of the narrative to help inform puzzle progression and other mechanics
- More 3D asset generation
### 2D Terminal Shaders
Finished off last week by doing some 2D visual upgrading, and I got a CRT shader on it today to make it feel more like the terminal it's supposed to be on. Looks a bit better on video, but I'm still tweaking the shader, maybe gonna use a different one for some more control. Definitely gonna change colors too.
![[Screenshot 2026-02-11 at 9.39.34 PM.png]]
# Week 4
## February 4, 2026
### Week 4 Progress Report
#### Week 4 Goals
- Many a puzzle created
	- Creation of 3D puzzles to test varying levels of mechanics integration.
	- 2D puzzle creation
	- Testing these, changing/adding mechanics if needed
- 3D puzzle visual rework for dither postprocessing
	- Mostly to look at how the "wireframe" look of the puzzles will work in the shader stylization
- 2D puzzle/terminal assets integrated with 2D puzzle

I spent a lot of my time this week actually preparing the testing and not testing, which was a bit annoying, but I do think I got good test feedback from this week. The visuals rework hasn't been implemented yet, but I am glad I didn't fully integrate it since I got some good feedback on how to make it more effective from testing. Also same with the 2D puzzle assets. No unexpected events, just the constant cycle of creating and fixing, but mostly fixing.
### 2D Puzzle Visuals
For the node sprites and node connections, I decided not to make full sprites for them, since they're just circles and lines, which I can write in the code. That'll make it easier since I wont have to worry about all of the settings to make imported assets look nice. I can focus more on the shaders to give them a more stylized look. I put the dither shader over the 2D puzzle just to give it more of a look, but it's definitely just a placeholder. I also added a border on the line connections to make then have more depth.
![[Screenshot 2026-02-04 at 9.53.01 PM.png]]
### 3D Puzzle Path Visual Rework
To help distinguish the puzzle paths, especially on the dither shader, I'm going to give them a bit more of an emissive shader to help make them pop in the shader, as well as reduce the emissions and saturation as the paths get further from the camera to help distinguish depth on the puzzle. They can look fairly flat at the moment in even lighting and it doesn't help that they kind of disappear in the shader at the size I've been testing them at.
### UX/HX Testing I
#### Player 1
The first play tester is someone who mostly does 3D work, though plays a decent amount of video game, mostly PC games and older XBOX games. They spent most of their time playing the 2D puzzles, trying to figure out the strategies to solve the the untangling puzzles. They were able to solve the puzzles fairly quickly, preferring the puzzles to be harder. They wanted to see more mechanics in the 2D puzzles that would limit player movement of the nodes, like certain lines that couldn't be crossed by the nodes.

For the 3D puzzles, this play tester also spent a decent time trying to figure out strategy for the 3D puzzles, but found that there wasn't really a set way to solve the 3D puzzles and that they are more open ended. This player wanted to see more juice on the 3D puzzles and thought it would deeply aid the feel of the puzzles. They didn't have much time for some of the mechanics test puzzles, and as they were leaving pitched that I should make a mechanic that has a puzzle cube inside of the regular puzzle cube to solve at the same time, which is very similar to the shifting ability already in the game.

#### Player 2
The second play tester is a game developer plays games on PC mostly. This play tester only played the two harder 2D puzzles I had prepared, and warned against over saturating the game with the 2D puzzles, which should be fine with how the puzzles are planned out currently. This player got stuck on the 2D puzzles in a place that I also saw other play testers get stuck at, but maybe a bit more than others. When nearing the end of the 2D puzzles, a lot of times there's two intersecting connections and to solve the puzzle, the player has to move a lot of nodes from one side of that line to another. This play tester needed a bit of push to get past that hump. Example on a simple puzzle below:
![[Screenshot 2026-02-04 at 7.25.24 PM.png]]
The player spent some time on the 3D puzzles, but mostly in the base 3D puzzles. They found the puzzle movers' physics felt strange. They thought they were not responsive enough and that they too slippery on the paths. Though they liked the control scheme for the game, they felt the feedback from the puzzles themselves were a bit lacking for what input you put into it.
#### Player 3
Player 3 is a visual artist and plays games, mostly with controller and not fast paced games. Player 3 found the 2D puzzles fun at higher node count and was able to solve fairly quickly. There was a bit of difficulty in the smaller 2D puzzles though. When they decided how to move nodes when starting 2D puzzles, they would usually try to group nodes that were separated by seeing what node connections were the longest. As of now, the controls of the 2D puzzles are only on mouse and keyboard though they made a suggestion for how navigation on a controller could work. The main way of selection would be a cursor the player could move around the screen. To select a node, the player presses a button and the node can be moved around. The player suggests that the controls should allow for a player to "tab" between the connected/surrounding nodes to move next so they player doesn't always have to deselect and select another node when placement of a node is finished.

This player spent most of their time with the 3D puzzles on the puzzles with the shifting ability. They liked the amount of rails on the puzzles with the shifting ability and thought that the ability itself was meaningful to the overall progression of puzzle mechanics. They felt that the portals on the puzzle was a bit lackluster and didn't provide much to the puzzle in it's current use case. They liked the idea of having a puzzle that wasn't completely connected and required the use of portals to move movers across those gaps to complete the puzzle. 

Visually they felt both puzzles were flat in their current state, and would benefit from some kind of visual depth. They felt the 3D puzzle paths should have a loss of saturation as their depth became more from the camera. They also think more stylization of the paths could help with distinction in the paths. They got confused at points in the 2D puzzles about what nodes were connected, and think that distinction of connection though outlines or other depth indicators on the lines would help. In its current state, the puzzles use flat colors to say whether the connection is tangled or not and the nodes are also square shaped, which can cover connections up when connections are grouped together.
#### Player 4
Player 4 had some experience from playing the game, but mostly observed. They think that I should be careful with how much the 2D puzzle is used in the game, especially since the 3D puzzle is the puzzle system that utilizes more interesting mechanics. I think their concerns are valid, though I do want the 2D puzzles to, at some point, become extremely overwhelming to give a sense of anxiety. They think that having the 2D puzzle retangle as the player goes through the 3D puzzle would help with that experience.
#### Player 5
Player 5 is Danny. I've been wanting to test the new control scheme I have with him for a bit now, and I'm glad to say that he does like it. He didn't grasp that doing the joysticks in opposite directions would rotate the puzzle in a different way until I told him, so I definitely need to make that more apparent in game when tutorialization happens. For other terms of tutorialization, Danny sees a good path for introducing controls and mechanics of the 3D puzzles, first introducing basic rotation, then the opposite joystick rotation, and then other mechanics. He mentioned plenty of ways I could take the 3D puzzles in their mechanics, either through adding new ones or revamping ones I already had. He said that it was good there was a lot of ideas being developed for other mechanics; that it was a good sign that there was a good base interaction going on with the puzzles, which I was happy to hear. He thought that the 3D puzzle that had a lot of paths and all the mechanics added on to it was good, but was also certainly a later game puzzle, which is reciprocated in my designs. 

To add on to creating the experience of inducing anxiety in the player, he suggested leaning into subverting the player through mechanics and changing things about the puzzle that the player had already gotten used to. He added on to what Player 4 said about the 2D puzzles retangling as the player solved the 3D puzzle, saying that when the player goes back to untangle the 2D puzzle, the puzzle could shift gravity, flip axes, or something of the sort to throw the player off balance.

He was a big proponent of adding juice into the game, which of course it doesn't have too much now but he certainly through out great ideas. He wanted the movers on the path to have an audible element to them, where the movers would have different sounds depending on the angle the path they were on or their speed. He also wanted the movers to make sounds when they hit the end of a path and make a sound when they went past an intersection as well. He threw out that there could even be a puzzle that was just sound based and you have to solve the gravity 3D puzzle just through sound, but I don't think I'll be doing that. He also wants more easing in the movement of the 3D puzzles to help with the idea that the object has more mass.  As for juiciness in the 2D puzzle, he thinks that the nodes of the puzzle moving around, maybe even more erratically as the puzzle progresses would be good.

He thinks that the game has "good bones" though, which I feel like is a good description of where the game is. He was telling me how some of the best puzzle games have a kind of branching difficulty that the player can choose and that it's good to explore those, but since this project is going to be more like a very integrated demo at the end of capstone that I should try and focus on one of those difficulty paths and really hone that in. Being able to hone that corner of what the game could be would be a good place to get the project to for capstone, and flesh things out more fully afterwards. Pretty much making a vertical slice for what the game could become.

#### Summary
I heard a lot of what I'd heard for the game before about controls and mechanics, but I did hear some new problems with things, get new solutions, and got quite a few ideas on changes that could be made. I got good reinforcement on how the controls felt and, for the most part, on the base mechanics of the puzzle. I had some worries about the portals not being meaningful enough for for the gameplay, and that was true, but I got good insight in how people would like to see them used in gameplay. I had some worries about the time dilation path effect, but it seemed to be a lot more solid than I thought it was for the gameplay; it was useful in helping solve the puzzles by kind of holding the mover in place for a bit and let the player move the other mover around for a bit to get it where they wanted it to be. There was good feedback on how the game could feel better through mechanic tweaking or adding new things as well. Got a lot of feedback on what other mechanics could work in this puzzle system from Danny, and I definitely want to explore what I could add/change in the game to make it a but more funky, without adding too much to the workload of it all. I want to try and start on more puzzle progression for the 3D puzzles, seeing how adding on mechanics will feel as the player progresses and how that actually feels to do in order. I definitely want to explore the 2D puzzles more, as I think that making them a bit more interesting could be good, but again, they are supposed to be the anxiety mechanic at some point so they can't be too enticing. I'm happy with the feedback on what I've done so far; it's gave me good insight on what works, what doesn't, and what can be added and it's also been a good morale boost to see people play it and give generally positive feedback.
## February 2, 2026
### 3D Puzzle Mechanics Test
To test the mechanics and how they compound on each other, I'm placing the mechanics on a copy of the larger, low density puzzle I'm testing for the base puzzles. I want to have the base puzzle be more of a control, since I'm more interested in how the mechanics work together and how they matter in context of the puzzles as a whole. For the Mechanics test, I took the first bigger, low density puzzle and put some portals on it. To test the shifting ability, I created two new puzzles that were larger, but also had a smaller amount of rails. Each of the puzzles had a single moving piece and a single goal point. The player then has to shift between the two puzzles to solver both puzzles simultaneously. I deemed it was too hard to do with more than 1 mover on a puzzle at a time if it was being shifted.
### 3D Base Puzzles
To test the 3D puzzles in their base state, I created a larger puzzle that has a lower density and a smaller puzzle that has a higher density of rails. The two have about the same amount of rails, but play a bit differently in size on screen and how fast it takes to get the follower around the puzzle.
### 2D Puzzle Tests
For testing 2D Puzzles, I've created 3 different puzzles that I see as easy, medium, and hard. I've, of course, been handing this puzzle for a bit now, so I'm fairly used to the mechanics, so I'm interested to see how the difficulty of these puzzles is for someone who has little or no experience with this kind of puzzle. I'm able to solve the 'hard' puzzle fairly quickly at this point in a time that I think would be maybe a bit too short for the game, but if done by someone who hasn't been messing with these puzzles could be a good time. Or maybe too long. But we shall see.
## February 1, 2026
### Course of Testing

| Test Material                                                               | Things to Test                                                                                                             | Things to Look For                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| --------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Base 3D Puzzles at various sizes and density of rails                       | Puzzle Mover Feel; General Feel                                                                                            | - What size do people like<br>- how does rail amount effect difficulty<br>- what rail formations do people like/not like; reactivity<br>- does a cube formation feel good<br>- size or rail density change for progression?<br>- Does this core mechanic of moving separate movers to different locations feel good<br>- Should movers have to go to specific points or should player have more freedom of where movers should go<br>- Movers visible enough in 3D space, if not how can depth more be represented. |
| One puzzle per compounded puzzle mechanic(Portals, Redshift, Time Dilation) | Combination of puzzle mechanics; how mechanics work together; Time to Complete                                             | - Does progression feel good<br>- do mechanics feel meaningful in the puzzles<br>- does it feel like enough puzzles<br>- see if other ideas for mechanics could be good to add or replace other mechanics                                                                                                                                                                                                                                                                                                           |
| 2D Puzzles with varying amounts of nodes                                    | Puzzle difficulty increase; scoping if just node amount increases difficult or if node placement matters; Time to Complete | - What node amount is a too overwhelming vs what is too easy<br>- Do people want more mechanical things at work<br>- Does it feel like a good contrast to 3D puzzles                                                                                                                                                                                                                                                                                                                                                |

## January 29, 2026
### UX/UH Testing 1
- Most testing is going to involve both 2D and 3D puzzles in usability interviews with varying game familiarity in players.
- Testing UI and visual elements
	- This is mostly to make sure the postprocessing(dithering in 3D/CRT filter in 2D) is readable and playable. Also testing this to get feedback on if the vibe people get from hearing about the game matches the visual style.
### Week 4 Goals
- Many a puzzle created
	- Creation of 3D puzzles to test varying levels of mechanics integration.
	- 2D puzzle creation
	- Testing these, changing/adding mechanics if needed
- 3D puzzle visual rework for dither postprocessing
	- Mostly to look at how the "wireframe" look of the puzzles will work in the shader stylization
- 2D puzzle/terminal assets integrated with 2D puzzle
# Week 3
## January 28, 2026
### Week 3 Progress Report
My goals for this week were: 
- Puzzle Mechanics Implementation for 2D and 3D
	- Test in Parallel
	- Document for Puzzle Progression
- 2D/3D Asset Creation
	- Base Level Lighting and Post Process Shaders
	- Focusing on environment and 2D terminal assets
I was pretty happy with my time management, although I wish there were a few more hours over the weekend. Fridays-Sundays keep being week days for my progress. Feedback was big for refining the controller inputs for the game, I think that with a bit of tweaking will feel great. I had input on the 2D and 3D visuals as I developed them which was nice. Didn't get as much time in on 2D stuff as I wanted, but I do think that the 3D puzzles need more attention currently.
### 2D Puzzle Visuals
The 2D puzzles take place on a terminal in the test chamber. I want it to have a CRT like overlay, which I've implemented in Godot before, so I know that I will be able to do that. I already have the 2D puzzle mechanics mostly figured out, so texturing them shouldn't be too difficult, just mostly switching out the placeholder sprites I have, placing other static 2D assets, and some shader magic. In the final iteration, I want to have a moving blackhole shader or video in the bottom right, either if thats a shader or a looped video made in Blender.
![[GdDMvQAAAAZJREFUAwDRWVeWp3FdTwAAAABJRU5ErkJggg.png]]
### Visuals In Engine
To get a styling down for the 3D assets in the game, I wanted to make sure it would match the dithering post process that I would have setup for the game, so I added a rough post process filter to help guide what the 3D assets would look like. The [post process shader](https://github.com/Donitzo/godot-color-dither?tab=readme-ov-file) is a fairly simple dithering effect that is build for Godot by Donitzo. Along with the shaders is a dither palette generator that takes an image of 2-16 colors and outputs an image mapping those colors to dither noise. Along with the dither post process filter, I also configured Godot's real time lighting features. The two come together to create a colorful, but dark visual, matching the dark, cybery visuals I wanted for the game(Dithering might be a bit distorted from Screendoor effect if the images are not viewed at a larger size). The first image is of the test chamber where the 3D puzzles are held and solved; the second image is of the room the player is in for the game. The red panel on the back wall is to be a placeholder for the terminal the player will interact with for information and to solve the 2D puzzles.
![[Screenshot 2026-01-28 at 8.32.32 PM.png]]
![[Screenshot 2026-01-28 at 8.40.55 PM.png]]
### New Path Effect
Worked on one of the other path effects that I want for the puzzles(currently the last one that has to be made). The effect is time dilation, which effectively just makes the acceleration and speed of the puzzle mover less. When making the system for how the puzzle movers were supposed to move, I had this effect as an idea, so I luckily had the foresight to make it very easy for the component of the effect to reduce the acceleration and speed of the mover when on the path, and return it to normal once off the path.
### Control Testing Cont.
Tested the new controls I have with some more people today with varying levels of "gamerness". I first tested with my roommate, who has put a lot of hours into games, but by that I mean it's mostly 4000 hours in The Sims on PC, so she does have a bit less experience on controllers. She's certainly used one before, but mostly for the occasional Mario Kart. I handed the controller and just told her to use the joysticks and figure out how to rotate the puzzle. She figured out pretty quickly how to rotate just using a single joystick, but it took her a second to figure out how to rotate the puzzle clockwise/counter clockwise by doing the joysticks in opposite directions. After she had figured that out, she was able to use the controls comfortable. A second test subject is also more of a PC gamer with mostly hours in competitive FPS games and Minecraft. I too told him the same instructions of just figure out how to rotate the puzzle with the joysticks. He too easily picked up simple rotation and took a second to be able to rotate with opposite joystick movements. A question I've asked everyone after testing these controls is if they are able to imagine a way they want to rotate the puzzle, are they able to without resistance on these controls. Everyone has said yes. I'm happy to say everyone has felt very comfortable on this new control scheme, with a few of the people also being able to try out the old control scheme and having dislike for it. There's some tweaking that can be done on the movements that can be made, but overall I think that the controls are very intuitive based on the responses from everyone who's tested these controls.
## January 27, 2026
### Restructured Point Effect(Portal)
I had started adding in a point effect for the puzzles that would allow for a portal to teleport to other parts of the puzzle. I had gotten a bit stuck on it, in my attempt to make a streamlined way to add the effect to the puzzle. I had mostly gotten stuck on the actual adding of the effect to puzzle as well as linking up paths on the puzzle so they effect could work and not actually ever really getting to the effect itself. I was trying to make a fairly complex setter function for a few variable I had, and it was just being annoying with how Godot works under the hood. Fortunately I have friends smarter than me. I was working with my friend who knows Godot fairly well and he suggested to not do the complex setter function and just check if the set variable exists and utilize it in the exact way it was being used in the setter but only when it was needed. This of course worked. I don't really know why I didn't think of just performing operations on a variable when I needed it instead of when the variable is set in the editor. Maybe I was just so set on having a cool lil setter function that ran when I set the variable. But Occam's Razor prevails.
### Portal Effect
After passing this annoying issue of setting the needed variables for this effect, the effect itself was fairly easy to setup. On any given path on a puzzle, you can attach a resource that represents a portal on that path. In that resource you can select another path in the puzzle as well as either endpoint of the path as a location for the portal to teleport to. Then, while the game is running, it checks 
## January 26, 2026
### Newwwwwww Controls
I've been working on my new control scheme for my game, and have it in a working state today. Tested it with some folk, who found the controls initially confusing, but once gotten the hang of, felt a lot more fun to use than controller axes being transposed to specific rotation axes. The control scheme is a bit similar to Katamari's controls. You can use both joysticks pointed in a direction to roll that direction. I'm also testing being able to point just a single joystick to be able to rotate the puzzle. Like in Katamari, as well, you can do the joysticks in opposite direction in the up and down vectors to rotate the puzzle. In the video below, you can see the joystick movements and the corresponding movement of the puzzle.
![[Screen Recording 2026-01-26 at 3.24.52 PM.mov]]
I intend to test these controls with people who don't have as much familiarity with gamepad controllers to see how they feel the controls work. I think the controls are not necessarily intuitive with how controller joysticks are usually used, but make sense in how they affect the puzzles rotation in its own context.
## January 22, 2026
### Week 3 Goals
- Puzzle Mechanics Implementation for 2D and 3D
	- Test in Parallel
	- Document for Puzzle Progression
- 2D/3D Asset Creation
	- Base Level Lighting and Post Process Shaders
	- Focusing on environment and 2D terminal assets
# Week 2
## January 21, 2026
### Level Blockout
My time today working on my capstone was mostly of the blockout of the room the player is inside of for the duration of the game. It's a pretty simple 2 room test chamber where the player is in one side looking into the other room, where the 3D puzzle is they must rotate to solve. Shapes are very simple and I used some placeholder materials to give an idea for color and lighting of the environment, though everything I used will eventually be replaced.
![[Blockout1.png]]![[Blockout2.png]]![[Blockout3.png]]![[Blockout4.png]]![[Blockout5.png]]
### Week 2 Progress Report
My goals for this week were: 
- 2D puzzle design and testing
	- Would like to get implementation started in engine by the end of week 2 as well to show for presentation. Definitely ideal condition.
	- Do testing before it's implemented in engine, since who knows how far that will actually get in engine.
- Blocked out level
	- Simple greybox in engine
	- Maybe some fidelity since it's a fairly simple room layout
- Keep testing and iterating on puzzle effects and abilities

I got all of these done luckily. Very happy to have gotten the 2D puzzles implemented in engine. Spent a lot more time on capstone this week, which I'm happy with. I did give myself a bit of a break over the weekend, which I don't want to do every weekend, which will help spread out my work a bit more over the week. I spent a majority of my time working on last Friday and Tuesday, with only a few hours spread through the other days of the week. I definitely hit more than 12 hours this week, but I don't think it's sustainable to pack my workload vertically on only a few days a week.

Main integration of feedback is definitely on the controller input. It still has a few kinks in it, but now that I know it's what I naturally want to do with the controller to rotate the puzzle, I have high hopes for it. Gonna keep chugging on puzzle mechanics and design to keep that testing rolling.

The time to make some of the things I made definitely exceeded my expectation of time, but it's just prepared me to make sure I give myself the time to do the things I need to do. I'm fine with spending the time on this, but I want to be able to be more efficient with the time that I do use. Though with the more time I spend in engine, I'll be able to sniff out the bugs more easily, so just gotta keep going. Overall good time spent on capstone, and I hope it's a good foundation for things to come.
## January 20, 2026
### Controls cont.
I've gone through much strife today. Before that, I forgot to finish off talking about the new controls I wanted to implement yesterday. Started using quaternions to do the new control scheme, which seems promising. They're weird math things, but on the most basic level, they have two components: a 3D normalized vector that points away from the object's center and an amount of rotation around that axis. I'm heavily simplifying that, if that's even what they actually are. Either way, the controls of it are half baked, but I think with some smoothing out of the code it'll work well.
### 2D Puzzles Implementation
I spent most of my day implementing the 2D puzzles into engine to be able to show them for Iteration 1 this Thursday. It took so long and I had problems that were annoyingly simple to fix, yet the people of StackOverflow and the Godot forums, as well as my sludgified brain could not come up with solutions quick enough to fix my problems. I created a tool that lets me add nodes into my Godot scene, connect them through the inspector, and then save that setup of nodes to a file. Confusingly, I'm not exactly talking about nodes as in the Godot sense, but the "nodes" in these 2D puzzles are also represented by Godot's node system. ![[Screen Recording 2026-01-20 at 10.46.37 PM.mov]]The shown puzzle is fairly simple, but it showcases the basic mechanics of this puzzle and how it works overall. If you looks closely, you'll be able to see some of the nodes collapsing on each other. That's a byproduct of how the dragging mechanism of the nodes works and I'm just too lazy to fix it right now(but I know how to :)). Luckily I'm not too lazy though; you can see the lines in between the nodes flicker in the video above, but I just thought of a simple method change I had to do to get rid of that. I'm happy with how it turned out, despite how many issues I had with it.

My biggest issue was with the Resource data type that Godot has. They're really useful and cool, but there's just a few esoteric things that the documentation decided to hide away in places that were terribly difficult to reach. 
	I'm not one to usually use AI for my projects, and I even resorted to that to fix my problems. It still only managed to get me closer to my solution, but it honestly didn't feel like it did a whole lot to really help. It failed to give any reasonable answer that worked and in its rambling of solutions that failed to do anything, I at some point had an idea about what could work. 
In Godot, pretty much everything you see on your screen in game is represented by a node that is held in the Godot node tree. Sometimes you don't need something to have that "physicality" in a game space; it doesn't need to have a position, or a hierarchy with the other things in the game, etc. At that point you pretty much just need to hold data in some way, which is where Resources are really handy. They store data in the base engine, like 3D model Materials, images, sounds, and many other things. You can also create your own Resources, extending from the base Resource class, which is what I did. I made a new Resource class that stores the positional data of all of these nodes as well as their connection relationships. I have a scene in Godot that is able to read these Resources, generating the nodes where they need to go and how they connect. That scene also lets me add new nodes to the Resource, change the connections, remove nodes, and connections, then allowing me to save that Resource again to my disc. Makes a really lightweight way to store the puzzles that's still easily accessible.

My problems arose mostly in the saving of the Resources. Sometimes it wouldn't save to my disc, but stay saved if my editor was open, sometimes the resource would disappear when I ran the game, and sometimes the Resources that I had just replicated each other, making multiple copies of the same puzzle. Luckily I have a friend who has had some of these same issues that I had today, sometimes I was lucky to find someones solution on the Godot Github Issues, and one time I just tried a combination of things I was pretty sure I had already tried and it fixed everything. 

I spent most of time on that set of tools that let me create the puzzle, which is kind of annoying cause I spent most of my time not making the puzzles which felt like a very bad method of prototyping, but these tools will let me iterate on puzzles faster, especially since I think this is a good base for the 2D puzzles for this game. Maybe I'll just make a game of only inspector tools one day, could be good.

## January 19, 2026
### 2D Puzzles
Last week broke my brain a bit, so I had to take a good break over the weekend with work and general consumption of media. I spent a lot of time last week doing that too, perhaps you could call it procrastination, but after that break, I'm feeling much better(less brain melt) about working on this project. I'm starting today by designing my 2D puzzle system. This puzzle system will be fairly prominent in the game, the same amount as the 3D puzzles, though the 2D puzzles will rely more on complexity to increase difficulty, rather than introduction of new mechanics to increase difficulty. The point of the 2D puzzles is to eventually overwhelm the player with complexity using a simple mechanic to simulate a sense of anxiety.

I want the 2D puzzles to be line connecting/pipe connecting puzzles. My original inspiration are the puzzles used in [The Witness](https://www.youtube.com/watch?v=Mj3nCfB64AI), though they introduce mechanics to increase difficulty, as well as increase complexity overall, which I think would be overwhelming if I did with the 3D puzzles also bringing in new mechanics. I know I said I want the player to be overwhelmed, but I think that bringing in new mechanics for both the 3D and 2D puzzles would be overwhelming to a point of wanting to not play the game. 

I was pointed to Rusty Lake's Cube Escape point and click puzzles for some inspiration of line based puzzles. In their game *The Cave*, they have a puzzle where the player must "untangle" some nodes that are connected together([Puzzle in Question](https://youtu.be/d80AQGv7BfE?t=481)). It's a fairly simple mechanic, but has the ability to be made more complex by just adding more nodes together. I think it also has some linkage to the game's themes, specifically through the black hole device the player uses throughout the game. Though it certainly isn't how it actually works, the tangling of the nodes reminds me of quantum entanglement by name, and it has a relation to black holes, at least through a a thin connection of quantum physics. Of course this is a game, and things don't need to be necessarily explained through true physics, but some theoretical studies have show that entangled particles keep their entanglement, even in black holes, which I could use as the rough explanation for the device the player uses works.

How that puzzles works is: You have a certain amount of nodes on the screen that are connected to a certain amount of other nodes in the puzzle(Not sure if it's relevant to the puzzle, but in *The Cave*, each node is connected to at least 3 other nodes). The puzzle starts with multiple of the connections overlapping each other. Your goal is to arrange the nodes so that none of their connections overlap with any of the other connections.

I like the contrast this puzzle would provide to the 3D puzzle I already have. Both of them are logic based to an extent, but the 3D puzzle has the fairly freeform(solvable through various ways, slightly more skill based) object management through physics and this Cube Escape puzzle is a more strict solve of object management through their physical connections. I want to have some separation from the Cube Escape puzzle so it isn't the same puzzle exactly, besides visual wise. I also don't want to introduce too many more mechanics into the 2D puzzle, but I think if I were to add a mechanic and keep it consistent in the 2D puzzles, that would be ok.

### Testing Today
I had someone test my game today, mostly about the feel of the controls and the puzzle physics. They found the physics of the puzzle felt a bit sticky/un-responsive. When they rotated the puzzle, they felt like it took too long for the movers on the puzzle to begin moving, which they felt like they had to anticipate when they were rotating the puzzles, which they didn't like. As for the controls, they forgot to use the triggers to rotate the puzzle. Even after remembering they could use the triggers to rotated the puzzle, they often only used one of the triggers on the controller, almost completely abandoning the left trigger on the controller, which is operated by the same hand that also operated the left joystick(possibly overwhelmed by the amount of controls on left hand and underwhelmed on the right hand with a single trigger to press). They felt like they wanted to use the right joystick in some way to control the puzzle, even if it was just to zoom in on the puzzle.

### New Controls to Test
I like the idea of using both joysticks to control the puzzle, especially if both axes were usable to rotate the puzzle. I have this idea in my head about using both of the joysticks, though I can't remember if there's some precedent that uses it that I can actually base the controls on. The idea is to have each of the joysticks control one of two control points on the left and right of the puzzle. This sounds a bit strange so I have a physical example to imagine:
	Imagine you have a globe in front of you. It stays stays stationary in its translation, but it can be rotated. You can rotate the globe with your hands, but try to imagine rotating the globe with your hands pulling in different directions. If you were to pull the globe downwards with both of your hands, the top of the globe would rotate towards you, as a simple example. But if you were to pull up on the globe with your left hand and down with your right hand, the the top of the globe would rotate downwards to the right, around the z axis, if x is left and right, y is up and down, and z is backwards and forwards.
I'm trying to think of how to implement this at the moment, but I'm having trouble with translating the 4 linear axes of two joysticks into the 3 axes of rotation. I think there may be some kind of answer in the transforms of the objects: the matrices that represent the rotation of an object in space. Maybe the answer is in the example I gave of rotating a globe with your hands; I can try and think of rotating it in terms of pulling vectors on the outside of the puzzle, not just vectors acting on the origin of the object.
## January 16, 2026
Went back into working on some of the components for the puzzles. I tried to add portals that can be placed on the puzzles to allow for the puzzle moving pieces to teleport across the puzzles. I had started to add ways to add portals onto the puzzles on the 15th, but didn't finish it; was trying to make a system at 1 am and felt my brain melting from the lack of glucose it had so I had to stop. Today I resumed the system, having to start from scratch after making a mess of logic the night before; it was terribly cyclical and didn't make sense, overcomplicated in a lot of ways too.

I spent a lot of the work on the puzzles today fixing the logic of attaching the portals to the puzzle as well as the logic that connects them, letting the portals reference each other. Logic to make movers go through isn't completed yet, but should be fairly easy to add with what I have. Not too happy with how much time I spent on the tools of the mechanic and not the mechanic itself, but what I did make will make using the portals so much easier down the line, especially adding them to multiple puzzles. I really want to stay away from hard coding as much as possible, and using this component system is certainly going to help greatly with that. This is my first time utilizing a component system in a game, so I'm getting used to how they work, but I think it going to greatly benefit my game overall, especially with speed of iteration on puzzles.
## January 15, 2026
OMGGGGGGG Iteration 1 next !!!! so exciting . 

### Week 2 Goals
- 2D puzzle design and testing
	- Would like to get implementation started in engine by the end of week 2 as well to show for presentation. Definitely ideal condition.
	- Do testing before it's implemented in engine, since who knows how far that will actually get in engine.
- Blocked out level
	- Simple greybox in engine
	- Maybe some fidelity since it's a fairly simple room layout
- Keep testing and iterating on puzzle effects and abilities

--- 
# Week 1
## January 14, 2026
For work on my game, I mostly started implementation of being able to add components to specific rails/tracks on the puzzle. This allows for specific effects/abilities on certain parts of the puzzle, rather than the whole puzzle. The components will work fairly similarly to how the whole puzzle components work, but unfortunately I've ran into a problem with the engine in a tool script I was creating to make adding components easier. I've got a friend who luckily has had this same problem and is going to send me his solution tomorrow. I know how the rest of the system will work once that is resolved.

My goals for the week were:
- Component system to attach abilities/effects to paths/path points
	- At least one ability/effect to accompany, but want to have 2 or 3
- Test component system as it's constructed as well as for general feel for game
	- Continuing controller input and how it feels, especially if more buttons are added in for abilities/effects
	- Going to try and set up pipeline to share builds digitally with people to allow them to simply download an .exe from a file share link to test the game.
- Ideation on visual styling for visual redesign
- The framework that the abilities that don't exist on the puzzle will exist
	- How will the time manipulation, redshift/blueshift, and spaghettification work

I made good progress on the component systems for the game, giving good leeway for testing the mechanics of the puzzles this next week. I'm not too happy with how I spent my time this week; I watched all of the first season of The Pitt and the newest episode out, which was great, but I really could've put more time into this to get further than I am now. I've set up a place in my apartment that isn't where my desktop is, hoping that I'll be able to be more efficient in a separate space more set out for work, which has been nice so far.

I worked with the controls of the puzzles a bit to try and make them feel better from the feedback I've gotten so far, but I think I need to do more testing on it. When ever I use the controls, I keep trying to use controls that I think will intuitively work with these rotation puzzles, but it's not how I have the controls set up. I'm not quite sure what controls I'm expecting should work for the puzzles when I do that, so I want to see what others have to say on that. No unexpected lessons, just the same old lesson of if you don't do things earlier, you've got more things to do later. One day I'll internalize that
## January 13, 2026
My original concept for the visuals of the game were comprised mostly of just pixelating the textures of the 3D models of the game and not doing too much on the shader side of things. Even for lighting, I was planning on just baking the lighting, so it was consistent but left it fairly flat. It kinda looked like Minecraft, which I didn't really like for this game:
![[TestRender1.png]]
Elsewhere in the devlogs, I mention a video from a GodotFest talk(https://www.youtube.com/watch?v=cfipwefB0Ac) which inspired me to take a different approach to my visuals. The visual style for Godot, developed by Antti Tiihonen, combines common techniques of game visuals into a more unique approach. Commonly you see games either using realistic lighting and textures or more low fidelity approaches using low quality textures/rendering with flat baked lighting. Tiihonen utilizes Godot's fairly complex lighting systems and combines it with a dithering shader, like how a retro game would appear with. This allows for textures to be fairly simple in their creation, using simple shapes as markers of detail, while still having a nice dynamic lighting that reacts to the world and still looks good in a lower fidelity resolution:
![[Screenshot 2026-01-13 at 8.37.29 PM.png]]
I really like his approach of this visual style, though there are multiple aspects I want to change to make it my own/work with my game better. I would certainly want to use a different color palette than he uses, and I almost feel as if the granularity of the filter is too much. I also want to use 3D models that aren't voxel based, like Tiihonen uses, which I think will show very differently in this style. The lighting is fairly dark in how he uses it, and I think a more sterile lighting would better fit my game, although I need to do some in engine tests first. 

This will greatly speed up my 3D asset creation as well, as before I was creating models in Blender, then exporting to Substance Painter to meticulously texture my models, then put a pixelate texture over that to create the style I wanted. The pixelating filter was often not consistent enough to make models look similar and every model I wanted to texture required a new Substance Painter file, which is just a pain in the ass. Using Tiihonen's approach, I could simply model in Blender AND do simple texture painting in Blender as well, greatly refining my 3D pipeline. 

I want the 2D portions of the game to take place with a monochromatic CRTish look. I really like retrofuturist cyberpunk aesthetics, and I think they work really well with the games themes. The 2D parts of the game are going to take place on a terminal in the test chamber that will be themed in this way, and having a monochromatic, or tricolor display would work well with that styling:

![[67f13efb9588ea2f2a2d213f7301f8d6.jpg|300]]![[e963b66200ba48a0cb2cb9a3dd7ac4e0.jpg]]
## January 11/12, 2026
Did some amazing procrastination of going to the library to work and then not feeling that environment, so I went to where I work my job to do work in the tea house there, but of course it was full, so I just talked to my coworkers for a bit and went home to watch half an episode of The Pitt. My resolve is truly unmatched. After that way too long of a time, I got to work on my project. 

My main goal for this week is to get get a component system working for my puzzles that lets me attach abilities/effects to each of the puzzles. This will let me stack these abilities on top of each other without worrying about too much conflict between the abilities. Also reduces the hard coding of everything, making everything a lot more modular and easy to work with. Though I also want to add effect components on the separate rails of the puzzles, I started with a component system that applies to the whole of the puzzle, rather than specific sections of it. These puzzle encompassing abilities are the main focus of mechanics chance for the puzzles, which is why I chose to work on it first. It's fairly simple at the component management level since there's only a few components and a handful of puzzles that will be used. 

The ability components that I want for a puzzle can be added to an array in the game engine inspector, which then the puzzle itself reads the abilities it has attached to it, executing the specific code per ability at the script level of the puzzle. Since the components are executed by the puzzle they are attached to, there isn't any dependency between the components. As of Jan 12, I have a component that allows for the player to "shift" the puzzle between two different puzzles while working on them at the same time.

### Shifting Ability Example
![[Screen Recording 2026-01-12 at 3.18.59 PM.mov]]

This is, of course, visually lacking, but allows me to begin to test the capabilities of this mechanic. I'm writing this almost immediately after finishing this mechanic, so I have not had time to test, but I will be shortly.

---
# Week 0
## January 9, 2026
I've spent my time today for the most part trying to set up this very devlog to show up on my Github website. It's showing up but being a bit squirrelly on showing up, I think it has something to do with the Quartz building that it's using. ANYWAYS, I also have to work on this project instead of procrastinating with things that relate to the project but aren't actually the project and with that I've got some goals to reach before next week:
### Week 1 Goals

- Component system to attach abilities/effects to paths/path points 
	- At least one ability/effect to accompany, but want to have 2 or 3
- Test component system as it's constructed as well as for general feel for game
	- Continuing controller input and how it feels, especially if more buttons are added in for abilities/effects
	- Going to try and set up pipeline to share builds digitally with people to allow them to simply download an .exe from a file share link to test the game.
- Ideation on visual styling for visual redesign
- The framework that the abilities that don't exist on the puzzle will exist
	- How will the time manipulation, redshift/blueshift, and spaghettification work

### Project Milestones Assignment
#### Project Name: **Heart of Darkness**

##### Elevator Pitch: 
A first person psychological horror game that aims to make players who struggle with anxiety and depression feel understood through experience-based gameplay. The player will solve a series of puzzles in the confines of an eerie test chamber under the watchful eye of a cyberpunk mega-corporation that simply sees the player as a means to the end. A device the player is given to test will begin destabilize both the testing environment and their own grasp on reality, guiding the player towards understanding what it is like to struggle with mental disorders.
###### 30% project complete mark
- Greyboxed puzzles implemented in Godot with current design(room for iteration through testing)
- Design/testing of 2D puzzles
	- Can iterate faster on these through paper tests since they don't have to exist in 3D space.
	- Plan for implementation in Godot and execute that if time permits(won't have too much visual fidelity since asset creation will come later down the line)
	- Noting what people understand about puzzles, what they don't, what would give them more insight on how the puzzles work, etc. Help to create a tutorial phase of puzzles and a visual language to help players understand how puzzles work.
- Level layout
	- Greybox of the singular 'test chamber' that the game takes place in
- New design for visual style
	- Mostly examples and plans for visuals, maybe a few examples of visuals if time permits

###### 50% project complete mark
- Visual redesign in engine with rough shaders and lighting 
	- Originally wanted this more towards the polish side of things, but with my planned visual redesign, the shaders and lighting will most likely inform how texturing will be done
- 3D/2D visual asset creation starts
	- 3D assets will most likely be simply textured with the current visual redesign plans. The shaders I plan on using will most likely hide finer details in models, meaning detail will have to be conveyed using more visible shapes on objects. 
	- Original planning had texturing done in Substance Painter, though doing basic shapes for detail on the textures can probably just done in Blender now, which helps refine the pipeline for the assets a bit.
	- 2D assets will involve text, which I will have to be careful about with the shaders. The 2D parts of the game might exist without the dithering. The 2D parts of the game exist on a terminal in the 'test chamber', so when the player interacts with the terminal, the game will probably fade to another 2D viewport of the terminal with visual effects for a CRT like screen, but higher fidelity than the shaders used in the 3D parts for text reading purposes.
- Implemented 2D puzzles
- Iterate puzzles through testing
- Start on music/sounds for the game
	- For music I would at least like for the main menu to have around a 2 minute long song on loop.
	- Game will rely more on ambient sounds than music for its psychological horror elements. I don't see music appearing much in the game itself.
###### 90% project complete mark 
- Asset creation finished
- Main mechanics of puzzles ideally finalized by here
	- Refining on numbers and feel will be main priority after this
- All sounds created and mapped in game. Looping music for main menu.
- Save/load features
###### 100% project complete mark
- Create opening menu and splash screen for the game
- Finalized puzzles
- Polished visuals
	- Cohesive colors and shapes through the shaders
- Logo/basic marketing material
	- I don't plan on selling this game, but I want it to at least have an itch.io page with decent visuals and styling
## January 6, 2026
Only a matter of days before the reckoning. In 2 days, the end of the beginning. At 9 AM will be the first Capstone Projects class. And I want to have organized what I have done currently and what I will start working on this Thursday! My time management over break for this project was god awful, but I needed a bit more of a break to make sure I wasn't gonna burn out too much. After my rest of watching movies and shows, listening to music, playing games, I'm ready to get back into this project. I want to make sure I have a good time management for this project, mostly because I'm kinda bad about doing work when I'm along, probably cause of that ol ADHD, but I want to give myself the tools and resources to keep myself accountable for this project and others.

### What I have:
- Rough Player Controller
- Visual Test Scene in Godot(Deprecated)
- Visual Test in Blender(Deprecated)
- Audio Test(Music) in Ableton
- Storyboard on "Gameloops"
- Puzzle Design in Progress(Done Over Break)
	- 3D shapes that the player manipulates to have a puzzle object follow the paths
	- Possibly using different shapes besides squares
	- Brainstorm on mechanics of paths, shifting towards abilities/effects that relate to blackhole:![[Screenshot 2026-01-06 at 1.50.33 PM.png]]
- Basic Mechanics of Puzzle Implemented(Done Over Break)
	- Moving puzzle object on paths
	- Giving abilities/effects on paths(WIP)

### Next Steps:
- <u>**ORGANIZE FOLDERS!!!!!!!!!!!!!!!!**</u>
- Playtest systems
	- Test control schemes for moving puzzles, currently using a joystick and triggers to control the 3 axes 
- Play around with basic layouts for puzzles
	- Puzzles that don't require the abilities/effects
	- Puzzles that help the player learn the base mechanics
- Create system to attach abilities/effects to rails
	- Maybe implement as player controlled, not just when on specific rail
- **KEEP TESTING AS THINGS ARE MADE**
#### Less Priority
- Visual Rework
	- I Like What This Guy is Doing  --> https://www.youtube.com/watch?v=cfipwefB0Ac
- Test Room Blockout
- Way to make puzzles in Blender
	- Was working on a way to lay out empties in Blender and then having a script in Godot draw paths between those empties. Currently not working because I'm detecting if a path can be drawn between empties with a raycast detecting empty space between those empty points, but the detection is failing at the moment