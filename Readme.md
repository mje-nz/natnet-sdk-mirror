# NatNet SDK

This repository contains each version of NaturalPoint's [NatNet SDK](http://optitrack.com/downloads/developer-tools.html).


## Changelog

__2.5__ _(October 2013)_

Features & Enhancements

* Added Motive 1.5 streaming support.
* A new Matlab sample demonstrates how to read from the NatNet stream through MatLab scripts.
* Additional function signature overloads to better support MatLab.
* Added new Motive remote control commands Start/Stop Recording, Start/Stop Playback, LiveMode, EditMode, * SetRecordTakeName, SetLiveTakeName. Refer to WinForms sample for usage examples.
* Added Motive record broadcast message parser sample.
* Samples were updated to illustrate accessing point cloud model solved marker locations.
* Added timing information to WinForms sample.
* New QuaternionToEuler() helper routines are now included.
* Winforms Sample updated with a new layout and sample Command/Requests for use with Motive.

Fixes

* SimplerServer compile issue.
* SampleClient when more than two skeletons are streaming.

