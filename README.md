# Design_of_Wide_Range_Tunable_Delay_Line
<p>Variable Delay Lines are circuit elements that introduce a controllable amount of delay to a signal passing through it. This delay can be adjusted based on specific requirements, making it an important element in modern ICs. They have found applications in various domains, such as signal processing and communication systems. A commonly used variable delay element includes a <b>Voltage Controlled Delay Line (VCDL)</b>, where the delay is controlled by an external voltage given to the circuit. This type of delay line is commonly used in delay-locked loops (DLLs), and phase-locked loops (PLLs).</p>

<p><b>Cadence Virtuoso</b> has been used to simulate all the circuits. Cadence Virtuoso is a Linux-based computer-aided tool used to create and analyze IC designs and layouts. The PDK used was the <b>180nm Generic Process Design Kit (GPDK180)</b>, where the minimum channel length of MOSFETs was 180nm.</p>

## Current Starved Inverter architecture
<p>A current-starved inverter consists of a standard CMOS inverter with additional transistors that control the current flowing through the inverter. By adjusting the gate voltage of these additional transistors, the delay through the inverter can be controlled.</p>
