---
title: Main Devlog
---
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