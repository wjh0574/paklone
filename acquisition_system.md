# Introduction #

Figure out what sensor platform will be used. Everything else is either a "solved problem" (a good film transport can be designed by any competent mechanical engineer) or dependent on the sensor platform that is chosen.
Sensor must have good imaging properties and a well documented interface. An actual API if possible. What are good imaging properties to look for in a sensor?
Area sensors are preferable to line sensors, unless there is a prohibitive price difference. For example, the Fuji Frontier SP-3000 uses an area sensor.

The imaging device is not intened to give a perfect accuarcy of the film corlor, but ratyher to ensure the repeatability of the scanning process.

# Device #
## Protopying ##

For the prototype / entry level Paklone, Canon looks to be the best choice in terms of hackability.
- The Powershot series can be tweaked with CHDK for those on a very tight budget, and a second hand microscope eyepiece could possibly be used as a diopter for a non-interchangeable lens. Probably only useful for B&W scans.
- Canon DSLRs can be seriously enhanced with Magic Lantern, which also has an API for writing simple scripts or advanced extensions. We might be able to create a significant amount of logic in a very short time with a Magic Lantern script.

- Another interresting project is the gphoto2 program, that run on raspbery pi. Gphoto2 allows (on some camera) to configure, shoot and retrieve the pictures. The list of supported camera is : http://www.gphoto.org/doc/remote/ .
The retrieval of the camera is non-mandatory, but could be interresting for using the wifi of the raspberrypi (as a file server).


## Final specs ##
Far far in another time ;)