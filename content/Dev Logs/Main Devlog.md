---
title: Main Devlog
---
# Week 4
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