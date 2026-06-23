%% PID-Based Voltage Stability and Fault Detection System
% Author: Shivam Kumar
% IIT (ISM) Dhanbad

clc;
clear;
close all;

%% System Model

s = tf('s');

% Plant Transfer Function
G = 1/(s^2 + 10*s + 20);

%% Open Loop Response

figure;
step(G);
title('Open Loop Step Response');
grid on;

%% PID Controller Design

Kp = 5;
Ki = 2;
Kd = 1;

C = pid(Kp,Ki,Kd);

%% Closed Loop System

T = feedback(C*G,1);

%% Closed Loop Response

figure;
step(T);
title('Closed Loop Response with PID Controller');
grid on;

%% Performance Analysis

info = stepinfo(T);

disp('Performance Parameters');
disp(info);

%% Compare Open Loop vs Closed Loop

figure;
step(G,'r',T,'b');
legend('Without PID','With PID');
title('Performance Comparison');
grid on;

%% Disturbance/Fault Simulation

t = 0:0.01:10;

% Step disturbance introduced at t = 5 sec
disturbance = zeros(size(t));
disturbance(t >= 5) = 0.5;

[y,t_out] = step(T,t);

fault_response = y + disturbance';

figure;
plot(t_out,fault_response,'LineWidth',1.5);
hold on;
plot(t_out,y,'--','LineWidth',1.5);
xlabel('Time (s)');
ylabel('Voltage');
title('System Response Under Disturbance');
legend('Fault Condition','Normal Response');
grid on;

%% Fault Detection Logic

Vref = 1;

threshold = 0.1;

fault_flag = abs(Vref - fault_response) > threshold;

figure;
plot(t_out,fault_flag,'LineWidth',2);
ylim([-0.1 1.1]);
xlabel('Time (s)');
ylabel('Fault Status');
title('Fault Detection Output');
grid on;

%% Display Fault Information

if any(fault_flag)
    disp('Fault Detected');
else
    disp('System Operating Normally');
end

%% Root Locus Analysis

figure;
rlocus(G);
title('Root Locus Analysis');
grid on;

%% Bode Plot

figure;
bode(T);
grid on;
title('Bode Plot of Closed Loop System');

%% Stability Margins

figure;
margin(T);
grid on;
title('Gain and Phase Margin Analysis');
