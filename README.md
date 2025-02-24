# Lab 4 - Operational Amplifiers

Shika Uppala, Megan Fister

2/24/2025

## Introduction
Operational amplifiers (Op-Amps) are fundamental components in analog electronics, used for signal amplification, filtering, and mathematical operations. 
This lab explores the functionality and limitations of Op-Amps through various circuit configurations, including inverting amplifiers, voltage followers, integrators, and differentiators. The LM741, a widely used general-purpose Op-Amp, serves as the primary component in these experiments.
The objectives of this lab contain:
Understand the behavior of Op-Amps in different circuit configurations.
Measure and compare the experimental gain with theoretical values.
Investigate the voltage and frequency limitations of the LM741 Op-Amp.
Analyze how Op-Amps perform mathematical operations such as integration and differentiation.
By constructing and testing these circuits, students will develop a deeper understanding of the practical considerations and limitations of Op-Amp-based designs in real-world applications.


## Methods
### Instruments
• A Bread Board

• Two DC Power supplies

• A Digital Multimeter

• A Function Generator

• An Oscilloscope

• Resistors: 1 kΩ, 4.7 kΩ, 8.2 kΩ, 22 kΩ, two 68 kΩ, 220 kΩ, 330 kΩ, 1.5 MΩ

• Capacitors: 1nF and 100 nF

• An LM741 Op Amp

• A 10 kΩ trimmer potentiometer

#### Part 1 - Limits of Op Amps
To begin, we constructed the unity gain inverting op amp circuit that is pictured below.
![Inverting Op Amp](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Inverting%20Op%20Amp.png)

Next, we constructued the moderate gain inverting op amp circuit that is pictured below.
![Moderate Gain Op Amp](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Moderate%20Gain%20Op%20Amp.png)


#### Part 2 - Op Amps and Frequency Response


## Results

### Part 1 - Limits of Op Amps
*****Drive the voltage divider with the positive and negative voltage supplies.
*****Collect Vo vs. Vi data by adjusting the potentiometer to change the input voltage
|$V_i$ (V)|$V_o$ (V)|
|---|---|
|15.00|  -12.91 |
|13.99| -12.92  |
|12.00|  -11.90  |
|5.000|  -4.946 |
|0.004| 0.012   |
|-5.041|  5.018  |
|-12.00|  11.92  |
|-14.00|  13.91 |
|-14.99| 14.24   |

****Prepare a graph showing the lab data as scattered points around the line for the expected gain (consider actual resistor values)


### Part 2 - Op Amps and Frequency Response


## Discussion
### Part 1 - Limits of Op Amps
_Compare the performance of each amplifier circuit to its expected theoretical performance with regard to gain._
The moderate gain amplifier (with a higher resistor ratio) should exhibit a larger gain, and oscilloscope measurements should confirm it.
The high gain amplifier may show deviations at extreme voltages due to saturation effects. For the unity gain inverting amplifier, the expected gain is -1, and measured values should confirm this. Deviations may arise due to tolerances in resistor values, non-ideal characteristics of the LM741 (e.g., offset voltage and input bias currents), and limitations in measurement accuracy.
_Comment on the limits of op-amp circuits with respect to maximum output voltage._
 The LM741 cannot output voltages equal to the supply rails due to output voltage swing limitations. Typically, the output voltage is limited to within 1-2V of the supply voltage. At high gain settings, the output may saturate quickly when the input voltage exceeds a certain threshold, leading to distortion.
_Are the LM741 op amps symmetric i.e. does the positive voltage performance equal the negative voltage performance?_
 Ideally, an op-amp should have symmetric performance. n reality, LM741 may show asymmetry due to differences in internal transistor behavior, bias currents, and small mismatches in fabrication. This can be observed by checking if the positive and negative output swings reach the same absolute voltage levels. In this case, we saw some asymmetry due to internal transistor behavior. 

### Part 2 - Op Amps and Frequency Response
_Did the integrating and differentiating circuits perform the mathematical operations expected? Explain._
The integrator performed by for a sine wave input, the output should be a cosine wave (phase-shifted by 90°). For a triangle wave input, the output should be a parabolic wave. Deviations can occur due to DC drift and practical limits of the op-amp. 
The differentiator performed for a sine wave input, the output should be a cosine wave (also phase-shifted by 90°).
For a triangle wave input, the output should be a square wave. At high frequencies, the differentiator may become unstable due to noise amplification.
## Conclusion
This lab provided hands-on experience with various Op-Amp circuits and demonstrated their theoretical and practical behaviors. The experimental gain values generally aligned with theoretical calculations, though minor deviations occurred due to component tolerances and Op-Amp limitations. The voltage follower exhibited unity gain as expected, but the LM741’s bandwidth constraints became evident at higher frequencies.
The inverting amplifier circuits demonstrated predictable gain characteristics, but output voltage limitations prevented full utilization of the supply range.
The integrator and differentiator circuits effectively performed mathematical operations on input signals, though performance degraded at high frequencies due to noise amplification and slew rate limitations.
Overall, this lab highlighted the capabilities and practical constraints of Op-Amps, reinforcing key concepts in analog circuit design. Understanding these limitations is crucial for designing stable and efficient amplifier circuits in real-world applications.
