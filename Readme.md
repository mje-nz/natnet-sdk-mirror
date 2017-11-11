# NatNet SDK

This repository contains each version of NaturalPoint's [NatNet SDK](http://optitrack.com/downloads/developer-tools.html).


## Changelog

__2.9.0__ _(October 19, 2015)_

Features & Enhancements

* Added: Motive 1.9 streaming support.
* Added: Stream ID of unlabeled markers over NatNet. Please refer to updated Winforms sample to show new unlabeled marker data access.
* Added: Add Force Plate information to data descriptions and FrameOfMocapData structure. ( Bitstream syntax change)
* Added: (NatNet Managed Library (NatNetML) only) Update Winforms sample to illustrate data polling as an alternative to data callback.

Fixes

* Fixed: (NatNet Managed Library (NatNetML) only) Update NatNetML with marker parameter data (e.g. occluded flag)


__2.8.0__ _(September 2, 2015)_

Features & Enhancements

* Added: Motive 1.8 streaming support
* Added: New MATLAB wrapper sample.
* Added: Add playback range and looping commands ("SetPlaybackStartFrame,frameNumber", "SetPlaybackStopFrame,frameNumber", "SetPlaybackLooping,0or1") to NatNet command list, and updated NatNet SDK Winforms and PacketClient samples to illustrate usage.
* Added: DecodeID() helper routine, which illustrates usage in Winforms and SampleClient apps for decoding legacy marker ID
* Added: Updated Unity3D streaming sample to stream rigid bodies and skeletons.
* Added: Add Z-up quaternion to Euler decoding example to WinForms sample when streaming Z-up from Motive.
* Added: Add support and examples for explicitly disconnecting Unicast clients.
* Added: Add support for Z-up streaming, and update SampleClient 3D to illustrate usage.
* Changed: (NatNetML only) Change GetLastFrameOfData() routine in managed client to lock the frame and return a copy of the data (polling clients only). Update WinForms sample app to illustrate usage.
* Changed: (NatNetML only) Provide copy constructors to simplify .NET client data deep copy operations, and update Winforms sample with data copy operation.
* Changed: (NatNetML only) Fix graphing for correct frame alignment for Motive.
* Changed: (NatNetML only) Add timing testing operations and reporting.

Fixes

* Fixed: Fix for PointCloud solved bit indicator.
* Fixed: Debug x64 WinformsSample was not compiling out of the box.
* Fixed: RigidBody tracked flag in managed clients is now transmitted correctly.


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

