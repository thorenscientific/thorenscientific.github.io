Table of Contents
=====================

Stream of Consciousness Brainstorm for a table of contents.

Data Converter History
----------------------

* Fluff chapter with some interesting architectures.
* Potentiometer servo ADC
* Kelvin-Varley Divider (don't forget Williams' references)
* DAC with external deglitcher

Fundamentals of Sampled Data Systems
------------------------------------

dt * dv/dt = dv... it's the law!

* Toolbox Items
   * Data sources and sinks
   * Analog signal sources and sinks
   * Hardware for converter testing
      * ADALM2000
      * Sound Card
      * ADALM-Pluto
      * Clock sources

Analog to Digital Converters
----------------------------

* ADC Architectures
   * SAR (Modern, q noise lower than thermal noise)
   * RF (Beyond typical pipeline)
   * Multi-slope

* Testing ADCs
   * Overview of commercial production Testing Techniques
   * Practical techniques
   * Reference Noise: Broadband
   * Reference Noise: Amplitude Modulation
   * Reference Noise: "Noisy Wire" techique



* ADC Circuit Techniques
   * Correlated Double sampling and AC excitation (LTC2415 datasheet, AN96)
   * Transparent, cotinuous low-noise gain and offset calibration from noisy calibration readings (AN112)
   * Multitone narrow-band detection (FTC colorimeter)

Digital to Analog Converters
----------------------------

* DAC Architectures
   * PWM DACs
   * Microcontroller PWM peripherals and their Limitations
   * Analogy to sigma-delta DACs
   * Extension to Class-D modulation

* DAC Circuit techniques
   * Settling time - the Autozero Clamplifier (Don't forget Williams appnotes)
   * Settling time - ADC techniques

* Voltage references
   * Ratiometric circuits
   * Noise reduction techniques - filtering, paralleling
* Interfacing to Data Converters
* Data Converter Support Circuitry
* Data Converter Applications
* Hardware Design Techniques


.. # define a hard line break for HTML
.. |br| raw:: html

   <br />