Hands-On Mixed Signal
=====================

.. toctree::
   :maxdepth: 4
   :caption: Table of Contents Draft:

   table_of_contents/index.rst

A starting point for a(n) (e)book / survey / other on various things practical mixed signal.

Why? Well, I've been in the industry for almost a quarter of a century, touching on not all (which is impossible), but many, analog, digital, and mixed signal topics, applications, products, test methods, etc. And it's thoroughly enjoyable, and somewhat addictive. Here's a blurb I wrote as one of our Active Learning exercises was turned into an Analog Dialogue article:

"Sometime in 1998, I followed a tutorial for hooking up an Analog to Digital converter to a "Basic Stamp" microcontroller. As I turned the little blue dials and watched the numbers on my (MS DOS 6.22) screen go from 0 to 4095, my jaw dropped, and something snapped in my brain - paraphrasing: "Holy F___!!** this is the coolest thing EVER!". Soon after, I quit my job, went back to UMaine for my MSEE degree, and ended up supporting that very ADC as an apps engineer at Linear Technology Corporation. 20 years later, I'm still fascinated by converting signals from analog to digital and vicey-versy.
What are these magical devices that show up everywhere - in you cell phone, your TV, your car... everywhere.?? Build one yourself! Here's a little tutorial from my colleagues and I: `ADALM2000 Activity: Analog-to-Digital Conversion <https://www.analog.com/en/resources/analog-dialogue/studentzone/studentzone-february-2022.html>`__"

This appnote is still out in the wild, I recently re-built it for nostalgia sake. ToDo: Add photo of rebuild. |br|
`BASIC Stamp II Application Notes: Serial ADC with Shiftout and Shiftin <https://www.farnell.com/datasheets/307474.pdf>`__

** "Holy Fun." (That's what I said... really.)

So what can I add to the conversation? Punchline first: The hands-on experience, connecting theory to simple, low-cost experiments that you can actually run on your lab bench, desk, or kitchen table.

Also - "Hybrid Techniques". One of the many fun aspects of my job is that I get to explore lots of strange and creative circuits.

 - Correlated Double sampling and AC excitation (LTC2415 datasheet, AN96)
 - Transparent, cotinuous low-noise gain and offset calibration from noisy calibration readings (AN112)
 - Multitone narrow-band detection (FTC colorimeter)

I'm not an expert in any one particular field - DSP, IC design, matierial science, analog filter design, computer science, RF/microwave, EMI/EMC, power, etc.**, but somehow I've managed to stay employed by "connecting these dots" - making sure all of these disciplines are properly applied to designs so customers can get stuff released. Add to this my "layered" experiencec - it's not just helping tier-1 "strategic and key" customers - it's designing and releaing evaluation boards, conceiving and delivering internal training sessions, onboarding new college graduates, developing university-oriented lab exercises, and if you go far enough back, presenting science topics to all ages, back to kindergarten and ealriler.

Throughout all of these, there has been a common thread of trying to make things as interactive, intuitive, and interesting as possible. I've found that the bar for an effective hands-on activity is extraordinarily low - you just have to have some nonzero physical representation of a concept in your learner's hands to augment what you're saying, what you've given as reading material, and what you're presenting on screen. (We'll very rapidly get to examples below...)

One of the inspirations for this is effort is this dissertation: |br|
`The ASPEN platform : tools for mixed signal electronics, digital signal processing, and biomedical electronics <https://purl.stanford.edu/nq977kw3386>`__ William Esposito, 2018. It's a REALLY nice collection of, well, see the title.

Work / Analog Devices related referenes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`Tools for Low Speed Mixed Signal System Design <https://analogdevicesinc.github.io/documentation/learning/tools_for_ls/index.html>`__ |br|
This one is mostly focused on software control of ADCs and DACs using Linux device drivers. Think of it as a "facilitator" or foundational section. But it does have a tiny bit of LTspice, some basic measurments involving a tiny bit of math, so it's not a bad place to start out. Also a great place for pointing out the distinction between industry standard software vs. bespoke / one-off.

`ADI’s Software Infrastructure for designing with ADCs, DACs, and Sensors <https://trupples.github.io/adi-documentation/learning/sw_infrastructure/index.html>`__ |br|
This is also foundational, but adds in tools for generating and analyzing signals, working with buffers of data .

Note that this is in a fork of analogdevicesinc/documentation, The future home will be `HERE <https://analogdevicesinc.github.io/documentation/learning/sw_infrastructure/index.htmltr>`__.






My own stuff to expand upon
~~~~~~~~~~~~~~~~~~~~~~~~~~~
I've explored various topics to one degree or another before, so why not start with these? 

`Using Python for Analysis and Verification of Mixed-mode Signal Chains <https://proceedings.scipy.org/articles/majora-1b6fd038-001>`__ |br|
Mark Thoren and Cristina Șuteu, Scientific Computing with Python Conference, July 2021. |br|
The one with the most current relevance is this paper from a few years back. It doesn't dive terribly deep, but links analog and digital simulation and measurement, and provides a template for other topics.

