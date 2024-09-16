						Readme
INSTRUCTIONS:

For help or questions regarding the use of this product, 
please contact:

National Imagery and Mapping Agency
ATTN: John Factor
DOGIGB3/L-41
3200 South Second Street
St. Louis, MO  63118-3399

This package contains 3 files:
1. WGS84 (data file of geopotential harmonic coefficients)
2. ClenGui.exe (executable file)
3. README (Instructions to use the executable)

Procedure: 
1. Go to the directory where the wgs84 zipped file was stored.

2. Double click on the wgs84 zipped file.

3. Inside the winzip window click on the extract button. Inside 
   the extract window enter a directory name and extract
   the three files to the same directory.

4. Go to the above entered directory.
 
5. If desired, create a shortcut for the executable and drag
   the shortcut to the desktop.

6. Double click on the blue NIMA WGS84 icon to run the program.

7. A message window will pop up when the coefficients from
   file WGS84 are read in. Press "OK". If the coefficients cannot
   load, a message will appear.

8. A second message window will pop up when the coefficients
   are read in. Press "OK".

9. A menu will appear. Enter latitude/longitude for the desired 
   geoid height in degrees, minutes, and seconds.

10. Press "Run" to compute the geoid height (a height anomaly is 
   computed if the geodetic height is not zero).

11. Press "Clear All" to clear the input boxes.

12. Press "Close" to exit the application.

**************   WARNING  *******************************
*
* Use zero for the geodetic height if the 
* geoid height is desired.
*
*********************************************************

Comments:

1.  For southern or western hemispheres, the user need only
    to apply a negative sign to the degrees.
	The negative sign will automatically get applied
    to the minutes and seconds components.
	The user can also apply the negative signs during input.  

2.  This program will not compute a geoid at +/- 90 degrees
    latitude, rather the latitude is internally changed to 
	+/- 89.9999999... instead.