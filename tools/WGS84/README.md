# WGS84
This directory contains information and tools concerning WGS84.

You can find more information at the *Office of Geomatics* website:
- https://earth-info.nga.mil/index.php?dir=wgs84&action=wgs84

I have also copied the information from this website directly into this README below because the website has been slow and/or unreliable.


### World Geodetic System 1984 Reference System
Brief Description: WGS 84 is an Earth-centered, Earth-fixed terrestrial reference system and geodetic datum. WGS 84 is based on a consistent set of constants and model parameters that describe the Earth's size, shape, and gravity and geomagnetic fields. WGS 84 is the standard U.S. Department of Defense definition of a global reference system for geospatial information and is the reference system for the Global Positioning System (GPS). It is compatible with the International Terrestrial Reference System (ITRS).

Definition:

- **Origin:** Earth’s center of mass being defined for the whole Earth including oceans and atmosphere.
- **Axes:**
    - Z-Axis = The direction of the IERS Reference Pole (IRP). This direction corresponds to the direction of the BIH Conventional Terrestrial Pole (CTP) (epoch 1984.0) with an uncertainty of 0.005″.
    - X-Axis = Intersection of the IERS Reference Meridian (IRM) and the plane passing through the origin and normal to the Z-axis. The IRM is coincident with the BIH Zero Meridian (epoch 1984.0) with an uncertainty of 0.005″.
    - Y-Axis = Completes a right-handed, Earth-Centered Earth-Fixed (ECEF) orthogonal coordinate system.
- **Scale:** Its scale is that of the local Earth frame, in the meaning of a relativistic theory of gravitation. Aligns with ITRS.
- **Orientation:** Given by the Bureau International de l’Heure (BIH) orientation of 1984.0.
- **Time Evolution:** Its time evolution in orientation will create no residual global rotation with regards to the crust.
- **Coordinate System:** WGS 84 follows the criteria outlined in the International Earth Rotation Service (IERS) Technical Note 36. The WGS 84 Coordinate System origin also serves as the geometric center of the WGS 84 Ellipsoid and the Z-axis serves as the rotational axis of this ellipsoid of revolution. WGS 84 geodetic coordinates are generated using its reference ellipsoid.
- **Defining Parameters:** WGS 84 identifies four defining parameters. These are the semi-major axis of the WGS 84 ellipsoid, the flattening factor of the Earth, the nominal mean angular velocity of the Earth, and the geocentric gravitational constant as specified below.



| Parameter                                                               | Notation | Value                             |
|-------------------------------------------------------------------------|----------|-----------------------------------|
| Semi-major Axis                                                         | a        | 6378137.0 meters                  |
| Flattening Factor of the Earth                                          | 1/f      | 298.257223563                     |
| Nominal Mean Angular Velocity of the Earth                              | ω        | 7292115 x 10-11 radians/second    |
| Geocentric Gravitational Constant (Mass of Earth’s Atmosphere Included) | GM**     | 3.986004418 x 1014 meter3/second2 |

** The value of GM for GPS users is 3.9860050x1014 m^3/sec^2 as specified in the reference below.


**Relationship to International Terrestrial Reference Frame:** The realization of a system into a frame is accomplished through the establishment of physical reference markers whose coordinates are consistent with its definition.  Following this model, the WGS 84 Reference Frame (WGS 84 RF) is made real through the Cartesian coordinates of the Antenna Reference Points at the NGA/USSF GPS Monitor Stations.  WGS 84 RF is aligned to ITRF to within one centimeter in each 3D component.  At this level, NGA states the two frames are coincident for positioning, navigation, and targeting.

The 7-parameter transformation from WGS 84-to-ITRF is zero in all components by design.  To support this claim two sets of metrics are provided:
1. The 7-parameter transformations between the IGS GPS Precise Ephemerides and the NGA GPS Precise Ephemerides with the view that each is a reflection of their underlying reference frames.
    - [Download IGS vs NGA](./IGS-vs-NGA.xlsx)
2. The offsets in Precise Point Positioning solutions using NGA GPS Precise Ephemerides to a subset of IGS stations’ coordinates as presented in the SINEX data.
    - Download SINEX Offsets (Not Available)

Reference:
- National Geospatial-Intelligence Agency (NGA) Standardization Document “Department of Defense, World Geodetic System 1984, Its Definition and Relationships with Local Geodetic Systems” Version 1.0.0] - [Download Directly](./NGA-STND-0036_1-0-0_WGS84.pdf)
    - This standard contains the authoritative definition of the World Geodetic System 1984 (WGS 84), which currently is the official NSG positional reference system. It defines the coordinate reference frame upon which all NSG coordinate systems (e.g. latitude/longitude/height; Military Grid Reference System) are based. It specifies the horizontal datum for all NSG mapping and charting, and provides parameters for transforming coordinates to other local horizontal datums. It provides precise coordinates of GPS tracking stations which form the basis of the WGS 84 coordinate reference frame. It defines the components of WGS 84, such as the ellipsoid (mathematical basis of coordinate systems); Earth Gravity Model (needed for elevation data, inertial navigation systems, etc.); and World Magnetic Model (needed for navigation and other applications). This document is an updated version of NIMA Technical Report 8350.2, Third Edition (4 July 1997).
    - https://nsgreg.nga.mil/doc/view?i=4085
        - (NGA.STND.0036_1.0.0_WGS84 available in NSG Standards Registry)
        