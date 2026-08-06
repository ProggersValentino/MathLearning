[game math chp 3](https://gamemath.com/book/multiplespaces.html)

The reason we have multiple coordinate systems instead of one singular one is because certain information may only be able to be expressed or determined with a certain context applied to it.

### World space
This is the global reference to every other coordinate system that is located within the world. This establishes a "true" location that can be universally applied to all other coordinate systems. 

For instance, the location Perth in Australia is determined as the Western part of Australia relative to the center of Australia. However, globally taken from Greenwich England, it resides Eastern from the global origin point.

### Object Space & Camera Space
Object space is a coordinate space associated with a particular object. When its orientation and/or location changes, coordinate space associated to that object changes with it.

For instance, if I'm (the person) sitting at my desk and my monitor is directly in front of me then relative to me (being the object coordinate space) my monitor is 0.5m in north of me. 

But when I swivel my chair to the left by $100^\circ$ then everything within my coordinate space changes so now instead, the monitor is $100^\circ$ to the right of me at a distance of 0.5m or **0.5m east from me the object coordinate space**

### Upright space
Upright space is where it's location and rotation represent the in between of world space and object space. 

this is determined by the axis' being rotation to be parallel to the world space axis' and its location displaced to the origin of the object space:
![[Pasted image 20260706113053.png]]

This is space is very important for **translation** between world and object space, if this was done in reverse from world space to object space, then we'll need to inverse the process from adding the world space to subtracting it and inversing the upright basis vectors:

![[Pasted image 20260706113127.png]]

All the spaces allows us to manipulate objects between spaces to represent what we want to focus on for example, if we have a robot and a camera in a scene then depending on what context we focus on determines the perspective that object:


|                      | Absolute Perspective                 | Local Perspective                    |
| -------------------- | ------------------------------------ | ------------------------------------ |
| Robot Object space   | ![[Pasted image 20260706124320.png]] | ![[Pasted image 20260706124328.png]] |
| Robot upright space  | ![[Pasted image 20260706124348.png]] | ![[Pasted image 20260706124419.png]] |
| World space          | ![[Pasted image 20260706124435.png]] | ![[Pasted image 20260706124439.png]] |
| Camera Upright space | ![[Pasted image 20260706124452.png]] | ![[Pasted image 20260706124456.png]] |
| camera space         | ![[Pasted image 20260706124520.png]] | ![[Pasted image 20260706124522.png]] |
this represents two types of transformations being **active** and **passive** transformations.

The absolute perspective represents the **active transformations** where the coordinate space remains stationary but the objects (the points in the coordinate space) are moving around.

The local perspective on the other hand represents the **passive transformation** (from the robot's perspective) where the objects (the points in the coordinate space) remain stationary while the coordinate space moves around to accurately represent the location and rotation of the objects

All can be summarized to this:

| Active Transformation Paradigm                                                                                           | Passive Transformation Paradigm                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Fixing a perspective with the designated coordinate space so vectors and objects move around as their coordinates change | Perspective is fixed to a particular object being transformed, making it appear as if the coordinate space is being transformed and the object remains stationary |
Transforming an object under any of these paradigms have the same effect on the coordinates as performing the opposite transformation to the coordinate space
^transformationParadigms

We can specify these coordinate spaces by describing the origin and its axes. 

The origin is a point that defines the position of the space and can be described just like any other point. The axes are vectors and describe the orientation of the space (and possibly other information such as scale), and the usual tools for describing vectors can be used. 

The coordinates we use to measure the origin and axes must be relative to some _other_ coordinate space.

