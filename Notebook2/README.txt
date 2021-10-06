Instrument: MIRI
Mode(s): MRS
Data Level: Lvl1b, 2a, 2b, 3
Source of Simulations (Version): mirisim 2.4.0
Pipeline Used: v1.3.2
Data Location: https://stsci.box.com/s/kdzsylowpp5q6herx4hc23noc9z71z0f

Target Description: Mock point source with a realistic science spectrum, 4-pt POINT SOURCE dither, and sky/telescope background
Detector Configuration:
Subarray(s): FULL
Filter(s): All MRS bands (1A-4C)
Readout(s): SLOW
Groups/Ints/Exposures: 20/1/4
Dithers: Standard 4-point dither

Detailed information:

Data Issues:
mirisim has multiple known issues that impact data quality and require either careful simulation design or pipeline workarounds.  These include:
(1) FAST mode has incorrect noise properties, rendering FAST mode data processed by the pipeline unreliable.  These simulations thus use SLOW mode.
(2) Extended sources are not simulated unless they meet a minimum size that varies with each band.
(3) Point sources are not simulated properly, with the PSF profile being simulated incorrectly in the cores.  These simulations therefore should not be used to study the PSF shape.
(4) Reference pixels are not treated consistently, the refpix step of detector1 must therefore be turned off to process mirisim data without artifacts.
(5) Channel 4 flux calibration is incorrect.  No workaround available- channel 4 fluxes will be incorrect.
(6) WCS alignment is incorrect, sources jump in location by a couple of pixels between channels.  No workaround available- do not use mirisim data to test spatial alignment.
(7) Flux conservation is not perfect within mirisim. Likewise, the aperture correction factors in use by the pipeline correspond to the expected performance in flight (to be udpated during on-orbit commissioning) and are not well matched to mirisim data. No workaround available, do not use mirisim data to test flux conservation.
(8) mirisim does not add all of the necessary header keywords for the pipeline to know how to do background subtraction, identify source type, etc. In order to get these APT-derived keywords correct they will need to be set manually.
The pipeline has a few issues than can impact data quality without workarounds.  These include:
(1) Straylight step is designed for flight data and does not interact well with mirisim data.  Since simulated data have no straylight, this step should be skipped.

List of Data Files: Many, in stage0/, stage1/, stage2/, stage3/ subdirectories

List of Extensions: .fits, _rate.fits, _cal.fits, _s3d.fits, _x1d.fits, and other intermediate stages

Other Notes: Simulated data and pipeline outputs for MRS Notebook 2 (https://github.com/STScI-MIRI/MRS-ExampleNB/tree/main/Notebook2), a version of which will be part of JWebbinar #5 (IFU mode overview).
