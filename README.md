Meteor Defense
====================

This is a program learn how to use vectors in a simple game.  The contest is to write a procedure that
shoots down a meteor.

Demo
------

(click to see video)

[![ScreenShot](https://i1.ytimg.com/vi/C3um6Djq4mc/mqdefault.jpg)](http://youtu.be/C3um6Djq4mc)


The Task
--------

The problem is a warm up exercise, mostly focused on getting used to programming the C-language.

The exercise is to write a procedure **targetArtillery()** that decides a how to shoot an meteor before it hits the ground.
The procedure is given the location of the artillery canon, and the meteor's position and velocity.
It computes how to shoot, by computing artillery's velocity.  When it has done so, it sets two global
variables with the results:

* *artillery_v_x*  is the x velocity to shoot
* *artillery_v_y*  is the y velocity to shoot

The procedure has access to the global state of the game, but it is not allowed to change any.  These
state variables are:

* *artillery_x0*  is the artillery's starting x position
* *artillery_y0*  is the artillery's starting y position
* *meteor_x0*     is the meteor's starting x position
* *meteor_y0*     is the meteor's starting y position
* *meteor_v_x*     is the meteor's starting x position
* *meteor_v_y*     is the meteor's starting y position


### Steps to solve the challenge

This is intended to be a straight-forward learn-the-language task, and how structure some of the relevant math
into it.  So this problem doesn't rely too heavily on deriving the equations -- but you're expected to work out
how to get them into the computer program appropriately.

It is too easy to dismess the pictures.  Do not.  They help break the problem down, make it easily solvable (or
at least, easier to solve), organize the information you need, and help reduce mistakes.

->!(Step 1)[step1.png "Step 1"]-<

The first step is diagram the basic event that is happening: the who's, the when's, and the where's.
The objective is to shoot an meteor before it hits the ground.  So the "who's" are a meteor and a bullet (which I'm
calling an artillery.).  The where's is the place they hit each other.  And the "when" is the point in time they intersect

Diagram the meteor's flight:
->(System Diagram)<-


->!(Step 2)[step2.png "Step 2"]<-

The next step is to describe the meteor and it's flight.

!(Meteor diagram)[meteor.png "The meteor's parameters"]



->!(Step 3)[step3.png "Step 3"]<-

Pick a time before the meteor will hit the ground.  In the simple challenge, the meteors never hit the ground before t=1.0.
So pick a time such as t=0.5 and intercept the point there.

1. Calculate where the meteor be at t=0.5
2. Calculate the vector from artillery starting point to where the meteor will be
3. Divide that t=0.5.  Why do we have to do this?  The vector says how far (and which direction) the artillery has to go, but not how long.   So we need to divide it by the amount of time it has to get there.




Requirements
---------------
The was created using the Xcode editor running under Mac OS X 10.8.x or later. 

