---
layout: post
title:  "Phased Arrays"
date:   2025-05-08 10:00:00 +0200
tags:   [oscillators]
---

I recently became interested in phased arrays after watching [this](https://youtu.be/z4uxC7ISd-c?si=QM6bxZAGs_SjXdXq).   
From what I understand, a phased array is basically a collection of regularly spaced oscillators that, due to interference, produce (somewhat focused) beams of waves. The more oscillators, the more focused the beam becomes. These beams which can be steered by subtle tuning of the phase difference between the individual oscillators. If all oscillators are in phase, the beam will propagate perpendicular to the array.

This phenomenon is used for a range of tech applications, such as antenna's (electromagnetic waves), and ultrasound imaging (ultrasonic acoustic waves). I was a bit inspired by this phenomenon, and formulated a vague goal for myself: to build a 2D phased array, for scanning 3D objects. The oscillators in question will produce ultrasonic waves of 40 KHz, and should be individually controlled through a microcontroller. The amount of oscillators I have in mind is a 4x4 or 5x5 grid, this amount is limited by the amount of ouputs on the microcontroller.

As a first step, I thought it would be a good idea to simulate these systems on a computer, to get a feeling for the behaviour of such systems.
