# Random walk 2D

To simulate and analyze various types of random walks on the lattice in the plane (all steps are
of the same length d = 1, but the direction is randomly chosen from a certain set of prescribed
possibilities).

1. Simple random walk on 2-dimensional lattice
   steps in any of the four directions  with the same probability.

2. Restricted random walk on 2-dimensional lattice
  1. without immediate returns
     steps in three possible directions with the same probability, the first step is in any direction

## Compile and run

Compile and run main program:

   gfortran .\random_walk_2d_main.f90 .\random_walk_2d.f90 -o .\random_walk_2d_main.exe
   random_walk_2d_main.exe

Compile and run test program:

    gfortran .\random_walk_2d_test.f90 .\random_walk_2d.f90 -o .\random_walk_2d_test.exe
   random_walk_2d_test.exe

## Decisions

TODO I decided to pass a random numbers as values to functions.
The reason is that it is more testable the generatei inside functions.
We can pregenreate random values
at the beginning of the program and then pass them down to procedures/fucntions.

I also decided to use type (structure) `position`.
The reason is that it better express a domain model and encapsultes `x`, `y` coordinates.

Can we determined trials and steps from random?

TODO function persistent_random_walk_2D(steps, trials) result() ... end function
TODO function restricted_random_walk_2D(steps, trials) result() ... end function
TODO Simple command line interface.
HOWTO Write an array to CSV like format?

## Reference
- http://utf.mff.cuni.cz/vyuka/NTMF021/homeworks/HW_task_1.pdf
- http://compphysics.github.io/ComputationalPhysics/doc/pub/rw/html/._rw-bs061.html
- https://github.com/jakehanson/2D_RANDOM_WALK/blob/master/main.cpp
- https://balitsky.com/teaching/phys420/Ph4_random.pdf
- https://blogs.sas.com/content/iml/2015/07/08/drunkards-walk.html
- https://blogs.sas.com/content/iml/2015/08/12/2d-drunkards-walk.html
- https://gist.github.com/rsnemmen/879cb5452effcf2d20a8f0041b8724e4
- https://cyber.dabamos.de/programming/modernfortran/random-numbers.html