# Description

Example project to demonstrate cutting socket windows. Usage scenario: 

- [ ] You have a circuit with connectors on it.
- [ ] Create an enclosure for that circuit, arrange the placement with assembly container. 
- [ ] Cut the connector windows 
- [ ] Relocate circuit inside enclosure, **expect** the connector window cuts are relocated accordingly. 
- [ ] Place additional circuits inside the enclosure 
- [ ] Create additional window cuts without breaking previous work.
- [ ] Refine the window cuts without breaking any previous work.

# Status 

Work In Progress

# Instructions

> Original Tutorial is [here](https://github.com/realthunder/FreeCAD_assembly3/wiki/Modeling-using-Assembly)

Instructions to window cut for the connector in the `panel` 

1. Import the circuit or draw from scratch if it doesn't exist yet

2. Draw panel

  1. Go to PartDesign
  2. Draw rectangle 
  3. Pad 
  
???3. Create an assembly container to hold the circuit and the panel, optionally make the positioning (optionally by creating some constraints)

1. Select the object face on the circuit you want to create the cut for connector 

2. Go to `Sketcher` workbench, click "Create a new sketch" button

![image](https://user-images.githubusercontent.com/6639874/43920382-76b50f7c-9c21-11e8-818c-2fffbfb128b9.png)

3. Draw the cuts' footprints.

4. Go to `Part` workbench, extrude the cut footprints (preferably select the "symmetric" checkbox) (label this `panel-cut`)


------------------------------







??? add panel-cut into the same asm-container with the circuit 

5. Select `panel-cut`, go to `Part Design`, click "sub-shape binder"

6. Select `panel` and `Binder`, go to `Part` workbench, click "cut". (label this cut as `panel-part`)



7. Select `panel-cut` and make it invisible

8. Create new Asm3 container, select `pcb`, `socket-part` and `panel-part` and drop into this Asm3 container. 

# Updating cut shape 
TODO 
# Updating panel position
TODO
