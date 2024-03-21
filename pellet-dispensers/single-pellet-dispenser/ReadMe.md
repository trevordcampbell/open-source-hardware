Pellet Dispenser ReadMe

This assembly contains the design for a pellet dispenser. It can be used and adjusted to dispense a single pellet of adjustable shape and size.

Catalogue of Parts:

- Hopper Tank
- Hopper Tank Cover
- Motor Mounting Plate
- Rotating Plate with Pellet Dispensing Slots
- Pellet Slot Blocker
- Pellet Outlet Track
- Base Stand
- Motor Cover Plate  (optional)
- IR Break Beam Unit Mounting Plate  (optional)
- Pellet Outlet Track Mounting Plate  (optional)

*Not Modeled Yet:

- Pellet Receiving Tray / Bowl
- Pellet Routing Track to deliver pellets from Dispenser to Receiving Tray / Bowl


Design Info:

- Parts designed in Metric / MMGS

----------------------------------------
TO-DO:

- Model the Pellet Receiving Tray / Bowl
	- Receiving tray / bowl could be placed inside of a seat which contains slots for each Routing Track to insert

- Model the Pellet Routing Track (which delivers pellets from the dispenser to the receiving bowl)
	- Figured routing track could be bent out of thin sheet metal (just a rectangular track with 90deg bent sides)

----------------------------------------
Major Design Considerations:

- Try to make design adjustable / modular such that it could handle a pellet of any dimension or shape

- Try to ensure that only a single pellet is dispensed at a time

- Try to prevent jamming of pellets within the system

- Try to ensure pellets are contained within a fully enclosed system until the time which they are dispensed (failed due to pellet slot blocker mounting strategy)

- Try to make design fully modular and easily manufactured via traditional machining methods OR 3D printing

- Try to make design simple to assemble and take apart

----------------------------------------
Design Structure & Methodology

- This assembly was modeled in top-down fashion, using a shared "variables&equations" file used in all parts to drive dimensions for each part (this "variables&equations.txt" file can be found included with the assembly, and should be imported and linked for each part)

- An attempt was made such that the assembly and all subsequent parts are highly flexible to change driven by the values of the "variables&euqations.txt" file. If parameters need to be changed, they can be changed in the singular shared file and will propagate to all parts in the assembly. The models are flexible and should not break in most variable change cases (although you might expect some fillets and things to break depending on the variable and magnitude of change)

- Parts do contain external references to other parts in the assembly

- The design was attempted to be implemented such that it could be mostly agnostic to manufacturing method, whether it will be machined or 3D printed. Obvious optimizations are available if a specific machining method will be chosen, such as enhancing part mounting strategy

- Because it was modeled top-down in the context of the assembly to start, a couple of the parts have their part bodies extraneous to their part origins
	- Pellet Slot Blocker
	- Hopper Tank Cover
	- Pellet Outlet Track

- An attempt was made to make the total design modular, such that some parts are optional and all parts are adjustable as needed

----------------------------------------
Important Notes:

- Some parts which contact or fit into others have been modeled with a "generalFittingTolerence" variable included in their measurement, to ensure the parts have less risk of contacting in an undesirable way. If this is not something you want to consider, you can simply set the value of "generalFittingTolerence" to be 0

- All of the holes used for mounting purposes are modeled as simple dowel throughholes for now. Mating and mounting parts will be simplest using a bolt and nut for each hole. Not worrying about threading holes for now (parts have been designed to mate and mount with gentle compression alone)

- All of the holes used for mating and mounting purposes are created as Assembly-level hole-wizard features, propagated down to each part required.

- Even if you will be machining parts out of metal, a few of the parts should probaly be 3D printed regardless, given the nature of their usage / their design / their difficulty to machine with traditional methods:
	- IR Beam Mounting Plate
	- Pellet Outlet Track Mounting Plate
	- Pellet Outlet Track
	- Pellet Slot Blocker
	- Rotating Plate

----------------------------------------
Critical Measurements to Check & Variables to Adjust Before Manufacturing:

- Pellet size & dimensions

- Motor dimensions

- IR Beam Unit Dimensions

- Diameter of rotating plate / hopper base / hopper tank

- Value for the "generalFittingTolerance" variable

----------------------------------------

Ideas for Futher Improvements to the Design:

- Not sure how strong motor will have to be in order to turn the rotating plate / agitator in the case where it is fully immersed in pellets and the tank is full. It could require a lot of torque... but then you also don't want too much torque to damage the pellets. That could potentially be solved by making the agitator blades much smaller, or by removing them entirely.

- I do not like the strategy for mounting / adjusting the pellet slot blocker component inside of the hopper tank, since it leaves a small exposed gap in the mounting slot where the interior of the hopper is exposed. I'm still trying to think of a better way to do this in a modular / adjustable fashion...

- The bulk of the hopper tank (the straight-pipe section) above the hopper base chamfer could potentially be extracted as a separate part from the hopper base (this could make the base and tank more modular, or make machining simpler)

- The "Agitator" portion of the rotating plate could potentially be extracted as a separate part from the rotating plate (this could make the rotating plate / agitator more modular, or make machining simpler)

- Currently the rotating plate attaches directly to the motor spindle. If a gear is affixed over the spindle, that gear mounting hole will have to be modeled into the bottom of the rotating plate

- Think of a better way to attach pellet outlet track to the motor mount

- Think of better approach to the base stand, such that it can be height adjustable as needed

- Fix the components with their part bodies extraneous to their part origins as a consequence of top-down design strategy

- Could remove external references from all parts and have complete geometry driven by the shared "variables&equations.txt" file (this will require more work)
