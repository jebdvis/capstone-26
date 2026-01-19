---
title: Main Devlog
---
# Week 2
## January 19, 2026
Last week broke my brain a bit, so I had to take a good break over the weekend with work and general consumption of media. I spent a lot of time last week doing that too, perhaps you could call it procrastination, but after that break, I'm feeling much better(less brain melt) about working on this project. I'm starting today by designing my 2D puzzle system. This puzzle system will be fairly prominent in the game, the same amount as the 3D puzzles, though the 2D puzzles will rely more on complexity to increase difficulty, rather than introduction of new mechanics to increase difficulty. The point of the 2D puzzles is to eventually overwhelm the player with complexity using a simple mechanic to simulate a sense of anxiety.

I want the 2D puzzles to be line connecting/pipe connecting puzzles. My original inspiration are the puzzles used in [The Witness](https://www.youtube.com/watch?v=Mj3nCfB64AI), though they introduce mechanics to increase difficulty, as well as increase complexity overall, which I think would be overwhelming if I did with the 3D puzzles also bringing in new mechanics. I know I said I want the player to be overwhelmed, but I think that bringing in new mechanics for both the 3D and 2D puzzles would be overwhelming to a point of wanting to not play the game. 

I was pointed to Rusty Lake's Cube Escape point and click puzzles for some inspiration of line based puzzles. In their game *The Cave*, they have a puzzle where the player must "untangle" some nodes that are connected together([Puzzle in Question](https://youtu.be/d80AQGv7BfE?t=481)). It's a fairly simple mechanic, but has the ability to be made more complex by just adding more nodes together. I think it also has some linkage to the game's themes, specifically through the black hole device the player uses throughout the game. Though it certainly isn't how it actually works, the tangling of the nodes reminds me of quantum entanglement by name, and it has a relation to black holes, at least through a a thin connection of quantum physics. Of course this is a game, and things don't need to be necessarily explained through true physics, but some theoretical studies have show that entangled particles keep their entanglement, even in black holes, which I could use as the rough explanation for the device the player uses works.
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
	- Maybe some fidelity since it's a fairly simple room layout\
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