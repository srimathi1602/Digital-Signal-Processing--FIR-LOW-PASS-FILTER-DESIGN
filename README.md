# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%Low Pass Filter Coefficient
n=0:1:N-1; 
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))
%Bartlett Window Sequence 
n=0:1:N-1; 
wh=1-2*abs(n-alpha)/(N-1) 
hn=hd.*wh 
% Plot the Low Pass Filter with Bartlett Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="698" height="618" alt="Screenshot 2025-11-14 103101" src="https://github.com/user-attachments/assets/d2894e18-2c4c-4302-a7d1-8622da587884" />

## RESULT:

![WhatsApp Image 2025-11-24 at 22 28 45_082de3e6](https://github.com/user-attachments/assets/0b3f828d-bd53-4c24-bd77-eb5aecce5f73)

