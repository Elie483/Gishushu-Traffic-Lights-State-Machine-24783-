# Gishushu-Traffic-Lights-State-Machine-24783-
Description of the Gishushu Traffic Lights State Diagram:
This state diagram represents the behavior of a traffic light system at an intersection, which includes handling both vehicle and pedestrian traffic.

Main States:
Green State:

When the traffic light is green, vehicles are allowed to move.
The Green state contains two substates:
Active: Vehicles are moving, and the green light is on.
Yellow: This is the transition phase where the yellow light warns drivers to prepare to stop.
The system transitions to the Yellow substate when the timer for the green light expires, indicating that the green light will change soon.
Yellow State (Substate of Green):

Warning: The yellow light is on, signaling vehicles to slow down and prepare to stop.
After a short duration, when the timer expires, the system moves out of the Yellow state and enters the Red state.
Red State:

This is the state where vehicles must stop, as indicated by the red light.
The Red state also manages pedestrian traffic, allowing people to cross the road safely when they press a button.
The Red state contains two key phases:
Waiting: The red light is on, and vehicles are stopped.
PedestrianCross: This substate is entered when a pedestrian presses the crosswalk button, and pedestrians are allowed to cross.
Substates in the Red State:
Waiting: This is the default substate of Red. It indicates that the traffic light is red, and vehicles are stopped.
PedestrianCross: When a pedestrian presses the button, the system transitions to this substate. It has the following subphase:
Crossing: Pedestrians are actively crossing the road. This state is active while the pedestrian light is on, allowing safe crossing. After the pedestrian cross timer expires, the system returns to the Waiting state, stopping pedestrian movement.
Transitions:
The system transitions between states based on timers and pedestrian actions:
Green to Yellow: After the green light’s timer expires, the system moves to the Yellow state to warn drivers.
Yellow to Red: After the yellow light’s timer expires, the system transitions to the Red state, stopping vehicle traffic.
Red (Waiting) to PedestrianCross: When a pedestrian presses the crosswalk button, the system transitions to PedestrianCross, allowing pedestrians to cross.
PedestrianCross to Waiting: After the pedestrian cross timer expires, the system returns to the Waiting state where the red light remains active for vehicles.
Red to Green: Once the red light’s timer expires and there are no pedestrians crossing, the system transitions back to the Green state, restarting the cycle.
System Behavior:
The traffic light alternates between controlling vehicle movement (Green, Yellow) and pedestrian movement (PedestrianCross in Red).
The system ensures that vehicles stop when pedestrians are crossing and resumes vehicle movement once the pedestrians are finished.
