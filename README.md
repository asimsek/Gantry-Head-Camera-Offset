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
8. You need to perform GHCO from 0 degrees to 90 degrees. The results will be saved in your GHCO log file under `Logs/LOG_Calibrate_GHCO.txt`.
9. Open your browser and go to this link: [Online Editor #1](https://www.jdoodle.com/python3-programming-online/ "Online Editor #1").
10. Copy all the commands from the `ghcoFitScript.py` script and paste them into the editor on the web page.
11. Set the `refPos` as in `geometry.tool_holder_offset:` in your `flex_config` file.
12. Use the upload button below and upload your `LOG_Calibrate_GHCO.txt` file.
13. Execute the script (try both, but `Subtracted` results are the ones you need to try first).
14. Open a new browser tab and go to this link: [Online Editor #2](https://www.w3schools.com/python/trypython.asp?filename=demo_ml_scatterplot "Online Editor #2").
15. Copy all the commands from the `ghcoPlotterScript.py` script and paste them into the editor on the web page.
16. Copy all the 10 x-y-z position information from the ghcoFitScript.py results and replace the data list on the editor on your 2nd web page.
17. Run the script and save the image by right-clicking on the image.

