# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
clc; % clear screen<br>
clear all; % clear screen<br>
close all; % close all figure windows<br>
wc=input('enter the value of Wc1='); <br>
N=input('enter the value of N=');<br>
alpha=(N-1)/2; <br>
eps=0.001;<br>
%High Pass Filter Coefficient<br>
n=0:1:N-1;<br>
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps))<br>
%Blackman Window Sequence <br>
n=0:1:N-1; <br>
wh=0.42-0.5*cos((2*pi*n)/(N-1))+0.08*cos((4*pi*n)/(N-1))<br>
hn=hd.*wh <br>
% Plot the  High Pass Filter with Blackman Window Technique<br>
w=0:0.01:pi; <br>
h=freqz(hn,1,w);<br>
plot(w/pi,abs(h),'blue');<br>


## OUTPUT:
![WhatsApp Image 2025-11-23 at 15 58 52_e95cc38f](https://github.com/user-attachments/assets/7dc15c58-1932-43fa-b3c1-1fd30ed75ae4)


## RESULT:
![WhatsApp Image 2025-11-28 at 22 27 49_5401c188](https://github.com/user-attachments/assets/cf7333ec-6a28-42a9-b7ff-877d994664bd)
