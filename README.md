# Design_of_Wide_Range_Tunable_Delay_Line
<p>Variable Delay Lines are circuit elements that introduce a controllable amount of delay to a signal passing through it. This delay can be adjusted based on specific requirements, making it an important element in modern ICs. They have found applications in various domains, such as signal processing and communication systems. A commonly used variable delay element includes a <b>Voltage Controlled Delay Line (VCDL)</b>, where the delay is controlled by an external voltage given to the circuit. This type of delay line is commonly used in delay-locked loops (DLLs), and phase-locked loops (PLLs).</p>

<p><b>Cadence Virtuoso</b> has been used to simulate all the circuits. Cadence Virtuoso is a Linux-based computer-aided tool used to create and analyze IC designs and layouts. The PDK used was the <b>180nm Generic Process Design Kit (GPDK180)</b>, where the minimum channel length of MOSFETs was 180nm.</p>

## Current Starved Inverter architecture
<p>A current-starved inverter consists of a standard CMOS inverter with additional transistors that control the current flowing through the inverter. By adjusting the gate voltage of these additional transistors, the delay through the inverter can be controlled.</p>
<p>This architecture tunes the charging and discharging currents of an inverter to achieve variability in delay. To design this delay unit, an NMOS and a PMOS transistor were used in the discharging and charging paths, respectively, to tune the currents, and a weaker, always-on current source was provided in order to ensure the current doesn’t go to zero.</p>
<figure>
  <img src="./Cascaded_Current_Starved_Inverter_Based_VCDU_Schematic.png" width="90%">
  <figcaption>Schematic of delay unit composed of 2 current starved inverters cascaded together</figcaption>
</figure>
<br><br><br>
<figure>
  <img src="./Testbench_Cascaded_Current_Starved_Inverter_Based_VCDU.png" width="90%">
  <figcaption>Testbench</figcaption>
</figure>
<br><br><br>
<p>The sizes of different transistors were adjusted to control the delay and obtain a reasonable delay range for the delay unit for different process corners.</p>
<p>The sizes of the always-on current source transistors(NM2 and PM2 for 1st inverter and NM5 and PM4 for 2nd inverter) can be tuned to increase the maximum delay obtained(at Vc=0)</p>


