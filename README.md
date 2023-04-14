# Gantry Head Camera Offset (GHCO) Calibration

The Gantry Head Camera Offset (GHCO) Calibration is a process that is used to align the camera mounted on the gantry head with the TFPX module placement tool head. This calibration process is essential for ensuring that the placement tool head can accurately pick up and place the components.

## Why is GHCO Calibration Necessary?
The GHCO calibration process is necessary for several reasons:

**1. Component Placement Accuracy:** The GHCO calibration process ensures that the placement tool head can accurately pick up and place components, resulting in precise component placement and improved overall assembly quality.

**2. Reduced Assembly Time:** Proper GHCO calibration can reduce the time required for TFPX module assembly by reducing the number of placement errors and the need for manual corrections.

**3. Minimized Material Waste:** Precise GHCO calibration helps to minimize the amount of material waste during the assembly process, reducing costs and increasing efficiency.

## How to Perform GHCO Calibration
> **Important Note:** Before performing GHCO, make sure that the z-axis offset is correct. If you're not sure, please set all x-y-z axis as 0.0!! The configuration can be found in your flex config file as `geometry.tool_holder_offset` and you can set it as: `geometry.tool_holder_offset: {0.0,0.0,0.0}  ## If you are not sure!`

1. Ensure that the gantry head is homed and the tool holder is in place.
2. Position the Glass Heater onto its designated spot, as shown in Picture #1.
3. Launch the GScript application.
4. Load and execute the `Calibrate_GHCO_CUA.gscript` script.
5. Activate the crosshairs in the lower-left corner of the window once the camera feed appears.
6. Locate the cross mark within the circle on the glass heater by clicking on the screen and center the enabled red crosshairs.
7. Follow the prompts, and for each angle, manually relocate the glass heater to its initial location.
8. The Gantry Head Camera Offset (GHCO) calibration needs to be performed from 0 degrees to 90 degrees. The results will be saved in a log file named LOG_Calibrate_GHCO.txt, which will be located in the Logs folder.
9. Open a web browser and navigate to the following link: [Online Editor #1](https://www.jdoodle.com/python3-programming-online/ "Online Editor #1")
10. Open the ghcoFitScript.py script and copy all of its commands. Paste the copied commands into the editor on the web page.
11. In the editor, set the value of refPos to the same value as geometry.tool_holder_offset: in your flex config file.
12. Upload your LOG_Calibrate_GHCO.txt file using the upload button below the editor.
13. Execute the script. Note that you should try both methods, but the results labeled "Subtracted" are the ones you should try first.
14. Open a new browser tab and navigate to the following link: [Online Editor #2](https://www.w3schools.com/python/trypython.asp?filename=demo_ml_scatterplot "Online Editor #2")
15. Open the `ghcoPlotterScript.py` script and copy all of its commands. Paste the copied commands into the editor on the web page.
16. Copy all of the 10 x-y-z position information from the results obtained in step 13 and replace the data list in the editor on your second web page.
17. Run the script and save the image by right-clicking on the image.
18. Repeat these steps a few times until you achieve a delta value of less than 10 microns. Remember, fewer microns in the delta values indicate better calibration results.
