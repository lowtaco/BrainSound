# BrainSound
A project to convert brain waves into a midi signal Ableton Live

# How to use
- The project is written in openvibe. The first thing you need to do is [download](http://openvibe.inria.fr/downloads/) it.
- The neural interface is built on the basis of [NeuroSky TGAM](https://store.neurosky.com/products/eeg-tgam).
- The project needs [Ableton Live](https://ableton.com/).

1. Connect the neural interface (connect the power supply and USB receiver to the PC).
2. Run a **openvibe-acquisition-server**.
3. Select **NeuroSky MindSet Driver** and open properties.
4. Make the necessary settings.
5. Click **Connect** and then **Play**. The Receiving label should appear.
6. Run a **openvibe-designer** and load file called **BrainSound Scenario**.
7. In Ableton Live run Max for Live plugins: **BrainSound Scanner**, **BrainSound**, **BrainSound Midi Mapper**.
8. Brain Sound Scanner should start receiving signals from OpenVibe, if this did not happen, check the ports in the OC Controller.
9. The Midi Mapper should stand after BrainSound. In it, select P1, P2, P3, P4, V1 and assign your OSC address to each of these parameters.
10. Install any Midi Instrument of your choice. Preferably with a long attack.
11. Run OpenVibe Scenario.

# Default OpenVibe OSC Setting:
 - OSC Server IP: 127.0.0.1
 - OSC Server Port: 9001
 
 Wave addresses:
 1. /attention
 2. /meditation
 3. /delta
 4. /theta
 5. /low-alpha
 6. /high-alpha
 7. /low-beta
 8. /high-beta
 9. /low-gamma
 10. /mid-gamma

***/attention** and **/meditation** these are selected waves based on NeuroSky eSense technology.*
