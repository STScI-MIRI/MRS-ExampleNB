# MRS-ExampleNB
Example notebooks for processing MRS data with the JWST pipeline.  This includes both notebooks that should be used for real flight data, and older ground notebooks to be used with pre-flight simulated data.

Flight Notebooks:

Flight Notebook #1: Batch processing for a typical MRS scene
* Requires pipeline version 1.8.0+
* Based on MRS ERO observations in Stephan's Quintet (APT 2732)
* 4-pt dithered MRS data with dedicated background
* 3 grating settings for full wavelength coverage
* Processes through Detector1, Spec2, and Spec3

A previous Flight Residual Fringe notebook has been removed now that the residual fringe correction step
has been included in the main jwst pipeline as of version 1.8.0.

Ground Notebooks:

Ground Notebook #1: Detailed Spec2/Spec3 Walkthrough
* 4-pt dithered point sources observations, SHORT grating setting, Ch1/Ch2 only
* A version of this notebook is included in the JWebbinar Series (JWebbinar 4: Intro to JWST Spectrocopic Mode)

Ground Notebook #2: Multiband and Parallel Processing Demo (Point Sources)
* 4-pt dithered point sources observations, all MRS bands (1A-4C)
* A version of this notebook is included in the JWebbinar Series (JWebbinar 5: Intro to JWST IFU Mode)

Ground Notebook #3: Extended Source Demo
* 4-pt dithered extended-source observations plus dedicated background, SHORT grating setting (Ch1A, Ch2A, Ch3A, Ch4A)
