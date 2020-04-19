# kicad

KiCad is an open source tool for designing PCBs.

## installing on windows
It can be downloaded [here](http://kicad-pcb.org/) and its easy to install. Remember that after installation its a good idea to pull the newest libraries before getting started.

## installing on ubuntu
follow [the instructions here](https://kicad-pcb.org/download/ubuntu/)
Remember that after installation its a good idea to pull the newest libraries before getting started.

### Tutorials
#### good beginners tutorial 

[here](https://github.com/MalphasWats/hawk)

#### good up to date video tutorials 
[John's Basement KiCAD tutorial](https://www.youtube.com/watch?v=9hcQQQxoRl0&list=PL3by7evD3F51fKkyrUbH-PCdwPCWc9F8a) 
It should be noted that the author makes a big deal about "acid traps" which are no longer a problem with modern PCB manufacturing [see here](https://resources.ema-eda.com/blog/are-acid-traps-still-a-problem-for-pcbs-in-2019)

## symbol and footprint libraries
In kiCAD the abstract representation of a part in a scemetic is called a symbol where as the abstract represenation of a part in the layout editor is called a footprint. These two representations are two different firmats, what links them together are the pin names. For example a schemetic symbol of a transistor with pin names 1 2 3 could match up to many different footprints. At the same time a TQFP100 chip package could match up with many different symbols for many different microcontrollers. In the symbol one can provide a default footprint and/or the user can edit this value on a per instance basis in the schemetic editor.

### adding symbol libraries
To add a symbol library go to **Preferences -> Manage Symbol Libraries...**, klick on the folder icon and brouse to the library you want to add.

Good places to load symbols and footprints from are:
 - the auto-intern library
 - [snapEDA](https://www.snapeda.com/)
 - [digikey kiCAD library](https://github.com/Digi-Key/digikey-kicad-library)

### creating symbol libraries
To create symbols and symbol libraries on the project screen go to **Tools -> Edit Schemetic Symbols** then either **File -> New Library...** to create a new library or select the library you want to add a symbol to in the left pane, right click it and select **New Symbol**.

Be sure to set the grid to 2.54mm when placing pins as a smaller grid may yield pins that are inaccessable to someone using a courser grid in their schemetic.

Add pins to your symbol and draw its body in this editor. Remember the pin names are just for humans, the machiene only cares about the pin number and in the case of design rule checking the *electrical type*.

### creating footprint libraries
To create footprints and footprint libraries on the project screen go to **Tools -> Edit PCB Footprints** then either **File -> New Library...** to create a new library or select the library you want to add a symbol to in the left pane, right click it and select **New Footprint**.

## hotkeys
### schemetic
 - M move item
 - C copy item
 - G drag component
 - A add component
 - P add power
 - R rotate item
 - E edit properties of item
 - V edit value
 - F edit footprint
 - W begin wire
 - L add label
 - H add higherarchial label
 - Q add no connect
 - S add sheet

### layout
 - Q change track width
 - X add new track
 - V add via
 - D drag track
 - M move item
 - F flip item (front to back of the board)
 - R rotate item
 - G drag item
 - E edit properties of item
 - B repour filled regions
 - U select track branch (piece betweeen two nodes)
 - I select whole track



 # plugins
 [panelize-plugin](https://github.com/msvisser/panelize-plugin)

