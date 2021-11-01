# **USER MANUAL BCCT**

## Safety precautions
Since you only work with water, there aren't any safety issues! Have fun!

## **1. Introduction**

This is the documentation  file of the Battery Construction and Cell Testing (BCCT) team of the 
FLowerPower group. In this file all the information required to conduct the experiment will be 
included. Our group focused on building a rechargeable  all-iron flow battery, and also conduct 
experiments  on the battery cell.  The purpose of this documentation  is for other people to be 
able to reproduce our results.  The goal of our measurement is to get a better understanding of the 
influence of the battery cell design of the fluid flow through the cell. The amount of fluid that 
can flow through holds a strong relation with the performance of the cell. More fluid that passes 
through the cell results in potentially more electrons interacting with the electrode.  This 
documentation goes together with the Mathematica program provided which is named 
PressiireMeosnrementPepro.nb and can be found in the Gitlab repository.  The program is well 
commented  and the information  on how to do the measurement together with this program is provided 
below.

## **2. Cell Testing**

The quantitative research on the battery cell will consist of a measure of the pressure drop due to 
the battery cell. The battery cell performance has a lot of dependencies, i.e. fluid flow rate, 
cell pressure electrode geometry to name a few. The focus of our group was on the measurement  of a 
pressure drop depending on the battery cell volume.  By increasing the volume between the 
electrode/anode and the membrane, more fluid is able to pass through the cell.  The pressure drop 
corresponding  to this change is what we are interested in. However we where not able to build the 
battery cell correctly, with not too much fluid leaking out of the system, creating a pressure 
loss. Thus this measurement  is left out. However there are other experiments to be done before 
being able to do measurements on the battery cell. The measurement  device needs to be calibrated, 
and there will be a reference measurement  done over the battery system without the battery cell in 
between the pipes. The pressure drop over a pipe of length L is thus measured.

### **2.1 Theory**

The measurement  of the pressure drop over the battery cell will not consist of a theoretical value 
of the pressure drop. This is due to the complexity of the problem. The flow of a fluid through a 
box of dimensions (x,y,z) is hard to calculate, and should be conducted by doing a numerical 
calculation of the navier-stokes  equation as was done by J. Houser et al. for different 
architectures of a battery cell.
The pressure drop over a regular pipe is better understood theoretically  and is given below:

$`ΔP=λ*L*ρ/(D*2*ω^2)`$ (2.1)

Where ΔP is the pressure drop over a pipe of length L, width D and flow coefficient λ.  The 
fluid has density ρ and flow velocity ω.  For practical reasons  we also are interested in how 
the pressure drop relates to the incoming and outgoing pressure over an object:

$`ΔP=(P_1^2-P_2^2)/(2*P_1)`$ (2.2)


Since the measurement  device used does not give values of pressure in pascals but in volts, we are 
also interested in a calibration  measurement  for the pressure relation to volts.  For this we 
conduct  a calibration measurement  as described in section 2.3.  There we will measure the pressure due to a Column of 
fluid of height h above a point. The theoretical relation for hydro-static pressure is given by:

$` P=ρ*g*h `$ (2.3)

where ρ is the density of the fluid, p the gravitational potential taken to be aprox. 9.81 and h 
the height of the collumn in meters.

### **2.2    Materials required**
This section consist of a list required to do the experiment with pictures. 
Pressure measurement device (M) illustrated in figure: [2.1](Images/pressure_measurement_device.jpeg) and [2.2](Images/device_part.jpeg)
* 3 pipes with outside diameter 4.7mm: 
1. 161cm
2. 135cm
3. 85 cm
* 400 mL of demiwater
* Cylindrical container 1000mL, 18cm height (C) 
* Oscilloscope (O) illustrated in figure: [2.4](Images/Oscillator.jpeg) 
* Peristaltic pump(P)  illustrated in figure: [2.5](Images/pump.jpeg) 
* Voltage meter (V)
* T-Junctions 
* Valves

![look in file](Images/pressure_measurement_device.jpeg)
Figure  2.1:  Amplifier  of  the pressure  measurement  device.   The  "nulinstelling" knob and 
"uitgang" output are of interest.  "nulin- stelling" knob should be calibrated to 0 volts at  
atmospheric  pressure,  and  the  output should be connected to a voltage meter.
<br>
<br>
<br>
<br>
![look in file](Images/device_part.jpeg)
Figure 2.2: Measurement device. The small transparent  wire  is connected  to  the  mea- sured  
system,  and the Green  valve  is  op- erated to equalize the pressure across the device.
<br>
<br>
<br>
<br>
![look in file](Images/Waves.jpeg)
Figure 2.3:  Using the "Scale" button in the vertical axis, you have to make sure that all the 
periods of  your wave are shown in the screen.  Otherwise  the measurement  won't be correct. The 
mean, max and min values appear on screen.
<br>
<br>
<br>
<br>
![look in file](Images/oscilloscope.jpeg)
Figure 2.4:  You connect the pressure measurement devise in channel 1. Using the position 
buttons you make sure that the wave you see is centered.  In order to take measurements you press 
"Measure".
<br>
<br>
<br>
<br>
![look in file](Images/pump.jpeg)
Figure 2.5:  Peristaltic  pump used.  Put the tube in the corresponding clamp and close it with 
the lever, change the fluid flow rate with the arrows.
<br>
<br>
<br>
<br>
![look in file](Images/container.jpeg)
Figure 2.6: Fluid container, the tubes can be attached to the designated openings, or the tubes can 
be laid over the top of the wall of the container as we did.
<br>
<br>

