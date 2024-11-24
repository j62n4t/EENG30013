java c
FACULTY OF ENGINEERING 
Coursework Component (worth 100% of total weight for unit) for the assessment of 
EENG30013 POWER ELECTRONICS, 
MACHINES AND DRIVE TECHNOLOGIES 
Autumn 2024 
DEADLINE: 
13:00 UK Time on Thursday 28th November 2024 (Week 11) 
Design and loss and performance assessment of an 
3-phase AC permanent magnet synchronous machine-based drive 
for use in a high-speed express elevator in “The Shard” 
Assessment requirement The aim of this assessment is for you to demonstrate your ability to use your understanding of taught content and the simulation techniques and principles taught in the various elements of this unit to design and assess an electric drive system.As such you should be aware that there is no “right” answer to the problems here and that you are being assessed  in  how  you  approach  and  synthesise  the  design  and  how  you  analyse  and  demonstrate  the suitability of your design solution to the problem you have been set.  The suggested approaches included in this script. are just guides to help you through this exercise, however you don’t have to follow them as long as your own approach achieves the requirements for each part of the study.
General Design Problem 
We will use an express elevator for “The Shard” in London as the fictional case study.  The full drivetrain that you will be exploring is shown inFigure 1. 
You are investigating the design of an electric drive that uses a conventional 3-phase, 2-level inverter with an 3-phase AC permanent magnet synchronous machine as a motor.The motor outputs a lifting torque for an express elevator through a mechanical gearbox connected to the permanent magnet synchronous motor through a mechanical shaft.  The output of the gearbox is connected to a drum around which as series of lifting wires are wound that connect to the lift.
The lift has a counterweight whose mass is 100% of the mass of the lift carriage (600kg) and 40% of the design load (10 people of 80kg).

Figure 1: Elevator Drivetrain For rigorous testing you are required to assess the capability of your electric drive when it lifts the express elevator through 95 floors (300m) in around 90 seconds with its maximum load. During this time, the elevator
needs to accelerate at a fixed rate over 3.5 seconds to a steady-state speed,̇(x)1(steady)  = 3.5 m/s,   and then
decelerate  to  zero  speed  over  3.5  seconds  at  a  fixed  rate.    This  is  equivalent  to  an  acceleration  and
deceleration of̈(x)1  = ±1m/s2
The elevator vertical speed vs time profile equivalent to this requirement is shown inFigure 2. 
The power supply available to the inverter is a rectified 3-phase 230VRMS AC domestic supply equivalent to approximately 325VDC.  You are not required to simulate or consider the rectification stage.
Details 
Lift requirements 
The lift must be able to travel a distance of 300m in 90s.
For the purposes of this exercise, you are asked that the speed vs time profile have the form. shown below:
•    accelerate the lift linearly to the steady-state velocity,̇(x)1   = 3.5m/s, from t  = 0s to t  = 3.5s,
• maintain the lift speed at steady-state velocity, ̇(x)1(steady)  = 3.5m/s from t  = 3.5s to t  = 86.5s,• decelerate the lift linearly from the steady-state velocity,̇(x)1(steady)  = 3.5m/sfrom t  = 86.5s to t  = 90s.
This results in a linear velocity Vs time profile x1 (t) for the lift that has the form. shown inFigure 2. 
Lift Velocity (x1) Vs Time Profile for Required Operation (Positive Velocity = Lift Moving Up)

