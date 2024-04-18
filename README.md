# FSM-protype
THIS is not the final FSM scripts ?
To create a Finite State Machine (FSM) for your VR walking speed research, you can use the following states and transitions:

1. Default:
   a. Load the VR environment in Unity.
   b. Set the sphere's height in front of the user.
   c. Transition: Press the space key to go to the "Pre-trial" state.

2. Pre-trial:
   a. Adjust the VR headset and make sure everything is properly strapped on.
   b. Perform eye calibration.
   c. Prepare to collect data.
   d. Have the user walk to the starting spot.
   e. Transition: Press a controller button on the VR headset to proceed to the "Trial" state.
   f. Extra: If the user is redoing the experiment, skip part "a."

3. Trial:
   a. Call the "Do Sphere Stuff" script coded by my friend, which controls the sphere's behavior based on the user's walking speed.
   b. Transition: Check to see if the trial is complete, and if so, save the data.
   
4. Post-trial:
   a. Every 5 trials, administer a survey asking how the user feels, primarily to check for VR motion sickness.
   b. Transition: Press a controller button on the VR headset to return to the "Pre-trial" state, allowing for the experiment to be redone.

Here's a visual representation of the FSM:

```
         +-----------+        +------------+
         |  Default  |--------|  Pre-trial  |
         +-----------+        +------------+
              |                   |   |   
              |                   |   |   
              |                   |   |   
              |                   |   |   
              |                   |   |   
              v                   |   |   
         +-----------+             |   |   
         |   Trial   |-------------+   |   
         +-----------+                 |   
              |                       |   
              |                       |   
              |                       |   
              |                       |   
              |                       |   
              v                       |   
         +-----------+                 |   
         | Post-trial |-----------------+   
         +-----------+
```

This FSM represents the flow of your VR walking speed experiment, allowing you to guide participants through various stages while monitoring their walking behavior and collecting data.
