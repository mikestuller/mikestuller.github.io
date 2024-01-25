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

When you first launch midiWorx, you'll see a nearly blank screen because you haven't created anything yet. Tap the "Add Module" (the one that looks like a "+" sign) to display the Module Browser. Here you choose modules to add to your project. For this example, choose the Piano Keyboard module. Then, also add an "Event Viewer" module. Now let's connect the two modules together.

Each module consists of two parts: a control panel, and a "node" where connections to other modules are made. When you connect two modules, you must choose which one will be sending MIDI messages and which will be receiving the sender's messages. In our example, the Piano Keyboard will send messages to the Event Viewer.

To connect one module to another, first select the sending module (the Piano Keyboard) by tapping on its node or its control panel. When you select a module, a ring of buttons appears around its node. Tap the connect button (see figure), then complete the connection by tapping the node of the receiving module (the Event Viewer). Play some notes by tapping on the Piano Keyboard. You should see the Note On and Note Off MIDI messages in the Event Viewer's control panel.

<figure>
  <img src="https://github.com/mikestuller/mikestuller.github.io/assets/97295847/fdfee1cc-f072-4f19-8c57-2c61026fb853" width = "200"> 
  <figcaption>Node Buttons</figcaption>
</figure>

Here's what each node button does:
* **Connect** Allows one module to send MIDI messages to another
* **Bypass** Bypasses the selected module. MIDI messages received by the selected module will be passed directly to its receivers.
* **Disconnect** Removes a connection
* **Choose Color** Allows you to change the color of the selected module
* **Delete** Deletes the selected module
* **Info** Shows information about the selected module


### More Details

[TODO]
