## midiWorx

![Uploading <?xml version="1.0" encoding="UTF-8" standalone="no"?>
<!-- Created with Inkscape (http://www.inkscape.org/) -->

<svg
   width="25"
   height="25"
   version="1.1"
   viewBox="0 0 6.614583 6.614583"
   id="svg838"
   sodipodi:docname="connect.svg"
   inkscape:version="1.1.1 (c3084ef, 2021-09-22)"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:svg="http://www.w3.org/2000/svg">
  <defs
     id="defs842" />
  <sodipodi:namedview
     id="namedview840"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     inkscape:pageshadow="2"
     inkscape:pageopacity="0.0"
     inkscape:pagecheckerboard="0"
     inkscape:document-units="mm"
     showgrid="false"
     units="px"
     inkscape:zoom="11.720245"
     inkscape:cx="24.316898"
     inkscape:cy="16.04062"
     inkscape:window-width="1495"
     inkscape:window-height="854"
     inkscape:window-x="544"
     inkscape:window-y="142"
     inkscape:window-maximized="0"
     inkscape:current-layer="svg838"
     inkscape:snap-object-midpoints="true" />
  <circle
     cx="7.2637267"
     cy="0.80464619"
     r="0.95467424"
     id="circle1036"
     transform="rotate(34.977028)"
     style="stroke-width:0.0939085" />
  <circle
     transform="matrix(-0.81938195,-0.57324796,-0.57324796,0.81938195,0,0)"
     cx="-1.9479399"
     cy="0.82342762"
     r="0.95467424"
     id="circle1042"
     style="stroke-width:0.0939085" />
  <path
     d="M 5.4905047,4.8232291 1.2231863,1.8606906"
     fill="none"
     stroke="#000000"
     stroke-linecap="round"
     stroke-width="0.368746"
     id="path1044"
     style="stroke-width:0.557189;stroke-miterlimit:4;stroke-dasharray:none"
     sodipodi:nodetypes="cc" />
</svg>
connect.svg…]()


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

![connect](https://github.com/mikestuller/mikestuller.github.io/assets/97295847/57e32021-6159-4fa6-850d-297e87982fa1)

[TODO]

### More Details

[TODO]
