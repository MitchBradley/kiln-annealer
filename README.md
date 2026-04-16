# Annealing Kiln Controller

This is the software for a temperature controller for a kiln
that is used to anneal brass rods for my Honu Putter production.
The brass rods need to be annealed before they are bent into a U shape,
otherwise they often break.

The kiln is a small jewelry kiln that runs on 110V.  A thermocouple
measures the inside temperature.  There is a solid state relay (SSR)
to switch the power.

The controller is an ESP32 with a MAX31855 module for reading
the thermocouple, using a GPIO to switch the SSR.

The software is a Python script that monitors the temperature
and controls the SSR to implement the desired temperature profile.

The temperature profile is very simple - when the controller is
powered on, the SSR is turned on