Figure 2: Required linear velocity Vs Time profile You will need to ensure and demonstrate that this speed time profile results in a required peak AC voltage that doesn’t exceed the electrical supply limits.  Recall that the rectified DC input to the inverter is VDC  = 325V.  The current limit will be determined by your final power semiconductor selection.
Design Challenge Overview 
Your challenge is to undertaken design and analysis of the electric drive at three levels:MACHINE – Convert speed Vs time requirements into a torque Vs time and assess efficiency of a single operation cycle based upon the load described. Calculate voltage and current at two specific operating points given.DRIVE (CONVERTER) – Use a 3-phase, 2-level converter to generate the required voltage waveforms and assess the impact of the PWM generated waveforms on harmonic content, resulting machine loss and DC link ripple. 代 写EENG30013 POWER ELECTRONICS, MACHINES AND DRIVE TECHNOLOGIES Autumn 2024C/C++
代做程序编程语言Do this at the operating points from the machine tasks. POWER ELECTRONICS (SWITCHES) – Select an appropriate switch and diode pair to model in detail for the converter and assess  device  losses  over  a  single  electrical  cycle.   Select  a  heatsink  and  assess  thermal performance.
Coursework Instructions 
MACHINE 
(A)  Use the speed Vs time profile (Figure 2) and details of the mechanical load (Figure 1) to determine the motor torque vs time profile and demonstrate that this is correct based upon a simulation.
(B)  Based upon the results from(A) use the machine parameters to determine the voltages and currents required at the following operating points (shown as stars on the speed Vs time profile inFigure 2) and assess any loss at these points.
• Operating point 1 (P1): Maximum positive electromagnetic torque at maximum positive velocity (time, t = 3.49s). Assume at this point, the electrical frequency of the machine is fe   = 25Hz
• Operating point 2 (P2): Half way through the deceleration phase at time t = 88.25s  (or when
̇(x)1  = 1.75m/s). Assume at this point, the electrical frequency of the machine is fe   = 12. 5Hz
(C)  Demonstrate the validity of your voltages and currents using a simulation and finally assess efficiency of the electro-mechanical energy conversion process at these operating points.
DRIVE (CONVERTER) 
(D)  Using the operating points detailed in step(B), assess the harmonic spectrum, total harmonic distortion and capacitor ripple for a 3-phase, 2-level inverter that result from one or more modulation schemes and sampling methods.   Focus on delivering a simple solution that could be easily implemented on a digital, low-cost micro-controller.  Select an appropriate switching frequency, fsw  and sampling interval, Ts  based upon the calculated fundamental electrical frequency of the machine at the highest rotational speed.
•    Remember for effective use of the FFT tool to ensure that the switching frequency,fsw  is an integer multiple of the fundamental electrical frequency of the machine at your selected operating point.
•    You will be provided with a capacitor datasheet on blackboard from which you can construct
your DC link capacitance
(E)  Use  the  harmonic  spectrum  from (D) to  assess  the  impact  of  harmonic  components  above  the fundamental frequency on loss in the machine.  Assume that for the purposes of this calculation that
you can use the machine resistance, Rs  and inductance, Ls   =  for all frequencies
POWER ELECTRONICS (SWITCHES) 
Use the outcomes from(B)and(E)to select a switch and diode to use in the converter based upon the range of devices selected for you and whose datasheets will be made available on blackboard.
(F)  Model the total loss in the converter arising from the switch and diodes over a single electrical cycle at the chosen operating points
(G) Select a heat sink to allow the devices to remain in a safe operating region thermally.
SUMMARY 
(H) Summarise key aspects of your design process , reflect on your design.
HIGHER MARKS If you have time and want to achieve the higher marks, then change at least one aspect of your design and redo your analysis for the drive reflecting on the outcome of the change made.   Ideally,  you  should  be exploring an optimisation to make operation more efficient or effective.
Provided models
LINKS TO SUPPLIED MODELS -https://tinyurl.com/EENG30013CourseworkSubmit2425 
You  have  been  provided with a  model that contains a standard  PMSM  machine  model implemented in SIMULINK with the model parameters for the motor being considered.
Elevator Drivetrain ( Load) Parameters 
The parameters that describe the details of the load shown schematically inFigure 2are given inTable 1. 
Table 1: Mechanical Load Parameters 

Machine Parameters 
Parameters that define the 3-phase, AC, Permanent Magnet Synchronous Machine (PMSM) machine are given inTable 2. They are based upon the B  R Automation 8KSC96 motor.
Table 2: Machine Parameters 

Datasheets 
A datasheet for
•    the motor (B  R Automation 8KSC96)                       •    the semiconductor devices (Switch and Diode)
•    the capacitor for this problem,                                     •    the heatsinks
to  be considered are  provided in “Datasheets” item on  Blackboard  in the “Assessment, submission and feedback” for this unit.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
