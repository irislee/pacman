From http://www.masswerk.at/JavaPac/pacman-howto.html:

1)	the maze has no dead ends (passages are connected at least at 2 sides)
2)	the pacman moves in straight lines
3)	if the pacman encounters a border, it stops
4)	ghosts move in straight lines
5)	ghosts never stop
6)	if ghosts encounter a crossing, the next direction of movement is evaluated
7)	ghost do not take opposite directions on crossings
(they will not reverse directly, but move in nested loops through the maze)
8)	if a ghost encounters another ghost both will reverse
(the pacman can't be there and ghosts spread out more widely)
9)	ghosts can evaluate their move
a)	based on random calculation
b)	based on strategic movement (get nearer to the pacman)
10)	movements of ghosts should be combinations of these
11)	ghosts should behave more strategic in higher levels to make them more difficult
12)	teleports: if a character encounters the absolute border of the maze, it is teleported to the other side.
13)	if a ghost encounters the pacman, the pacman's life ends
14)	the pacman eats any food it encounters in a passage
15)	if all food is eaten, the level ends
16)	if the pacman encounters a pill, the game is reversed:
a)	ghosts are in panic mode (half speed, strategic movement leads away from the pacman)
b)	if the pacman encounters a ghost, the ghost's life ends
17)	the reversed game ends after a short period of time and normal mode is acquired
18)	a pill is food
19)	a dead ghost travels back to the cage's entrance as eyes only.
20)	a dead ghost is revived in the cage
21)	there are 4 basic phases in ghost's life
a)	in the cage
b)	stepping out of the cage
c)	regular maze movement
d)	panic mode
22)	the maze setup varies from level to level
23)	if the last maze design is used, the next level reuses the first level's layout
24)	the cage and its door is placed on the same spot on every level-layout
25)	positions of teleports can vary from level to level (see rule 12)
26)	if the third pacman life is expired, the game ends
As we can see, there is much more to do for the ghosts, and the most definitions are about movements.

Some of these rules are general features of Pac-Man, while others are specific to our implementation.
For example the original arcade game lacks the rules 7 and 8, but has rules for scoring. Here we skip these additional rules in favor of a smaller download footprint and faster run time cycles.

To be strict, we had to define some additional rules concerning the display ....

In short we define:

27)	the pacman moves in alternating 3 animation phases in 4 directions
28)	a stopped pacman is not animated
29)	a ghost moves in 2 animation phases in 2 directions
30)	there are 4 ghosts in different colors
31)	a ghost changes color in panic mode
32)	a ghost changes to another color just before the end of panic mode
33)	panic and end-of-panic-mode color are the same for all ghosts
34)	dead ghosts homebound are displayed as eyes only
34)	the maze is defined by borders and passages
36)	border tiles can have 0 to 4 connections to other tiles
37)	a pacman life's end is animated as shrinking pacman in 3 phases
38)	a caught ghost is indicated by a single image animation
39)	levels are displayed in a level-display at the bottom of the maze
40)	player lives are indicated as pacman characters at the bottom of the maze
41)	the end of the game is indicated by a special "game over" display
