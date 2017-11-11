# NatNet SDK

This repository contains each version of NaturalPoint's [NatNet SDK](http://optitrack.com/downloads/developer-tools.html).


## Changelog

__2.7__ _(October 21, 2014)_

Features & Enhancements

* Motive 1.7 Streaming support
* New timing sample for validating mocap streaming frame timing.
* New Broadcast Trigger sample illustrating how to use remote record trigger/listen using XML formatted UDP broadcast packets instead of NatNet commands.
* NatNetML - added SMPTE Timecode and Timecode Subframe members. See WinForms sample for usage.

Fixes

* Fix for FrameID periodically displays dropped/duplicate packets during live mode.
* Fix for PacketClient incorrectly decoding rigid Body IsTracked parameter.
* Fix for crash in GetDataDescriptions() when streaming a Rigid Body with a single character name.
* Sample Clint incorrectly reports skeleton marker data
* Update SampleClient3D to clarify quaterion decomposition, add new visuals.
* Maximum markers per rigid body changed from 10 to 20 to match new RigidBody tracking capabilities in Motive.
* Frame timestamp now keyed off hardware frame id. fTimestamp resolution increased from float to double (DirectDepackatization clients should update their code (see timestamp in PacketClient.cpp for an example).


__2.6__ _(May 8, 2014)_


Features & Enhancements

* Added Motive 1.6 streaming support.
* New RigidBody tracking state parameter added to the NatNet stream.
* IsRecording flag on FrameOfMocapData was added, indicating frame was recorded in Motive.
* ModelsChanged flag on FrameOfMocapData indicating actively tracked model list has changed.
* Additional flags on LabelMarkerList indicating marker occlusion and marker position calculation method.
* Additional FrameOfMocapData timestamp added to the stream.
* NatCap remote capture sample for illustrating send/receive of Motive remote control commands via UDP direct broadcast.
* UDP Repeater / Unity3D
* Increased the unlabeled/other marker count cap to 1000 markers per frame.

Fixes

* SampleClient latency value was incorrectly calculated.


__2.5__ _(October 2, 2013)_

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

