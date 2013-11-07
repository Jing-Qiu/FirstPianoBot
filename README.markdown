PianoBot
========

A simple NXT robot that can play a given tune on a piano keyboard. Watch a [video](http://vimeo.com/13061942) of it in action!

Building Instructions
---------------------

1. PianoBot uses a 4x4 chassis as its base. Instructions for building one can be found on the NXT Programs [website](http://www.nxtprograms.com/4x4_chassis/steps.html).
2. Follow steps 10-11 found [here](http://www.nxtprograms.com/4x4_joystick/steps.html) to mount the NXT brick on the chassis.
3. Up-close pictures of the robot's "finger" can be found on my [Flickr page](http://www.flickr.com/photos/mattrajca/sets/72157624659077834/). The motor powering the "finger" should be connected to port A, while the other motors should be connected to ports B and C, respectively.
4. The source of the NXC program can be found in this git repository under the PianoBot subfolder. Change the `FILE_TO_PLAY` constant to match the name of the song file you wish to play.

Usage
-----

Before playing any song, make sure the robot's "finger" is lined up with the middle-C.

Song Files
----------

Songs themselves are stored in separate 'sng' files. Each line in a song file consists of a note value (greater than 0, see the `Note` struct in pianobot.nxc for more info) and a duration (in milliseconds). Both of these properties are followed by a space, and the file is terminated with an empty line. To include a "rest", use a note value of 0.

Limitations
-----------

The precision of the servo motors depends on the NXT's battery life, the surface they are operating on, and their power set-point. I made an effort to make playback as accurate as possible, but if anyone has any ideas on improving this furthermore, please drop me an email.
