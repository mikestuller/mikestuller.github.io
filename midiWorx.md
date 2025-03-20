# midiWorx

  * [Overview](#overview)
  * [What is MIDI?](#what-is-midi)
  * [More About Modules](#more-about-modules)
  * [Getting Started](#getting-started)
  * [Node Buttons](#node-buttons)
  * [Navigation](#navigation)
  * [&#8627; Workspace Navigation](#workspace-navigation)
  * [&#8627;  Panel Stack Navigation](#panel-stack-navigation)
  * [The Master Clock](#the-master-clock)
  * [Glossary](#glossary)

## Overview

midiWorx is a virtual MIDI workbench for iOS. With midiWorx, you can create MIDI messages, modify them, direct them, and more.

midiWorx is:
  * an aid to creativity, useful for sparking new musical ideas.
  * a performance tool to enhance the abilities of external hardware or other apps.
  * a bridge to enable other apps and external hardware devices to work with each other.
  * a diagnostic tool to identify problems in an existing MIDI setup.
  * a jack-of-all-trades MIDI toolbox consisting of everything from event filters and mappers to an arpeggiator and a sequencer.

midiWorx consists of many "modules" -- things like MIDI event filters, MIDI note generators, and more. While most of the modules can be useful on their own or in small combinations, the most powerful aspect of midiWorx is its ability to flexibly combine modules by connecting them with each other however you want to.

Here's an example: You could use a Midi In module to receive notes generated from an external keyboard. Then you could use a Note Splitter module to split the notes into a lower portion and an upper portion. You could then apply an Arpeggiator to only the upper portion, and a Transposer to transpose the the lower portion down an octave. Finally, you could use Midi Out modules to send the lower portion to a sound-generating app and the upper portion to an external synthesizer.

[Home](#midiworx)

### What is MIDI?

MIDI stands for "Musical Instrument Digital Interface". It is the standard protocol by which electronic music devices like synthesizers communicate with each other. It's important to realize that MIDI does not transmit recorded sounds. Rather, you can think of MIDI messages as being directions such as "play Middle C with velocity 93" (In the MIDI standard, "velocity" refers to how hard or loud a note is played.)

Typically, a device like a keyboard or some other "MIDI controller" would be used to generate and transmit MIDI messages to another device, such as a synthesizer. It is up to the synthesizer to produce the sounds with the pitches and velocities specified by the messages.

[Home](#midiworx)

### More About Modules

Modules are the building blocks of a midiWorx project. There are modules that generate MIDI messages ("Sources"), modules that consume MIDI messages ("Destinations"), and modules that transform MIDI messages in some way or another ("Modifiers"). Some modules, like the Recorder, are both Sources and Destinations.

Each module consists of two parts: a rectangular control panel, and a circular "node". The control panel is where you make adjustments to the various parameters of the module. The node is where you connect the module to other modules. The control panels are grouped together in a stack. You can drag the nodes around to place them wherever you want to.

There is no limit to the number of connections a module can have, although some modules only allow input connections and some other modules only allow output connections.

[Home](#midiworx)

### Getting Started

When you first launch midiWorx, you'll see a nearly blank screen because you haven't created anything yet. Tap the "Add Module" ("+") icon to display the Module Browser. Here you choose modules to add to your project. For this example, choose the Piano Keyboard module. Then, also add an "Event Viewer" module.

As mentioned above, you can position each node by dragging it. You can also move all the nodes by dragging the background, or pinch to zoom in and out.

In order to connect two modules, you first have to decide which one will be sending MIDI messages and which one will be receiving the sender's messages. In our example, the Piano Keyboard will send messages to the Event Viewer.

Select the sending module -- the Piano Keyboard -- by tapping on its node. You'll see a ring of buttons appear around the node. Tap the "Connect" button (see below), then complete the connection by tapping the node of the receiving module -- the Event Viewer.

Now play some notes by tapping on the Piano Keyboard. You should see corresponding Note On and Note Off MIDI messages displayed in the Event Viewer's control panel.

Congratulations, you've built your first layout! Try adding other modules and other connections. Have fun!

[Home](#midiworx)

### Node Buttons

When a module is selected, the following buttons appear surrounding its node:

<figure>
  <div style="text-align: center;">
  <img src="https://github.com/mikestuller/mikestuller.github.io/assets/97295847/fdfee1cc-f072-4f19-8c57-2c61026fb853" width = "150"> 
  <figcaption><i>Node Buttons</i></figcaption>
    </div>
</figure>


* **Connect** Lets one module send MIDI messages to another. First select the module that will send MIDI data. Tap "Connect" and then tap the node of the module will receive MIDI data. A line will appear connecting the two modules.
* **Bypass** Bypasses the selected module. MIDI messages received by the selected module will be passed directly to its receivers without being acted on by this module.
* **Disconnect** Removes a connection.
* **Choose Color** Lets you change the color of the selected module.
* **Delete** Deletes the selected module.
* **Info** Shows information about the selected module.

[Home](#midiworx)

### Navigation

#### Workspace Navigation

Press and drag on an empty part of the workspace to adjust your view of it. Pinch to zoom in or out. Tap on a node to select it. Press and drag on a node to move it. Tap the "Find" button to bring the currently selected module's node into view and to reset the zoom level.

#### Panel Stack Navigation

Select a module by tapping on its node or on its control panel. The Panel Stack automatically shifts up or down to display the currently selected module. Use the up and down chevron buttons on each control panel to change the order of the panels in the Panel Stack. Swipe up or down on the Drag Handle of a control panel to shift the entire Panel Stack up or down. Swipe right on the Drag Handle of a control panel to minimize the Panel Stack in order to view more of the workspace. Once minimized, swipe left on a Drag Handle to maximize the Panel Stack.

[Home](#midiworx)

### The Master Clock

Some modules like the Arpeggiator require a timing source. That is the purpose of the Master Clock. The Master Clock can either be internal, i.e. generated and controlled by midiWorx, or external, i.e. generated and controlled by another app or external hardware device.

To use an _external_ Master Clock, create a Midi In or a Midi Virtual In module to connect midiWorx to another app or external hardware device. The other app or hardware device must be capable of generating MIDI clock messages (sometimes called "MIDI beat clock"). Then, in the Midi In or Midi Virtual In control panel, enable the "Master Clock" switch. The other app or hardware device will now be used as the Master Clock.

If you don't have an external Master Clock configured, an _internal_ Master Clock will automatically be created if there's not already one whenever you add a module that needs a Master Clock. In that case, transport controls (Play from Beginning, Play, and Pause) and a Tempo slider will appear at the top of the screen. 

Whether you're using an internal or an external Master Clock, you can only have one Master Clock at a time.

[Home](#midiworx)

### Glossary

**Control Panel:** The part of a module that lets you configure it or view its operation. Control panels are located in the Panel Stack.

**Layout:** The positions of the nodes in the workspace and the connections between them.

**Module:** A component that creates, transforms, or otherwise acts on MIDI data. Each module either receives MIDI data, sends it, or both. You connect modules together in order to create something new and powerful. Each module consists of two parts: its node, which you use to connect to the nodes of other modules, and its control panel, which you use to configure the module.

**MIDI:** "Musical Instrument Digital Interface". MIDI is the standard by which electronic musical components like synthesizers and midiWorx modules communicate with each other. MIDI consists of a stream of data describing things like "Note On", "Note Off", "Pitch Bend", etc.

**Node:** The part of a module that is used to connect to other modules. Nodes appear as circles in the workspace. To make a connection, select the node of the module that you want to send MIDI data. Tap on the Connect button. Finally, tap on the node of the module that you want to receive the MIDI data.

**Panel Stack:** The stack of control panels on the side of the screen.

**Workspace:** The area on which the nodes are placed.

[Home](#midiworx)
