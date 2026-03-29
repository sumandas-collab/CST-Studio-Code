# Aim / Objective
To design and simulate a wire dipole antenna using CST Studio Suite with given phys
ical parameters and to analyze its performance in terms of S-parameter (S11), far-field
radiation pattern, and electric field (E-field) distribution at the resonant frequency.
Given Design Parameters. <img width="438" height="192" alt="image" src="https://github.com/user-attachments/assets/f681b3ce-c759-410d-9a48-a2c7e7bd77ce" />


# Theory
A dipole antenna is one of the simplest and most commonly used antennas in wireless
communication. It consists of two conductive arms fed at the center. When the total
length of the dipole is approximately half of the wavelength, the antenna resonates and
radiates efficiently.
The resonant length of a half-wave dipole antenna is given by:
L = λ/2
The wavelength is defined as:
where:
λ = c/f
• c=3×108 m/s is the speed of light
• f is the resonant frequency
At resonance, the radiation resistance of an ideal half-wave dipole antenna is approx
imately:
Rr ≈73 Ω
The reflection coefficient S11 indicates impedance matching between the antenna and
feed line. For proper matching:
S11 < −10 dB
# Resonant Frequency Calculation (For 3.5 GHz)
Given resonant frequency:

f =3.5 GHz =3.5×109 Hz

Step 1: Wavelength Calculation:

λ = 3×108/3.5 ×109 
= 0.0857 m = 85.7 mm

Step 2: Dipole Length Calculation:

L = λ/2 = 85.7/2 =42.85 mm

Comparison Between Calculated and Simulated Re
sults

Calculated dipole length: 42.85 mm

Simulated dipole length: 34.5 mm

Percentage Error

Error = {|42.85 −34.5|/42.85}×100

Error ≈ 19.5%

# Reason for Error:
The difference between theoretical and simulated values is due to practical antenna effects
such as:
• End effects of the dipole
• Finite wire radius
• Feed gap capacitance
• Material properties and boundary conditions
These effects reduce the effective electrical length, causing resonance at a shorter
physical length.
# Design Procedure in CST Studio Suite
1. Create a new antenna project in CST Studio Suite.
2. Select the Time Domain Solver.
3. Model a wire dipole with a total length of 34.5 mm and radius of 1 mm.
4. Introduce a feed gap of 4 mm at the center.
5. Assign Copper (Annealed) as the material.
6. Apply discrete port excitation at the feed point.
7. Set open (radiation) boundary conditions.
8. Define the frequency range around 3.5 GHz.
9. Run the simulation.
# Design Figure
<img width="1272" height="416" alt="1 3DImage" src="https://github.com/user-attachments/assets/f6911405-0724-4d06-b712-d944446ed519" />
Figure 1: 3D geometry of the wire dipole antenna in CST Studio Suite.
# Results and Discussion
# S-Parameter (S11)
The S11 plot shows a clear resonance at approximately 3.5 GHz. The minimum S11 value
is around 15 dB, indicating good impedance matching and efficient antenna operation.
<img width="1272" height="416" alt="1  S11" src="https://github.com/user-attachments/assets/15f91a10-28e0-4c73-97c9-e982fd8c3935" />
Figure 2: S-parameter (S11) plot of the dipole antenna.
# Far-Field Radiation Pattern
The far-field radiation pattern exhibits a donut-shaped distribution with maximum radi
ation perpendicular to the antenna axis. The simulated directivity is approximately 2.11
dBi, which matches theoretical expectations for a half-wave dipole antenna.
<img width="1272" height="416" alt="1  Farfield" src="https://github.com/user-attachments/assets/6a3babc1-6d7f-4d8c-94a2-9d359c775fb7" />
Figure 3: 3D far-field radiation pattern at 3.5 GHz.
# Electric Field (E-Field) Distribution
The E-field distribution shows maximum field intensity near the feed point, gradually
decreasing toward the ends of the dipole. This confirms proper excitation and resonant
behavior of the antenna.
<img width="1273" height="417" alt="1 EField" src="https://github.com/user-attachments/assets/cb431117-2959-4344-a450-230a0345a652" />
Figure 4: Electric field (E-field) distribution at 3.5 GHz.
# Conclusion
A wire dipole antenna was successfully designed and simulated using CST Studio Suite.
The antenna resonates at approximately 3.5 GHz with good impedance matching and
a typical dipole radiation pattern. Although the simulated length is shorter than the
theoretical value, the deviation is due to practical antenna effects and is within acceptable
limits. The results closely match theoretical expectations.
