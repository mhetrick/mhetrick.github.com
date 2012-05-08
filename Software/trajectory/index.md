---
layout: page
title: "Trajectory Synth"
description: ""
---
{% include JB/setup %}

<p>by Michael Hetrick, for UCSB MAT 240B (January-March 2011), taught by Matt Wright and Ryan McGee.</p>
<p>&nbsp;</p>
<p>Description:</p>
<p>Trajectory Synth was started as both a fun sound toy and an attempt to familiarize myself with a few important programming libraries. The original incarnation was simply an OSC message generator to communicate with Ryan McGee's Sound Element Spatializer, using the liblo library. Each particle represents a sound in space and its position in a 360-degree sound system (elevation is not considered).</p>
<p>After that was completed, I decided that I wanted to add sound and manual control to each particle. For this half of the project, I used Lance Putnam's excellent Gamma library (for sound generation) and GLV library (for an OpenGL interface). This was much more difficult than I originally intended, as both libraries are very deep.</p>
<p>The current version is effectively an eight-operator FM synthesizer, with multiple waveforms and a variable-resonance lowpass filter. Each particle is attached to a sound generator that outputs on its own channel.</p>
<p>&nbsp;</p>
<p>Technical Notes:</p>
<p>Many challenges presented themselves over the course of this project. For starters, the original base of this program was my first OpenGL program, which was a particle emitter (this emitter was designed to handle thousands of particles at a time). Turning it from a graphical demonstration into a musical tool was the first step. The next step was learning GLV and attaching it to the code. The callback function for OpenGL had to be modified in a few small ways to make it compatible with GLV (depth testing is turned on by default in GLV). The hardest part was learning how to use Gamma properly. The main issue is that Gamma will sample a wavetable once per callback function. To get a proper FM synth going, I had to create an interesting loop to make sure that all of the data is received once, but the frequencies are properly calculated for each oscillator.</p>
<p>&nbsp;</p>
<p>Future Ideas/Fixes:</p>
<p>-Particles will occasionally clump or just fly through each other. I need to add a few tweaks to the collision detection algorithm to fix this.</p>
<p>-I want to add a sound event for collisions. Perhaps increasing the frequency of a collided particle briefly for a &quot;ping&quot; effect would work well. I need to learn how to do envelopes in Gamma first.</p>
<p>&nbsp;</p>
<p>Conclusion:</p>
<p>Overall, I thought this was a successful project for me as a programmer. This wasn't really intended as a program that many people would want. Instead, I wanted this to be a way to force myself to learn many libraries and techniques (I just started C++ this quarter), and to create a sound toy that I would enjoy using. At the end of the project, I find myself to be a much-improved C++ programmer (actually, just a better all-around programmer), and I have a program that is capable of making compelling sounds.</p>
<p>&nbsp;</p>
<p>To use Trajectory Synth, download the following XCode project:</p>
<p><a href="TrajectoryControl.zip">Download</a></p>
