# CT Scanner

Some information such as the specific hardware being used is ommitted for confidentiality purposes. All following information is openly available to the public via the University of Idaho's EXPO student projects archive. 

## Key **Hardware** features include:

1. **Motor**: A stepper motor with a planetary gearbox was selected for precise angle control and increased rotation torque. Microstepping technology was implemented for smoother motion, which proved vital for image quality.

2. **Supporting Structure**: Aluminum sheet metal was chosen for the structure due to its lightweight, durability, and ease of post-processing for adjustments. The design allows for versatile configurations of system components and effective cable management.

3. **Power**: The system uses a USB-C Power Delivery (PD) compatible battery, providing different output voltages to accommodate the motor driver and microcontroller. The USB-C PD protocol allows for flexible power requirements.

4. **Circuitry**: An Arduino Nano was used as the microcontroller for its small size and sufficient data rate. The microstepping driver was chosen for its compact size and compatibility with the motor, fulfilling the system's weight requirements.


## Key **Software** features include: 

1. **Reconstruction Algorithm**: The team initially considered the Sheer-Warp algorithm but shifted to Filtered Back Projection (FBP) due to its applicability and documentation availability. FBP was chosen over Feldkamp Davis and Kress (FDK) due to implementation complexities.

2. **Image Acquisition**: Two methods were considered - start-stop and continuous rotation. The team chose continuous rotation for its simplicity. This approach required the operator to start and stop video capture on the x-ray machine, simplifying the process.

3. **Programming and Tools**: The software was developed in C++17, using Microsoft Visual Studio 2019 as the IDE. This decision was based on the team's familiarity with the tools and the need for a Windows-targeted development.

4. **Software Architecture**:
   - Input handling and command-line inputs managed through the REDACTED library.
   - Image input via REDACTED, using OpenCV for frame extraction and allowing for video trimming and orientation adjustment.
   - Preprocessing for Gamma Correction and Color to Grayscale conversion.
   - The main reconstruction phase involves creating sinograms, applying a sine filter, and reconstructing individual slices.

5. **Output Format**: The software outputs standard image files representing each slice of the object.

