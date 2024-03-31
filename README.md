Mars Rover Kata
====================

Develop an API that moves a rover around on a grid

# Description

You’re part of the team that explores Mars by sending remotely controlled vehicles to the surface of the planet.
Develop an API that translates the commands sent from earth to instructions that are understood by the rover.

# Requirements

1. You are given the initial starting point (0,0,N) of a rover
2. 0,0 are X,Y coordinates on a grid of (10,10)
3. N is the direction it is facing (i.e. N,S,E,W)
4. L and R allow the rover to rotate left and right
5. M allows the rover to move one point in the current direction
6. The rover receives a char of commands e.g **RMMLM** and returns the finishing point after the moves e.g **2:1:N**
7. The rover wraps around ifit reaches the end of the grid
8. The grid may have obstacles. If a given sequence of commands encounters an obstacle, the rover moves up to the last
   possible point and reports the obstacle e.g **0:2:2:N**
9. Implement commands that move the rover forward/backward (f,b)
10. Implement commands that turn the rover left/right (l,r)
11. Implement obstacle detection before each move to a new square. If a given sequence of commands encounters an
    obstacle, the rover moves up to the last possible point, aborts the sequence and reports the obstacle
12. If Mars Rover goes beyond the grid size it should be placed at the beginning of the grid again

# Rules
1. Apply  TDD
2. Change roles (driver, navigator) after each TDD cycle.

## Examples

- Given a grid with no obstacles, input **MMRMMLM** gives output **2:3:N**
- Given a grid with no obstacles, input **MMMMMMMMMM** gives output **0:0:N** (due to wrap-around)
- Given a grid with an obstacle at (0, 3), input **MMMM** gives output **0:0:2:N**
