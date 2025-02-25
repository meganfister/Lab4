# Lab 4 - Operational Amplifiers

Aashika Uppala, Megan Fister

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


## Methods/Results
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

We connected two different DC Power Supplies set to 15 V and drove the voltage divider with the positive and negative voltage supplies. We collected data for $V_o$ vs. $V_i$ by adjusting the potentiometer to change the input voltage, and recorded 9 $V_i$ values that range from negative to positive saturation points. The data we recorded can be seen below in Table 1.

_Table 1_
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

Measuring the true resistance of the 68 kΩ resistors gave us values of $R_f$ = 67.6 kΩ and $R_i$ = 67.9 kΩ.

Gain is found by using the equation - $R_f$ / $R_i$ 

Expected gain = -67.6 kΩ / 67.9 kΩ = -0.994

The graph below displays the lab data as scattered points around the expected gain line. Ideally, the gain would be -1 if the resistors were perfectly equal, but due to tolerance errors, we calculated a slightly different value of -0.9941. However, this is very close to -1, and the data points closely follow the expected trendline, indicating minimal deviation.

_Graph 1_

![Inverting Op Amp Gain](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Graph.png)


Next, we constructued the moderate gain inverting op amp circuit that is pictured below.

![Moderate Gain Op Amp](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Moderate%20Gain%20Op%20Amp.png)

Connecting this circuit to a function generator, we set the voltage to 100mV and the frequency to 2 kHz. 

![Moderate Gain Full Setup](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Moderate%20Full%20Setup.jpg)

We also connected both $V_i$ and $V_o$ to the Oscilloscope. $V_i$ is in channel 1, $V_o$ is in channel 2.

![Moderate Gain Connection to Oscilloscope](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Moderate%20Gain%20Connected%20to%20Oscope%20Gray%20Clips.jpg)

We use the oscilloscope to measure and calculate the gain of the circuit.

Measuring with the amplitude in Channel 1, we find $V_i$ = 35.2 mV. 

![Moderate Gain Channel 1](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Moderate%20Channel%201.jpg)

Measuring with the amplitude in Channel 2, we find $V_o$ = 2.56 V.

![Moderate Gain Channel 2](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Moderate%20Channe2%201.jpg)

Gain = - $V_o$ / $V_i$ = 2.56 V / .0352 V = -72.73


Next, we constructed the high gain inverting op amp circuit that is pictured below.