`Noise, Filters, and Mixed-Mode Signal Chains - Mark Thoren <https://www.youtube.com/watch?v=KYsf1FuKLIY>`__ (YouTube Video) |br|
Related to the above, a lecture at San Jose State with some nuggets to formalize and distill.

`Delta Sigma ADC Bridge Measurement Techniques <https://www.analog.com/media/en/technical-documentation/application-notes/an96fa.pdf>`__, Linear Technology Application Note, January 2005. |br|
Some ancient, but still relevant history.


Thoren, M. W., & Taufik, T. (2020, June), `Designing Introductory, Hands-on, Open Source Power Electronics Lab Exercises <https://peer.asee.org/34408>`__ Paper presented at 2020 ASEE Virtual Annual Conference Content Access, Virtual On line. |br|
Not mixed signal, but we'll be digging into plenty of power topics so why not?

`ADC Crash Course! <https://github.com/thorenscientific/ROUS/blob/master/educational/ADC_crash_course/ADC_Crash_Course_with_output.ipynb>`__ |br|
A VERY rough start on an "ADC Crash Course", as a Jupyter Notebook. |br|
(This is a verson with saved output plots, may be out of date. Take out the "_with_output" from the URL to get the latest.)


Unsorted References
~~~~~~~~~~~~~~~~~~~

Let's start by scrubbing Analog Devices' technical books. Here's a search: |br|
`resourceTypes=Education~Technical Book <https://www.analog.com/en/search.html?resourceTypes=Education~Technical%20Book>`__


`High Speed Design Seminar, 1990 <https://www.analog.com/en/resources/technical-books/high-speed-design-seminar.html>`__ - A/D, D/A conversion

This is a good chunk of the scope I hope to cover here... circa 2001: |br|
`Mixed-Signal Design Seminar, 1991 <https://www.analog.com/en/resources/technical-books/mixed-signal-design-seminar.html>`__. Edited by Walt Kester, Analog Devices, 1991, ISBN-0-916550-08-7. |br|
(`Zip file of entire book <https://www.analog.com/media/en/training-seminars/design-handbooks/Mixed-Signal-Design-Seminar-1991/Mixed-Signal-Design-Seminar-1991.zip>`__)

From the landing page: |br|
The first Analog Device’s worldwide seminar to treat the fundamentals of data conversion for DSP applications, including Fast Fourier Transforms, Digital Filters, and DSP hardware. The material was updated and expanded in the Mixed Signal and DSP Design Techniques book published in 2000.

(From Figure 1.10 - State of the Art in ADCs - Resolution 22 bits, sampling rate 1 kSPS - HaHa!)

This is dated, of course, but covers Amplifiers, ADCs, mux considerations, distortion mechanisms, analog prototyping techniques. |br|
`Practical Analog Design Techniques, 1995 <https://www.analog.com/en/resources/technical-books/practical-analog-design-techniques.html>`__


This is also probably a bit dated - we will sort through this for perspective: |br|
`The Data Conversion Handbook, 2005 <https://www.analog.com/en/resources/technical-books/data-conversion-handbook.html>`__, Walt Kester, ISBN 0-916550-27-3 (`Zip file of entire book <https://www.analog.com/media/en/training-seminars/design-handbooks/Data-Conversion-Handbook/analog_digital_conversion.zip>`__)


Digital Signal Processing
~~~~~~~~~~~~~~~~~~~~~~~~~

An insanely interesting collection of DSP concepts, illustrated with Python: |br|
`Learning DSP Illustrated <https://dspillustrations.com/pages/index.html>`__


Software-Defined Radio
~~~~~~~~~~~~~~~~~~~~~~

It does not get much better than PySDR.org: |br|
`PySDR: A Guide to SDR and DSP using Python <https://pysdr.org/>`__


Layout
~~~~~~

The best four pages ever written on mixed-signal layout: |br|
`Partitioning and Layout of a Mixed-Signal PCB <https://hott.shielddigitaldesign.com/pdf_files/june2001pcd_mixedsignal.pdf>`__

"OG" References - Fundamental stuff
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`Digital Signal Processing by Alan V. Oppenheim, Ronald W. Schafer <https://www.goodreads.com/book/show/166326.Digital_Signal_Processing>`__

`The Fast Fourier Transform and Its Applications by E. Brigham <https://www.goodreads.com/book/show/126326741-the-fast-fourier-transform-and-its-applications-prentice-hall-signal-pr>`__

`On the use of windows for harmonic analysis with the discrete Fourier transform, F.J. Harris, 1978 <https://ieeexplore.ieee.org/document/1455106>`__
(`PDF from an MIT site <https://web.mit.edu/xiphmont/Public/windows.pdf>`__)


.. # define a hard line break for HTML
.. |br| raw:: html

   <br />