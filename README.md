# InVehicleSecurityECUClassification

Introduction:

CAN protocol has been widely used as network protocol for in-vehicle communication. CAN protocol has been deemed as reliable ever since it has been first introduced and still being used in the modern vehicle. However, as the modernization of the vehicle took another turn and the communication of the vehicle does not limit to itself but also requires to communicate to external world, then vulnerability of the protocol was detected and required different solution. There were different techniques thought of to tackle the issue and one of the approach is machine learning. This project explores three different machine learning technique, first Gaussian Naive Bayes, second is Random forest and finally Artificial Neural Network to classify/detect the ECU from which the CAN message is transmitted. In addition, those three machine learning techniques are applied to intrusion simulated system to explore further ECU classification.

ECU classification starts with CAN messages taken as dataset. Fig. 1 shows CAN message signal from of one of the ECU from the dataset when its plotted in the graph. The red signal is the actual signal and the green signal is the expected signal in the voltage form. The actual signal in the figure shows that there is some fluctuation seen in each square wave compared to the green expected signal. The fluctuation in the CAN message collected from each ECU can be taken as feature set in machine learning algorithms to classify the ECUs. For the experiment, the dataset consists of CAN message signal from 8 different ECUs.

![image](https://user-images.githubusercontent.com/102163137/162272495-166f202a-3ad1-426e-bbb2-3df4ff699109.png)

Features Extracted: 

Features are selected by isolating each square wave from Fig. 1. There are total of nine features used to train the machine learning algorithm.
  1. Peak Time
  2. Percent Overshoot
  3. Settling Time
  4. Steady State Value
  5. Peak Voltage
  6. Lowest Voltage
  7. Settling Time Max
  8. Peak Frequency using Fourier Transform
  9. Least Frequency using Fourier Transform
 
Intrusion Simulation:
 
The intrusion on the vehicle signal is simulated by adding Gaussian noise to one of the eight ECUs used to build the model. For the experiment, ECU 1 was chosen (in random) and the Gaussian noise with zero mean and 0.05 standard deviation was added to the signal of ECU 1. The signal with Gaussian Noise on ECU 1 is named as ECU 9 in the experiment. Following figure is the noise added version of Fig 1.
![image](https://user-images.githubusercontent.com/102163137/162273961-e9cc3e01-b23f-45ba-b65c-7f6dd48e44d7.png)


