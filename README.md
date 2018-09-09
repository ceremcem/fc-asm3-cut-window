# Description

Example project to demonstrate cutting socket windows. Usage scenario: 

- [x] You have a circuit with connectors on it.
- [x] Create an enclosure (panel) for that circuit, arrange the placement with assembly container. 
- [x] Cut the connector windows 
- [x] Relocate circuit inside enclosure, **expect** the connector window cuts are relocated accordingly. 
- [x] Place additional circuits inside the enclosure 
- [x] Create additional window cuts without breaking previous work.
- [x] Refine the window cuts without breaking any previous work.

# Status 

Work In Progress

# Instructions

> Original Tutorial is [here](https://github.com/realthunder/FreeCAD_assembly3/wiki/Modeling-using-Assembly)

## Workflow 

You'll need two files: 

1. Create a file that holds the enclosure and the electronic part.
2. Create a separate file for the electronics part which holds the circuit and the other components (including cutters) that should be interpreted as a group. 

## Steps 

### 1. Electronics Part 

1. Import the circuit or draw from scratch if it doesn't exist yet. A RaspberryPi will be used in this example.

2. Draw the cutters

  1. Create a Part 
  2. Create Binder(s) for socket(s)
  3. Create cutter shapes with Part Workbench 
  
  ![create-electronics-and-cuts](https://user-images.githubusercontent.com/6639874/45267486-f20e5900-b475-11e8-801d-ef517e4e2cc9.gif)

### 2. Enclosure 

1. Create a link to the electronics part 

2. Draw the panel using PartDesign Workbench

![create-enclosure-include-electronics](https://user-images.githubusercontent.com/6639874/45267641-e4a69e00-b478-11e8-9509-98893d83eeee.gif)

### 3. Cut the panel with cutter

1. Create a Binder for the cutter 
2. Use "Cut" command in the Part Workbench to cut the `front-panel` with `cutter`

![cut-front-panel](https://user-images.githubusercontent.com/6639874/45267662-7a422d80-b479-11e8-92d9-f66e95c048e0.gif)

### 4. Refine the cutter shape 

1. Double-click the Sketch under the cutter
2. Refine as you like

![refine-the-cuts](https://user-images.githubusercontent.com/6639874/45267676-c3927d00-b479-11e8-84d2-50773c2ae013.gif)

### 5. Add more cutters in time

1. Add a new component, place accordingly. 
2. Create a binder for the new component, move into the `front-cutter`
3. Edit the Sketch under the cutter extrude 
4. All done, go to `enclosure`, refresh the view

![add-more-cuts](https://user-images.githubusercontent.com/6639874/45267929-08201780-b47e-11e8-82af-db39824790b5.gif)
