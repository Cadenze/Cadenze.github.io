---
layout: post
title: An Initial Look at the Poincaré
---

As I have written last week, my term 1 project involves writing about Perelman's solution to the Poincaré conjecture. After some initial reading and a small discussion with my mentor, these are my first thoughts on the topic.

## The Conjecture

The Poincaré conjecture, as conjectured by Henri Poincaré in 1904, states that:

<p class="message" style="text-align:center">
    Every simply connected, closed 3-manifold is homeomorphic to the 3-sphere.
</p>

This might look very confusing, and that is why we are going to break this down into parts and explain each concept briefly.

Firstly, a manifold. A manifold is defined as "a topological space that resembles Euclidean space at each point". A 2-manifold means that object looks like a plane locally, but does not necessarily need to be a 2-dimensional object, like a piece of paper, a Möbius strip, or even the surface of the Earth. To expand this concept one dimension higher, a 3-manifold will look like 3-dimensional space locally, but might be bent in another dimension (time?). The fabric of space itself can be considered a 3-manifold, since it is a 3-dimensional space (duh), but gravitational forces can bend it in respect to time.

Secondly, "simply connected". Simply connected (or 1-connected, since we all like numbers), means that any closed path (like a circle) on that manifold can be contracted into a point. Applying to 2-manifolds, it means that the surface cannot have any holes. The surface of a sphere is simply connected; the surface of a doughnut is not.

Thirdly, "closed". A closed manifold has no boundary, and is "compact" (imagine a closed interval). A 1-dimensional example is the circumference of a circle, where there is no "end" to the line, and the distance that line travels before it meets itself is finite.

Next, "homeomorphic". In layman's terms, an object is homeomorphic to another when they can be transformed between each other by stretching and bending it without creating holes. A classic example would be a coffee mug is homeomorphic to a doughnut, since they are both objects with one hole.

Lastly, a 3-sphere is a hypersphere. A circle, or a 1-sphere, is constructed using all the points on a plane a fixed distance away from a single point. A sphere, or a 2-sphere, is constructed using all the points in space a fixed distance away from a single point. A 3-sphere, by analogy, is constructed using all the points in spacetime a fixed distance away from a single point.

So, the Poincaré conjecture can be understood as: space, if it is limited in volume, has no boundary, and has no "holes", it is curved in another dimension, and is a hypersphere; an analogy for 2-manifolds would be how the surface of the Earth is limited in area, has no boundary, and isn't a doughnut, therefore it must be spheric.

## The Solution

Grigori Perelman, a Russian mathematician, provided the proof of the conjecture over 3 papers in 2002-2003. His proof utilized a method called Ricci flow with surgery, which successfully proved that those 3-manifolds can be reduced into 3-spheres. This problem regarding 3-manifolds is the last problem of its kind to be solved; all higher dimensions of the Generalized Poincaré conjecture have been proven true before the turn of the century.

Ricci flow, introduced by Richard Hamilton, is essentially a differential equation that changes a manifold based on its curvature over time. It tends to produce objects that are rounder in shape and reduced in volume, which is ideal in a problem that wants to reduce objects into a simpler one. However, as the differential equation proceeds through time, some objects might produce singularities, and since Ricci flow can only operate on smooth manifolds, not all 3-manifolds can be reduced to 3-spheres in this manner.

Perelman dealt with this scenario by introducing a "surgery" to cut, and then cap these singularities, and then perform Ricci flow again. He proved that all singularities can be dealt with this way without breaking homeomorphism.

A natural question to come up after this is the number of cuts needed. If singularities can be produced by a single Ricci flow process, it might happen again after cutting, potentially infinitely many times. Perelman spent most of his third paper proving that a finite number of cuts is enough for any object, and thus, Ricci flow can be used to reduce any simply connected, closed 3-manifold into a 3-sphere, and the Poincaré conjecture is proven true.

If you do have any insights on the Poincaré conjecture, please contact me on my [discord server](https://discord.gg/eTtJwKJ), I am in need of ideas to write this paper out.