### **2.3    Calibrating the Pressure measurement**

The pressure measurement  device in use registers the pressure of the fluid in a pipe. The output of the Pressure measurement is in (V) volts. To relate the amount of volts to a pressure in Pascal (Pa), we need to calibrate the device with a known amount of pressure.  By measuring several pressures which are of a known value, we know what amount of volt relates to the pressure by assuming a linear scale.  For this we use a vertical column of water which we vary in height h with discrete linear steps of fixed size. With these data-points we can relate the voltage to the pressure.  By taking multiple measures at the same parameters we increase the accuracy of the measurements. We can relate the uncertainty of the experiment by the standard deviation.

#### **How to calibrate the measurement  device.**
1. Connect the voltage meter to the pressure measurement device amplifier as displayed in picture 2.1.
2. Connect the a tube of sufficient length to the measurement device with the attached transparent wire.
3. Place the measurement device on the group, and the amplifier on a table.
4. Turn on the devices 
5. Calibrate the "nulinstelling knob" to 0 volts.
6. Do the measurements  for discrete steps of water height above the measurement device, by filling the tube and fixing the tube to a tripod with clamp.
7. Read out 5 measurements  of the voltage for each height and put the values in the Mathematica program.

The schematics of the measurement:
<br>
![look in file](Images/callibrationsetup.jpeg)
Figure 2.7: Calibration setup schematics.

#### **Using the mathematica file:**
A Mathematica file is added in which you only need to add the measured values of the height column, measured voltage at each height, flow rates of the pump and the measured mean voltages for the actual experiment.  Only replace values if stated so, the other parts produces plots for your experiment.  Also a function is provided, so you can switch from voltage to pressure manually.

### **2.4    Reference measurement**
The pressure drop over a battery cell can be simplified to the pressure drop over a pipe. By changing the flow velocity ω of the fluid we expect a pressure drop related to the theoretical values of relation 2.1. For practical considerations the pressure drop is measured by means of 
incoming and outgoing pressure with relation (2.2). The fluid velocity will now be varied from 2 to 6 4 $`(ml/min)`$ with steps of 1, and the resulting pressure drop will be measured. For this measurement we keep the entire setup at level such that the uncertainty due to gravitational pressure is minimized.  The total setup is displayed below in figure 2.8 and 2.9
![look in file](Images/set_up.jpeg) ![look in file]( Images/setupsketch.jpeg)
<br>
The setup is as symmetrical as practically possible such that the effect of measuring on either side is minimized.

#### **How to conduct the measurements step by step:**
1. You fill the container with 400mL demiwater (enough to fill the circuit and allow the pipes to 
have a constant flow)
2. You put one end of pipe 1 in the container and attach it to the pump. Make sure the clump lever 
of the pump is in the right direction.
3. You connect pipe 1 with 2 and pipe 2 with 3, with T-junctions  (at points M1 and M2), with 
attached valves.
3. You connect the pressure measuring device and the Oscilloscope (O), you set the Oscilloscope as 
explained in figure [2.4](Images/Oscilloscope.jpeg)
4. Attach the (M)-(O) system at the T-junction of M1.
5. Changing the flow-rate of the pump you take different measurements of the mean, max and min mV from the (O), you can see how to set up the wave in order to take the measurements in [2.3]
6. You attach the (M)-(O) system at the M2 T-Junction and repeat step 5.

### **2.5    Measurement Results**

![look in file](Images/PressureVoltageRel.PNG)
<br>
Figure 2.10: In this figure we see the measured voltages for different heights (red) and the best 
fit through this data (blue), such that we now know the relation between volts and pressure.
<br>
<br>
<br>
<br>
![look in file](Images/ResultFlowPressure.PNG)
<br>
Figure 2.11: In this figure we see the mean pressure for different flow rates.
<br>
<br>
<br>
### **2.6    Conclusion**
We where able to calibrate our measurement device and found a linear relation between voltage and 
pressure:

$`P_α+ρ*g(V-b)/α`$  (2.5)

where α and b are parameters set by the fitted model. For our fit, α=0.481336 and b=-0.14711.  This relation was then used to measure the pressure drop for the reference  measurement. 
The reference measurement was used to compare the pressure drop due to the battery cell with that of only the pipes used. We measured the pressure drop for different flow velocities over a pipe of length L.  The experiment was done to get a better understanding of the fluid dynamics in a battery 
cell which has a significant influence on the performance of the battery.
