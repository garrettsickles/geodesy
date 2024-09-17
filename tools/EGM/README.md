# EGM
This directory contains the tools necessary to generate EGM sample grids.
I generated the interpolation grids on Windows 11 using the exact precompiled EXE and data files provided by NGA.
You may try to use a Windows Fortran compiler or `gfortran` to compile the executable binaries from source, but I noticed the output DAT files were not identical between the two methods for the same input file and therefore chose to use the NGA provided binaries.

C Style header files containing 60 Minute (1 Degree) and 15 Minute samples are available in the following files:
- `EGM1984_30MIN.h`
- `EGM1996_60MIN.h`
- `EGM1996_15MIN.h`
- `EGM2008_60MIN.h`
- `EGM2008_15MIN.h`

The raw output sampled grids are also available in the specific version folder:
- `EGM1984/WWGRID.TXT` (30 Minute Sampling)
- `EGM1996/OUTF477.60MIN.DAT`
- `EGM1996/OUTF477.15MIN.DAT`
- `EGM2008/OUTPUT.60MIN.DAT`
- `EGM2008/OUTPUT.15MIN.DAT`

## EGM1984
You may attempt to generate you own EGM1984 grid using the source in `EGM1984/clenqt.for`.
NGA provides a 30 Minute interpolation grid in `EGM1984/WWGRID.TXT` which I have also converted into a C Header file.

## EGM1996
Example generation of the EGM1996 sample grid.

### Generating `EGM1996` Output files (Windows)
```shell
> cd .\tools\EGM\EGM1996\
> cp ..\INPUT_01DEG.DAT .\INPUT.DAT
> .\F477.exe
1

 MAXIMUM DEGREE = 360
 
> mv .\OUTF477.DAT .\OUTF477.60MIN.DAT
> cp ..\INPUT_15MIN.DAT .\INPUT.DAT
> .\F477.exe
1

 MAXIMUM DEGREE = 360
 
> mv .\OUTF477.DAT .\OUTF477.15MIN.DAT
```
## EGM2008
Example generation of the EGM2008 sample grid.

### Generating `EGM2008` Output files (Windows)
```shell
> cd .\tools\EGM\EGM2008\
> cp ..\INPUT_01DEG.DAT .\INPUT.DAT
> .\hsynth_WGS84.exe


c-----------------------------------------------------------------------


                              Execution


c-----------------------------------------------------------------------


               Constants Used in the Expansion
               -------------------------------


               Defining Constants for the GRS:

               ae     =   0.637813700000D+07   (m)
               C(2,0) =  -0.484166774985D-03          zero value
               gm     =   0.398600441800D+15   (m**3/S**2)
               omega  =   0.729211500000D-04   (rad/s)


               Derived Constants for the Zero-Type Ellipsoid:

               J2     =   0.108262982131D-02          zero value
               1/f    =   0.298257223571D+03          inverse flattening
               b      =   0.635675231425D+07   (m)    semi-minor axis
               e2     =   0.669437998996D-02          first eccentricity squared
               geqt   =   0.978032533590D+06   (mGal) equatorial gravity
               gpol   =   0.983218493786D+06   (mGal)      polar gravity
               k      =   0.193185265241D-02
               m      =   0.344978650684D-02


               Ref. Gravity Potential Even Zonal Terms (C-form)
               Subtracted From the Input Coefficients:

               C( 2,0) =  -0.484166774985D-03
               C( 4,0) =   0.790303733524D-06
               C( 6,0) =  -0.168724961164D-08
               C( 8,0) =   0.346052468485D-11
               C(10,0) =  -0.265002226377D-14
               C(12,0) =  -0.410790140988D-16
               C(14,0) =   0.447177356743D-18
               C(16,0) =  -0.346362564558D-20
               C(18,0) =   0.241145603096D-22
               C(20,0) =  -0.160243292770D-24


c-----------------------------------------------------------------------


               Output Quantity
               ---------------


               Computation for isw =  82:


               Geoid Undulation ............................(m).


               Excluded Data Flag =      9999.00


               Gravitational Model: EGM2008_to2190_TideFree

               (Lmin =    2     Lmax = 2190).

               aegm  =   0.637813630000D+07   (m)
               gmegm =   0.398600441500D+20   (m**3/S**2)

               Tide Free C(2,0) =  -0.484165037152D-03 (Input from File)
               Zero Tide C(2,0) =  -0.484165037152D-03 (Used in Synthesis)
                   Delta C(2,0) =   0.000000000000D+00 (Transformation)


               Correction Model: Zeta-to-N_to2160_egm2008

               (Jmin =    0     Jmax = 2160).


               Correction to height anomaly computed from spherical
               harmonic model.


c-----------------------------------------------------------------------


               Output at Scattered Points
               --------------------------


               Scattered Coordinate File: INPUT.DAT


                    Lat.        Lon.           N

                   -90.000000 -180.000000    -30.150
                   -89.000000 -180.000000    -30.070
                   -88.000000 -180.000000    -29.141
                   -87.000000 -180.000000    -30.551
                   -86.000000 -180.000000    -31.592
                   -85.000000 -180.000000    -35.681
                   -84.000000 -180.000000    -42.490
                   -83.000000 -180.000000    -46.427
                   -82.000000 -180.000000    -48.010
                   -81.000000 -180.000000    -50.150


c-----------------------------------------------------------------------


               Total number of points    =  65341


c-----------------------------------------------------------------------


               ASCII Output File : OUTPUT.DAT


c-----------------------------------------------------------------------


                           Normal Termination


c-----------------------------------------------------------------------


> mv .\OUTPUT.DAT .\OUTPUT.60MIN.DAT
> cp ..\INPUT_15MIN.DAT .\INPUT.DAT
> .\hsynth_WGS84.exe
1

 MAXIMUM DEGREE = 360
 
> mv .\OUTPUT.DAT .\OUTPUT.15MIN.DAT
```

### Reference
You can find more information at the *Office of Geomatics* website:
- https://earth-info.nga.mil/index.php?dir=wgs84&action=wgs84

I have also copied the information from this website directly into this README below because the website has been slow and/or unreliable.

```
Pavlis, N.K., S.A. Holmes, S.C. Kenyon, and J.K. Factor, An Earth Gravitational Model to Degree
2160: EGM2008, presented at the 2008 General Assembly of the European Geosciences Union,
Vienna, Austria, April 13-18, 2008.
```

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
