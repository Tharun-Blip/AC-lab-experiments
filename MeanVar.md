# SIMULATION OF MEAN AND VARIANCE USING SCILAB
## AIM:

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed:

•	Computer with i3 Processor
•	SCI LAB

## Algorithm:

1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation

## PROCEDURE:

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results

## Program:

```
clear; clc;

function y = f(x)
    y = 3.6 * x .* (1 - x).^2;
endfunction

function y = g(x)
    y = 3.6 * x.^2 .* (1 - x).^2;
endfunction

a = 0;
b = 1;

EX = intg(a, b, f);
EX2 = intg(a, b, g);
vX2 = EX2 - (EX)^2;

disp("i) Mean of X = " + string(EX));
disp(" ");
disp("ii) Variance of X = " + string(vX2));
disp(" ");

x_seq = input("Type in the reference sequence = ");
y_seq = input("Type in the second sequence = ");

n1 = max(size(y_seq)) - 1;
r = corr(x_seq, y_seq, n1);

disp("Cross Correlation:");
disp(r);

plot2d3('gnn', r);

```
## Output:
<img width="509" height="368" alt="image" src="https://github.com/user-attachments/assets/be78aeb6-31ae-4534-b501-cad9af56befc" />


## Tabulation:
![WhatsApp Image 2025-10-29 at 19 27 57_6d4b8667](https://github.com/user-attachments/assets/1ae55664-3758-42ab-8b26-0cc7f4ee928e)

## Result:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified. 





