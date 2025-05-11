---
layout: post
title:  "Phased Arrays"
date:   2025-05-08 10:00:00 +0200
tags:   [oscillators]
---

How do you focus waves? One way is to use phased arrays.
I recently became interested in phased arrays after watching [this amazing video](https://youtu.be/z4uxC7ISd-c?si=QM6bxZAGs_SjXdXq).

From what I understand, a phased array is basically a collection of regularly spaced oscillators that emit in the outward direction, each oscillator producing a wave with a spherical symmetry. The idea is that, due to interference, the array produces a (somewhat focused) beam of waves. The more oscillators, the more focused the beam becomes. These beams can be steered by subtle tuning of the phase difference between the individual oscillators. If all oscillators are oscillating in unison, the resulting beam will propagate perpendicular to the array.

This phenomenon is used for a range of tech applications, such as antenna's (electromagnetic waves), and ultrasound imaging (ultrasonic acoustic waves). I was a bit inspired by this phenomenon, and formulated a vague goal for myself: to build a 2D phased array, for scanning 3D objects. The oscillators in question will be transducers that produce ultrasonic waves of 40 KHz, and should be individually controlled through a microcontroller. The amount of oscillators I have in mind is a 4x4 or 5x5 grid, the amount being limited by the amount of outputs on the microcontroller.

As a first step, I thought it would be a good idea to simulate these systems on a computer, to get a feeling for the behaviour of phased arrays. I started out with a script in Python that can simulate a 1D array of oscillators, it can be found [here](https://github.com/samman350/2D_PhasedArray/). Essentially, it's just a superposition of circular waves, 
$$\psi_i=e^{ikr}$$

I tried a row of 4 oscillators:
![four oscillators in a row]({{ '/assets/images/Waves.png' | relative_url }})

then steered it by changing the relative phases:
![steering the waves]({{ '/assets/images/Waves4Steer.png' | relative_url }})

and extended it to 6 oscillators. It can be seen that the beam is more narrow: 
![6 oscillators]({{ '/assets/images/Waves6Steer.png' | relative_url }})

and here is the power of the beam:
![the power of 6 oscillators]({{ '/assets/images/Waves4Steer_power6.png' | relative_url }})

The last image is somewhat misleading
