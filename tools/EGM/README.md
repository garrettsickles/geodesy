# EGM
This directory contains the tools necessary to generate EGM sample grids.

You can find more information at the *Office of Geomatics* website:
- https://earth-info.nga.mil/index.php?dir=wgs84&action=wgs84

I have also copied the information from this website directly into this README below because the website has been slow and/or unreliable.

---
## Earth Gravitational Model (EGM)
This division in the Office of Geomatics at NGA is responsible for collecting, processing, and evaluating gravity data (free-air and Bouguer gravity anomalies). These data are then used to compute gravimetric quantities such as mean gravity anomalies, geoid heights, deflections of the vertical, and gravity disturbances. All of these quantities are used in World Geodetic System 1984 support, navigation systems, mapping projects, and different types of surveys.

An Earth Gravitational Model (EGM) is set of geopotential coefficients used in a spherical harmonic expansion to create a global potential surface to coincide with Mean Sea Level (MSL). This surface is called a geoid and it fluctuates above and below the reference ellipsoid surface established by WGS 84. For more information, click on a drop-down menu item above on the EGM tab.

### Earth Gravitational Model 2008 (EGM2008)
The EGM84 and EGM96 are legacy products. Users are recommend to use the latest EGM from NGA, currently EGM2008. In 2020, NGA plans to release a new EGM, tentatively named EGM2020, where upon EGM2008 will become a legacy product.

The EGM2008 is provided as a set of normalized, geopotential coefficients complete to degree and order 2159, and contains additional spherical harmonic coefficients extending to degree 2190 and order 2159. Also provided is a 2.5-minute worldwide geoid height file, precomputed from the EGM2008. The coefficient and geoid height files have associated software and documents. EGM2008 was approved for official DoD use as documented in NGA STND.0036_1.0, 2014-07-08.

#### WHAT'S NEW
- April, 2013 - EGM2008 Citation included below with Links to reference EGM2008 and the EGM2008 Erratum are given on left under Additional Information.
- EGM2008 Citation: The development and evaluation of the Earth Gravitational Model 2008 (EGM2008) - Nikolaos K. Pavlis, Simon A. Holmes, Steve C. Kenyon, John K. Factor; Journal of Geophysical Research: Solid Earth (1978-2012) Volume 117, Issue B4, April 2012.
- May, 2009 - Global 2.5 Minute Geoid Undulation Grid available in GIS format.
- February, 2009 - Middle East Geoid Undulation Grid available in GIS format.
- February, 2009 - Propagated Error Estimates of EGM2008 released.
- January, 2009 - Utility to convert binary files from Big Endian to Small Endian released.
- January, 2009 - Gravity Anomalies & Deflections of the Vertical data released.
- November, 2008 - SMALL ENDIAN versions of binary files released.
- November, 2008 - Files & Products for Oceanographic Applications released.
- July, 2008 - WGS 84 version of EGM2008 released. Includes grids and programs for computing geoid undulations relative to WGS 84 Ellipsoid.

### Earth Gravitational Model 1996 (EGM96)
The EGM84 and EGM96 are legacy products. Users are recommend to use the latest EGM from NGA, currently EGM2008. In 2020, NGA plans to release a new EGM, tentatively named EGM2020, where upon EGM2008 will become a legacy product.

The EGM96 is provided as a set of normalized, geopotential coefficients to degree and order 360. Also provided is a 15-minute worldwide geoid height file, precomputed from the EGM96. The coefficient and geoid height files have associated software and documents. EGM96 was approved for official DoD use as documented in NIMA TR8350.2, Third Edition, 4 July 1997.

### Earth Gravitational Model 1984 (EGM84)
The EGM84 and EGM96 are legacy products. Users are recommend to use the latest EGM from NGA, currently EGM2008. In 2020, NGA plans to release a new EGM, tentatively named EGM2020, where upon EGM2008 will become a legacy product.

The EGM84 is provided as a set of normalized, geopotential coefficients to degree and order 180. Also provided is a 30-minute worldwide geoid height file, precomputed from the EGM84. The coefficient and geoid height files have associated software and documents. EGM84 was approved for official DoD use as documented in DMA TR8350.2, Second Edition, 1 September 1991.
