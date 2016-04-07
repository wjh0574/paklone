# Introduction #

Surface defects absorb infrared (IR) light. Film base and emulsion do not. If you capture both visible and IR mask from a film image, then the IR mask can be used to instruct an algorithm on where to replace image information. Here this is called Infrared Defect Removal (IDR)

For each kind of light you are trying to separately capture, you need to filter out the light you do not want to capture. You can filter it at the light source, which makes it possible to capture using a monochrome sensor, so long as it is sensitive to each kind of light. You can filter it just before it gets to the sensor, but most of those filters are directly attached to the sensor, which means you might to remove that filter, or use an additional sensor that does not have that filter.

There are two ways of selecting the light that you want to capture:

  1. Use a full spectrum light source and then filter out what you don't want. This would mean using a filter wheel.

> 2) Use multiple light sources that each emit only a single kind of light. This would mean using an array of LEDs (for example), such as red, green, blue, and infrared.

Both of these approaches will be referred to as a ModalLight.

# Line Sensor #

The way to implement IDR with a line sensor that would give the greatest speed of capture would be to have two different line sensors: one with a Bayer filter, and one with an IR pass filter. There would be no need for a ModalLight, so for each advance of the film, one capture is made with each sensor.

The second fastest way is to use one Bayer filtered sensor that is IR sensitive, and to use a ModalLight with two modes: visible light and IR. There would be two captures by a single sensor per film advance.

The slowest way is to use a monochrome sensor that is sensitive to visible and IR light, and to use a ModalLight with 4 modes: red, green, blue, and IR. There would be four captures by a single sensor per film advance.

# Area Sensor #

For highest speed of capture, the simplest way to implement IDR with an area sensor is to use a Bayer filtered, IR sensitive area sensor with a ModalLight that has modes for visible and IR light. There would be 2 captures by a single sensor per film advance.

For highest image quality, use a monochrome sensor with visible and IR sensitivity and a ModalLight. There would be 4 captures by a single sensor per film advance.

While not ideal as it would be significantly more complicated to execute, it is possible to use both an area sensor and a line sensor. In that case, a Bayer filtered IR insensitive area sensor and an IR only line sensor would be carefully aligned to each other, and a non-modal full spectrum light source would be used. The line sensor would perform its captures while the film is advancing for alignment with the area sensor.

# IDR for Kodachrome and/or B&W silver film #

It might be possible to mount a separate line sensor at an angle to the film surface, and bounce a useful spectra of light off of the film surface from the same side as the film. If done exactly right, it might provide a mask with enough useful data for surface defect removal on one side. An additional sensor would have to be used for the opposite side.