# Introduction #

In order to capture the usual red, green, and blue (and IR) channels in a scanned image, each channel must be captured separately. This is usually done with a Bayer filter (filtering light at the destination), but it can also be done at the light source, so long as it is possible to make multiple captures. Each of these selections of the light spectrum are referred to as modes here.

# Filter Wheel #

If a full spectrum light source is used, then a filter can be placed in front of it that only allows the desired light spectrum through. If these filters are mounted on a wheel, then that wheel can be mounted to a stepper motor, and numbered steps can be assigned to each filter.

This approach is best for a light source that takes a relatively long time to stabilize, such as a lightbulb. The drawback is that even with a robust and fast mechanism for rotating the filter wheel, it will still take a significant amount of time to switch between each channel. This really adds up for monochrome line sensors, but is not as big of a deal for area sensors.

# Switchable LEDs #

If an array of LEDs with each desired spectrum are wired in groups in such a way that they can be turned on and off by their spectrum, then no mechanical parts are needed, and the unit cannot fail for mechanical reasons. If the LEDs come to full power and stabilize very quickly, then the full cycle of light modes can be run through much more quickly. This is critical for rapid multichannel capture with a line sensor.