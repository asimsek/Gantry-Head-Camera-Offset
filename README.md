# Gantry Head Camera Offset (GHCO) Calibration

The Gantry Head Camera Offset (GHCO) Calibration is a process that is used to align the camera mounted on the gantry head with the TFPX module placement tool head. This calibration process is essential for ensuring that the placement tool head can accurately pick up and place the components.

##Why is GHCO Calibration Necessary?
The GHCO calibration process is necessary for several reasons:

**1. Component Placement Accuracy:** The GHCO calibration process ensures that the placement tool head can accurately pick up and place components, resulting in precise component placement and improved overall assembly quality.
**2. Reduced Assembly Time:** Proper GHCO calibration can reduce the time required for TFPX module assembly by reducing the number of placement errors and the need for manual corrections.
**3. Minimized Material Waste:** Precise GHCO calibration helps to minimize the amount of material waste during the assembly process, reducing costs and increasing efficiency.

## How to Perform GHCO Calibration
>**Important Note:** Before performing GHCO, make sure that the z-axis offset is correct. If you're not sure, please set all x-y-z axis as 0.0!! The configuration can be found in your flex config file as geometry.tool_holder_offset and you can set it as: `geometry.tool_holder_offset: {0.0,0.0,0.0}  ## If you are not sure!`

1. Position the Glass Heater onto its designated spot, as shown in Picture #1.
2. Launch the GScript application.
3. Load and execute the "Calibrate_GHCO_CUA.gscript" script.
4. Activate the crosshairs in the lower-left corner of the window once the camera feed appears.
5. Locate the cross mark within the circle on the glass heater by clicking on the screen and center the enabled red crosshairs.
6. Follow the prompts, and for each angle, manually relocate the glass heater to its initial location.


