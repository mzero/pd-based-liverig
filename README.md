
crunch/pdbj - Pure Data Beat Jam
================================

About
-----

`cruncn/pdbj` was developed as a laptop replacement for my live performance
rig. It is aimed at running on a RaspberryPi with a Pisound card without a
display. One button click launches the patch and you have:

* simple looper
* stutter / glitch effect
* LFO gate
* low pass and high pass filter sweeps
* reverb
* triple rhythmic delay lines
* shelving EQs
* mixing buss
* mapping of MIDI controller
* MIDI control over synth/drum machine
* Ableton Link sync

Most of the effects are beat sync'd and will follow the tempo.
The effects all have parameters that are to be mapped to your MIDI controller.


Hardware
--------

**Computer:** `pdbj` should run anywhere `pd` and the required externals run.
I develop and play the patch on my MacbookAir under OS X. When performing I run
it on a RasberryPi with a [Pisound](https://blokas.io/) board. The whole patch
uses less than 20% of a RasberryPi, so I imagine it'll run whereever you like.

**Audio:** pdbj takes one stereo input and produces one stereo output.

**MIDI:** pdbj expects two MIDI ports in `pd`. The first is connected to your
controller. I use a [FaderFox UC44](http://www.faderfox.de/uc44.html), but you
can remap the parameters to your controller easily within the patch.

The second port is your synth or drum machine. I play with an
[Elektron Digitakt](https://www.elektron.se/products/digitakt/), but others
will work fine. `pdbj` sends MIDI clock to this device, and forwards eight
CCs from the MIDI controller to it. On the Digitakt, I have these set up to
be the master volumes of the eight tracks.


Installation
------------

pdbj was developed on pd 0.47 vanilla. Eariler versions might work, but haven't
been tested at all.

pdbj needs these pd externals:

    abl_link~
    freeverb~
    ggee

These can all be installed from the Deken installer built into pd (as of 0.47).






