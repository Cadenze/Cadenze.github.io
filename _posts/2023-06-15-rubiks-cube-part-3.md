---
layout: post
title: Rubik's Cube Part 3
---

2 years from the [last Cube Project post](2021/04/11/rubiks-cube-part-2),
some of you might be expecting
this third edition to come out sooner or later.

## The Idea

So far, I have had a single project related to the cube every single year;
the [Speedcube Method Efficiency Analysis project](/2021/04/09/rubiks-cube-part-1)
in first year as part of Science One,
and the Cube Timer project in second year as part of CPSC 210.
Naturally, it would be ingenious to continue the theme
and work on a cube-related project in third year.
As such, as part of PHYS 319, an electronics lab course,
I have chosen to build a microcontroller-based robotic Rubik's Cube solver.

## The Parts

### Stepper Motor

Since we would need to individually move the 6 faces of the cube,
we would need motors that have precise positional control,
with the additional benefit that
they can turn an indefinite amount in any direction.
Our choice is the use 6 stepper motors,
specifically the NEMA 17 bipolar stepper motors,
which you can often find for a cheap price on Amazon.

<!-- NEMA 17 image -->

Bipolar stepper motors operate on two coils,
and given a current alternately between the coils,
we can drive the motor shaft (a permanent magnet) to rotate a precise angle,
and in our case exactly 1.8&deg;.

<!-- NEMA 17 schematic -->

### Stepper Motor Driver

However, the delicate task of controlling a single stepper motor
requires four output pins on the microcontroller,
which adds up to 24 output pins to control six motors,
taking up a significant amount of the total available pins.
Therefore, we delegate the task of manouvering a stepper motor
to a specialized integrated circuit, the stepper motor driver,
which requires significantly fewer pins to control..

<!-- A4988 image -->

The cheapest and most common drivers found on Amazon are the A4988,
which we need one each for the six stepper motors.
Now they would only require 3 signals each to control,
2 of which can be the same signal between all drivers.

<!-- A4988 schematic -->

### Coupling Mechanism

Now that we have the thing that moves (the motor)
and the thing that is about to be moved (the cube),
we need to figure out a way to connect those two parts.
Since there is no premade component that interfaces a cube and a motor,
we must therefore design our own.

To successfully turn the face of a cube,
we merely need to turn the center of the cube.
Our mechanism relies on the cube having detachable center tiles,
which we can slot in our mechanism that grapples on it.

<!-- Coupling mechanism - cubeside -->

This cubeside part must be connected to the motorside part
such that as the motor shaft rotates,
the parts rotate along with it.
We have designed these two parts to be separable
so that we gain the possibility and convenience of
removing the cube itself without disturbing the motor setup.

<!-- Coupling mechanism - motorside -->

A small thank you to Morgan for lending me his 3D printer,
which made the production of these parts possible.

### Power Supply

The next issue is with a power supply.
Since the logic voltage supply is usually either 3.3V or 5V,
while the motor voltage supply needs to be above 8V,
we must use different power supplies for the logic and motor circuits.
As motors can often draw a lot of current and power,
to minimize heat dissipation,
we have chosen the logic voltage as 3.3V,
and the motor voltage to be 12V.
Although the motors themselves are rated at 7.3V,
we can tune the potentiometer on the driver itself
such that no excessive voltage or current will go through the motor.

The choice of 12V is also partly due to the cube itself.
Inside every single center,
there is a tunable spring.
If we let the spring be more loose,
then we would require a lower torque to overcome static friction,
and hence the motor would not require as much power and voltage;
however, the faces of the cube will cam outwards as we rotate them,
which might lead to small undesired movements of the cube itself,
and the faces might get stuck in the middle of a rotation,
potentially leading to a rapid disassembly of both the cube and the machine.
On the other hand,
to prevent that from happening,
we woudl require a higher torque to overcome the higher static friction,
and hence the motor would require more power and higher voltage.
Our final choice of 12V and 1.3A is a good balance.

<!-- Insignia power supply -->

Before successfully sourcing for a potential power supply,
I have been using the AC to 12V that came with the Wi-Fi router at home.
Luckily, I had found an identical power supply in Best Buy
merely days before the actual presentation for this project,
as otherwise my home would have to go without internet
every time I try to power up my robot.

### Structure

To package together all the components,
we must build a frame.
We used a Lego set that is readily available,
which allowed for quick prototyping of different structures
at the cost of a small amount of precision of placements.

The other obvious choice for the material for the structure
would be laser-cut acrylic sheets.
This would have been the preferred way to build the structure,
as I am familiar with laser cutters from grades 7 & 8;
however, I did not know that we had access to the laser cutters,
which were just situated in the engineering physics lab next door.

## The Logic

## The Algorithm
