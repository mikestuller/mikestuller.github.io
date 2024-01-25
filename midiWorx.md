## midiWorx


## Overview

midiWorx is a "virtual MIDI workbench" for iOS. With midiWorx, you can create MIDI messages, modify them, direct them, and more.

midiWorx can be used:
  * as an aid to creativity, to spark new musical ideas.
  * as a performance tool to enhance the abilities of external hardware or other apps.
  * as a tool which helps multiple external hardware and apps to work with each other.
  * as a diagnostic tool to identify problems in an existing MIDI setup.

midiWorx consists of many "modules" -- things like MIDI filters, MIDI note generators, and more. While most of the modules can be useful on their own or in small combinations, the most powerful aspect of midiWorx is its ability to flexibly combine modules by connecting them with each other however you want to.

Here's an example: You could use a Midi In module to receive notes generated from an external keyboard. Then you could use a Note Splitter module to split the notes into a lower portion and an upper portion. You could then apply an Arpeggiator to only the upper portion, and a Transposer to transpose the the lower portion down an octave. Finally, you could use Midi Out modules to send the lower portion to a sound-generating app and the upper portion to an external synthesizer.

### What is MIDI?

MIDI stands for "Musical Instrument Digital Interface". It is the standard protocol by which electronic music devices (like synthesizers) communicate with each other. It's important to realized that MIDI does not transmit recorded sounds. Rather, you can think of MIDI messages as being directions such as "play Middle C with velocity 93" (In the MIDI standard, "velocity" refers to how hard or loud a note is played.)

Typically, a device like a keyboard or some other "MIDI controller" would be used to generate and transmit MIDI messages to another device, such as a sound module. It is up to the sound module to generate and play the notes (the actual sounds) with the pitches and velocities specified by the messages.

### Getting Started

When you first launch midiWorx, you'll see a nearly blank screen because you haven't created anything yet. Tap the "Add Module" (the one that looks like a "+" sign) to display the Module Browser. Here you choose modules to add to your project.

Each module consists of two parts: a control panel, and a "node" where connections are made. When you connect two modules, you must choose which will be the "parent" module (the one sending MIDI messages) and which will be the "child" module (the one receiving the parent's messages).

To connect one module to another, first select the parent module by tapping on its node or its control panel. When you select a module, a ring of buttons appears around its node (see below). Tap the connect button, then complete the connection by tapping the child module.

![NodeButtons](https://github.com/mikestuller/mikestuller.github.io/assets/97295847/5e7b4f90-1542-4f09-8904-42bf495dfe3d)
*Node Buttons*

Here are the halo buttons and what they do:
* **Connect** Allows one module to send MIDI messages to another
* **Bypass** Bypasses the selected module. MIDI messages received by the selected module will be passed directly to the selected module's children.
* **Disconnect** Removes a connection
* **Color** Allows you to change the color of the selected module
* **Delete** Deletes the selected module
* **Info** Shows information about the module
[TODO]

### More Details

[TODO]
