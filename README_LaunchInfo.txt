Build and Launch Project (in desktop terminal, not workspace default):
(If terminal states directory can't be found, just cd anyway)

TODO: Read Note 4) before launching project.

Launch Instructions:

sudo apt-get install libignition-math2-dev // fixes math.h errors, required every startup
cd /home/workspace/RoboND-DeepRL-Project/build
cmake ..
make
cd x86_64/bin
./gazebo-arm.sh

Notes:
1)  Clarification of contacts->contact(i).collision2().c_str():
    Udacity Project: Deep RL Manipulator SubLesson3: Point 6. might falsely imply that with the gazebo contacts function you can check whether
    a particular collision element (defined in URDF file) is involved in a collision.
    They simply gave a bad example of how they named collision element of link2 'collision2'.
    The function contact(i).collision2() simply returns the name of the SECOND collision partner
    (a contact(i) always consists two partners, collision1 & collision2).

2)  Collision Partners:
    There seems to be no way to find out which collision partner is which (e.g. why is ground plane defined as collision2?).
    However, a particular collision element is at least consistently either collision1 or collision2.
    Printing them is a way to find out whether it's 1 or 2.

3)  READ before launching:
    - building project in Udacity workspace requires GPU enabled.
    - sudo apt-get install libignition-math2-dev to fix error messages related to math.h
    - According to lesson, the project launches already without defining the hyperparameters.
      In that case, gazebo crashes shortly after launching though. Make sure to define some example parameters (not 0).
