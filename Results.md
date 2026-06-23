# Simulation Results

## 1. Open Loop Step Response

The open-loop system response was analyzed to evaluate the natural behavior of the plant without controller action. The response exhibited a slow transient characteristic, indicating the need for a feedback controller to improve system performance.

<img width="726" height="875" alt="OL_Step_Responce" src="https://github.com/user-attachments/assets/f726b2e0-1b93-4a86-b687-aeaa9cf1228a" />


## 2. Closed Loop Response with PID Controller

A PID controller was implemented to improve voltage regulation performance. The closed-loop response demonstrated stable operation with improved tracking capability and reduced steady-state error.

<img width="731" height="875" alt="CL_Responce_with_PID" src="https://github.com/user-attachments/assets/26b9acf6-aa51-4b3a-89a4-0e52fa9ade52" />


## 3. Performance Comparison

A comparative analysis between the open-loop and closed-loop systems was performed. The PID-controlled system exhibited superior performance in terms of response accuracy and stability.

<img width="731" height="875" alt="perfomance Comparison" src="https://github.com/user-attachments/assets/b6313d32-801e-4fa4-b93c-231fbb5197bc" />


## 4. System Response Under Disturbance

A disturbance was introduced into the system to simulate abnormal operating conditions. The controller maintained system stability and demonstrated disturbance rejection capability.

<img width="710" height="845" alt="System Responce Under Disturbance" src="https://github.com/user-attachments/assets/267bfd4a-fae6-44f5-b43d-20dc13aa5a5b" />


## 5. Fault Detection Output Analysis

The fault detection algorithm monitored voltage deviations from the reference value. When the deviation exceeded the predefined threshold, the system successfully identified the fault condition and generated a fault indication.

<img width="710" height="845" alt="Fault_Detection_Output" src="https://github.com/user-attachments/assets/c2a07d61-7e45-4d85-968b-f1b63f78ef3d" />


## 6. Root Locus Analysis

Root locus analysis was performed to study the movement of system poles with varying controller gain. The analysis confirmed the stability characteristics of the closed-loop system.

<img width="700" height="870" alt="Root_Locus" src="https://github.com/user-attachments/assets/06f61c49-a051-494c-8cba-2f4f34726ca6" />


## 7. Gain Margin and Phase Margin Analysis

Frequency-domain stability analysis was carried out using gain and phase margin plots. The obtained margins indicated stable system operation with acceptable robustness.

<img width="690" height="876" alt="GM_and_PM_Analysis" src="https://github.com/user-attachments/assets/c1ecba69-4df1-4bd6-9ff4-17e0205ca63a" />


## 8. Closed Loop System Bode Plot

The Bode plot was used to evaluate the frequency response characteristics of the closed-loop system. The analysis provided insights into bandwidth, stability, and dynamic performance.

<img width="705" height="882" alt="CL_System_Bode_Plot" src="https://github.com/user-attachments/assets/3003e358-dee9-4cd7-bca5-1a6f166b700a" />


## Performance Parameters

Rise Time        : 25.3000 seconds

Settling Time    : 44.8363 seconds

Overshoot        : 0 %

Peak Value       : 0.9983

Fault Status     : FAULT DETECTED

## Conclusion

A PID-based voltage stability and fault detection system was successfully designed and simulated using MATLAB and Simulink. The controller maintained stable operation under disturbance conditions while the fault detection mechanism accurately identified abnormal voltage deviations. The project demonstrates the application of control systems, stability analysis, and monitoring techniques in power and industrial automation systems.