![High Gain Op Amp](https://github.com/meganfister/Lab4/blob/main/Lab%204%20High%20Gain%20Op%20Amp.png)

Connecting this circuit to a function generator, we set the voltage to 10 mV and the frequency to 2 kHz.

We also connected both $V_i$ and $V_o$ to the Oscilloscope. $V_i$ is in channel 1, $V_o$ is in channel 2. We use the oscilloscope to measure and calculate the gain of the circuit.

Measuring with the amplitude in Channel 1, we find $V_i$ = 10.6 mV. 

Measuring with the amplitude in Channel 2, we find $V_o$ = 7 V.

Gain = - $V_o$ / $V_i$ = 7 V / .0106 V = -660.38

These results make sense because the gain of our high gain inverting op amp circuit is almost 10 times greater than that of our moderate gain inverting op amp circuit.

#### Part 2 - Op Amps and Frequency Response
We constructed a voltage follower op amp circuit that is pictured below. 

![Voltage Follower Op Amp](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Voltage%20Follower%20Op%20Amp.png)

We set the function generator to 1V amplitude and 2 kHz frequency and made sure that $V_i$ = $V_o$ which means that the gain for the voltage follower is equal to 1.

We measured the frequency limit for the 741 op amp to be 14,000 Ω.

Next, we constructed an integrating op amp circuit as shown in the picture below.

![Integrating Op Amp](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Integration%20Op%20Amp.png)

We connected the function generator to observe the input and output waveforms for 4 kHz, 1 V peak to peak, sine, square, and triangle waves. Pictures of our results are shown below.

Note: The function to create square waves on our function generator was broken which is why the square waves display as flat lines.

![Integrating Op Amp Sine Waves](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Integration%20Sin.jpg)

![Integrating Op Amp Triangle Waves](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Integration%20Triangle.jpg)

![Integrating Op Amp Square Waves](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Integration%20Square.jpg)

Increasing the voltage increases the input and output voltage, while increasing the frequency leads to a decrease in output amplitude.


Finally, we constructed a differentiating op amp circuit as shown in the picture below. 

![Differentiating Op Amp](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Differentiating%20Op%20Amp.png)


We connected the function generator to observe the input and output waveforms for 4 kHz, 1 V peak to peak, sine, square, and triangle waves. Pictures of our results are shown below.

Note: The function to create square waves on our function generator was broken which is why the square waves display as flat lines.

![Differentiating Op Amp Sine Waves](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Differentiating%20Sin.jpg)

![Differentiating Op Amp Triangle Waves](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Differentiating%20Triangle.jpg)

![Differentiating Op Amp Square Waves](https://github.com/meganfister/Lab4/blob/main/Lab%204%20Differentiating%20Square.jpg)

Increasing the voltage increases the input and output voltage, while increasing the frequency leads to a decrease in output amplitude.


## Discussion
### Part 1 - Limits of Op Amps
_Compare the performance of each amplifier circuit to its expected theoretical performance with regard to gain._

The moderate gain inverting amplifier (with a higher resistor ratio) exhibited a larger gain, and oscilloscope measurements confirmed it. 
The high gain inverting amplifier showed deviations at extreme voltages due to saturation effects but still exhibited a larger gain than the moderate gain amplifier. 
For the unity gain inverting amplifier, the expected gain is -1, and measured values were closely aligned with this expectation.
There are deviations due to tolerances in resistor values, non-ideal characteristics of the LM741 (e.g., offset voltage and input bias currents), and limitations in measurement accuracy.

_Comment on the limits of op-amp circuits with respect to maximum output voltage._

The LM741 cannot output voltages equal to the supply rails due to output voltage swing limitations. Typically, the output voltage is limited to within 1-2V of the supply voltage. At high gain settings, the output may saturate quickly when the input voltage exceeds a certain threshold, leading to distortion.
 
_Are the LM741 op amps symmetric i.e. does the positive voltage performance equal the negative voltage performance?_

Yes, the LM741 op-amp is designed for symmetric performance, and our measurements showed that its positive and negative voltage responses were nearly identical. However, slight asymmetry can occur due to variations in internal transistor behavior.

### Part 2 - Op Amps and Frequency Response
_Did the integrating and differentiating circuits perform the mathematical operations expected? Explain._

Yes, because the integrator performed by for a sine wave input, the output was a cosine wave (phase-shifted by 90°). For a triangle wave input, the output was a parabolic wave. Deviations can occur due to DC drift and practical limits of the op-amp. 
The differentiator performed for a sine wave input, the output was a cosine wave (also phase-shifted by 90°).
For a triangle wave input, the output was a square wave. At high frequencies, the differentiator may become unstable due to noise amplification.
The square function on our function generator was broken, therefore all of our square data displays as straight lines which is incorrect. 
## Conclusion
This lab provided hands-on experience with various Op-Amp circuits and demonstrated their theoretical and practical behaviors. The experimental gain values generally aligned with theoretical calculations, though minor deviations occurred due to component tolerances and Op-Amp limitations. The voltage follower exhibited unity gain as expected, but the LM741’s bandwidth constraints became evident at higher frequencies.
The inverting amplifier circuits demonstrated predictable gain characteristics, but output voltage limitations prevented full utilization of the supply range.
The integrator and differentiator circuits effectively performed mathematical operations on input signals, though performance degraded at high frequencies due to noise amplification and slew rate limitations.
Overall, this lab highlighted the capabilities and practical constraints of Op-Amps, reinforcing key concepts in analog circuit design. Understanding these limitations is crucial for designing stable and efficient amplifier circuits in real-world applications.
