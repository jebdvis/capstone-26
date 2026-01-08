---
tags:
  - devlog
  - design
  - planning
---
Week 0 devlog! I am starting a series of devlogs as I work to keep track of my progress and expectations for my wondrous capstone game project. 

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
	- I Like What This Guy is Doing  ---> https://www.youtube.com/watch?v=cfipwefB0Ac
- Test Room Blockout
- Way to make puzzles in Blender
	- Was working on a way to lay out empties in Blender and then having a script in Godot draw paths between those empties. Currently not working because I'm detecting if a path can be drawn between empties with a raycast detecting empty space between those empty points, but the detection is failing at the moment