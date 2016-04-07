# Introduction #

The point of this document is to present simple way to move a strip of a define amount while keeping it in front of light source.
The first objective is to automatize the process "DSLR" scanning process.

The imaging device and the processing of the images will be discussed in another part of the project.


# Film gate with rollers #

The idea is to have a simple film gate that include a film guide. The strip will be fed into the film guide thanks to a transportation system.

## Simple motor solution ##
The transportation system will be made of a motor roller and a pinch roller.
The used motor could be http://42bots.com/tutorials/28byj-48-stepper-motor-with-uln2003-driver-and-arduino-uno/

While the motor and pinch roller could be the one from :
https://www.youmagine.com/designs/35mm-film-scanning-elements

The diameter of the rollers is a compromise of speed/stepping accuracy and ease to feed the strip in the film guide (larger diameter prevents to be close to the guide)

## Double motors solution ##

Another solution will be to motorize each roller to allow for a more straight trajectory of the film when leaving the rolls.

To be detailed.