# Rules

Similar to traditional Micromouse, MM3D allows competitors to make certain assumptions about the maze. These assumptions can be modified to change the level of difficulty for an event. With traditional Micromouse, one common assumption is the goal of the maze is in the center or a known location. This assumption allows competitors to implement search algorithms to find it rather than relying on chance. This is important for beginner and intermediate competitions where a robot may not be able to explore the entire maze and optimize a speed route in the allotted time.

For MM3D, allowing competitors to know the location and orientation of ramps beforehand helps to ensure their overall ranking won't be dependent on the random chance. Without these assumptions, a robots ranking may depend on choosing a left or right turn when little to no information is available for its algorithm to use.

## Pyramid Event

![](./../assets/images/pyramid.jpg)

The pyramid maze has multiple levels, each getting smaller with the goal at the center of the top level. Each level has one ramp in a known location and a known orientation. The locations and orientation of the ramps generally have some symmetry across the levels.

- First level is a grid of 10 x 10 cells
- Second level is a grid of 6 x 6 cells
- Third level is a grid of 4 x 4 cells
- Ramps are located along the opposite wall from where robots enter a level

[Here](pyramid.STL) is a 3D rendering of an example pyramid maze you can rotate and move around. In this rendering, all the walls you see are those which you can assume are present, except one wall outlining the goal.

- The starting location of robots would be on the lower level in one of two corner cells on the opposing wall of the ramp.
- The starting orientation of the robots would always be facing the direction of the ramp.
- The starting cell will have three walls.
- Ramps will always let robots out into a corner cell as seen in the rendering.
- Rankings are determined by the fastest run time from the start cell to the goal.
- Robots that do not make it to the goal are ranked by the lowest flood fill value of their current position when picked up by an operator. <strong>NOT</strong> the lowest flood value they achieve during the run, this is too difficult for judges to keep track of.
  - The entire ramp is treated as a single cell for flood fill rankings. Robots that are picked up on the same ramp are effectively tied with their final rankings up to the discretion of the judges.
- Robots have 10 minutes in the maze to perform as many runs as they want.

## Bridge Event

The bridge maze has two levels and two ramps. The second level acts like a bridge which must be traversed to reach the goal. The maze is configured in such a way robots are required to travel up one ramp and down the other to reach the final goal on the first level.

- First level is a grid of 10 x 10 cells
- Second level is a grid of 6 x 6 cells
- The goal is in the opposite corner the robot starts in on the first level
- Ramps are in known locations with known orientations

Here is a 3D rending of an example bridge maze. In this rending, all the walls you see are those which you can assume are present, except one wall outlining the goal.

- Rankings are determined in the same way as the pyramid event above.
- Robots have 10 minutes in the maze to perform as many runs as they want.