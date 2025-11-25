# Radar Range Equation 
## Aim
To implement and analyze the Radar Range Equation using Scilab, and to plot the received power with respect to range.

## Apparatus Required
Software: Scilab Hardware: Personal Computer

## Theory
The Radar Range Equation relates the power received by a radar from a target at distance 𝑅:

<img width="333" height="293" alt="image" src="https://github.com/user-attachments/assets/85a4c97f-d9c5-450a-9be9-9b2a00dd2ef0" />
<img width="182" height="83" alt="image" src="https://github.com/user-attachments/assets/6697a26d-7526-41f3-9aa7-dbbe67e67bac" />

## Program 
```
clf;

Pt = 7000;
G = 40;
eta = 0.5;
Ae = 1;
Smin = 1e-10;

Pt_values = 6000:100:8000;
R1 = zeros(1, length(Pt_values));

for i = 1:length(Pt_values)
    R1(i) = ((Pt_values(i)*G*eta*Ae) / (16*%pi^2*Smin))^(1/4);
end

subplot(3,1,1);
plot(Pt_values, R1, 'b');
xlabel("P_{t}");
ylabel("R_{max}");

Pt = 5000;
G_values = 40:1:70;
R2 = zeros(1, length(G_values));

for i = 1:length(G_values)
    R2(i) = ((Pt*G_values(i)*eta*Ae) / (16*%pi^2*Smin))^(1/4);
end

subplot(3,1,2);
plot(G_values, R2, 'r');
xlabel("G");
ylabel("R_{max}");

Pt = 5000;
G = 40;
Smin_values = linspace(0.5e-10, 1.5e-10, 50);
R3 = zeros(1, length(Smin_values));

for i = 1:length(Smin_values)
    R3(i) = ((Pt*G*eta*Ae) / (16*%pi^2*Smin_values(i)))^(1/4);
end

subplot(3,1,3);
plot(Smin_values, R3, 'g');
xlabel("S_{min}");
ylabel("R_{max}");

```
# Output Waveform
<img width="1784" height="973" alt="image" src="https://github.com/user-attachments/assets/342bb0e6-8906-4234-8ef4-a978d838dbe1" />

# Tabulation

![WhatsApp Image 2025-11-25 at 21 07 56_d7436a24](https://github.com/user-attachments/assets/d53513f4-1895-472f-b909-3c881a3f38e2)

# Result
Thus, the Radar Range Equation was successfully implemented in Scilab.

