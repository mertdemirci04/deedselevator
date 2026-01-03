🚀 DEEDS Elevator Simulation - Quick Start Guide
This guide explains how to load, configure, and run the dual-processor elevator simulation in the DEEDS (Digital Electronics Education and Design Suite) environment.

📦 1. Required Files
Ensure you have the following files in your project folder:

Elevator_Circuit.pbs: The main DEEDS schematic file.

AsansorProjectDMC1.mc8: Assembly code for the Cabin Control (Left Processor).

AsansorProjectDMC2.mc8: Assembly code for the Floor Call Manager (Right Processor).

🛠 2. Setup and Execution Steps
Open the Circuit: Launch Deeds-DcS and open the .pbs schematic file.

Load Code into Processors:

For DMC1 (Left Processor): Right-click the processor chip → Select "Load Microcomputer Project". Load AsansorProjectDMC1.mc8, click Assemble, and ensure it is loaded into the ROM.

For DMC2 (Right Processor): Right-click the processor chip → Select "Load Microcomputer Project". Load AsansorProjectDMC2.mc8, click Assemble, and ensure it is loaded into the ROM.

Frequency Setting: Ensure the Clock component is set to a visible speed (e.g., 10 MHz or 1 MHz) depending on your CPU performance.

Start Simulation: Click the "Start Simulation" (F9) button in the top toolbar.

🎮 3. Operating Instructions
Once the simulation starts, the elevator defaults to Floor 0.

Calling the Elevator: Use the four push-buttons (0, 1, 2, 3) on the right side to request a floor.

Memory/Queue Tracking: When a button is pressed, the corresponding LED will turn ON. This indicates the request is stored in the DMC2 memory.

Monitoring Movement: Watch the 7-segment display on the left. It will update in real-time (0...1...2...3) as the cabin moves.

Arrival: Upon reaching the destination, the floor LED will turn OFF, and the cabin will wait for the next request in the queue.

Emergency Stop: Press the Emergency/Interrupt button to freeze the system. The display will show a dash (-). You must reset the simulation to clear this state.
