# Digital-vlsi-soc-design-repo

# Day 1:Inception of Open source EDA, OpenLANE and Sky130PDK 

Introduction to QFN-48 Package,Chip,pads,core,die and IP’s 
Arduino is a popular open-source electronics platform based on easy-to-use hardware and 
software. It consists of a microcontroller (originally Atmel AVR family, now expanded to various 
architectures including ARM) and a development environment for writing software for the 
microcontroller. Microcontrollers are designed to be compact and contain all essential 
components on a single chip, including a CPU (Central Processing Unit), memory (both RAM and 
ROM), timers, and I/O (Input/Output) ports. Microcontrollers are typically programmed using 
high-level languages such as C or C++, as well as specialized integrated development 
environments (IDEs) provided by the microcontroller manufacturers. Program code is typically 
stored in non-volatile memory (ROM or flash memory) and executed by the microcontroller's 
CPU. 


The circled picture in the above image describes about the processor and its connectivity.

The below picture refers to Package. The pin placements are determined by the Arduino board 
under the development. The connectivity between the chip and the package are illustrated 
through the wires which determines the transmission of signals in and out of the chip. 


Components: 

Pads: 
• Pads refer to the interface between the chip and the outside world. They are the 
connection points on the integrated circuit (IC) where signals enter and exit the 
chip. Pads are typically arranged around the periphery of the chip and are used for 
various purposes such as power supply, ground, input/output (I/O), and 
test/debugging. 

2. Core: 
• In semiconductor design, the core usually refers to the central processing unit 
(CPU) or the main computational unit of a chip. It is the part of the chip 
responsible for executing instructions, performing calculations, and managing 
data processing tasks. In more general terms, a core can also refer to a 
fundamental functional block or module within a chip, such as a processing core, 
memory core, or graphics core.

4. Die: 
• Die refers to a single semiconductor chip that has been fabricated on a wafer 
during the semiconductor manufacturing process. A wafer typically contains 
multiple copies of the same chip design, known as die. After the fabrication 
process is complete, the wafer is diced into individual die, each containing a fully 
functional semiconductor chip.

6. Macros: 
• Macros, short for macrocells or macroblocks, are predefined functional blocks or 
modules that can be integrated into a larger chip design. These macros are often 
used to implement commonly used functions such as memory controllers, 
input/output (I/O) interfaces, or digital signal processing (DSP) blocks. 
Integrating macros into a chip design can help reduce design time, minimize 
development costs, and improve overall design efficiency.

8. Foundry IP's (Intellectual Property): 
• Foundry intellectual property (IP) refers to reusable design blocks or components 
provided by semiconductor foundries for use in chip designs. Foundry IP's 
typically include standard cell libraries, memory compilers, I/O libraries, and 
specialized IP blocks optimized for the foundry's manufacturing process 
technology. These IP blocks help chip designers accelerate the design process, 
reduce development risks, and take advantage of the foundry's manufacturing 
expertise.

In summary, pads provide the interface between the chip and the outside world, the core is the 
central computational unit of a chip, die refers to individual semiconductor chips on a wafer, 
macros are predefined functional blocks used in chip designs, and foundry IP's are reusable 
design components provided by semiconductor foundries to facilitate chip design and 
manufacturing.

#Introduction to RISC-V: 

RISC-V is an open-source instruction set architecture (ISA) based on Reduced Instruction Set 
Computing (RISC) principles. In order to execute a C-program on a chip with a particular layout, 
it has to be compiled into language program like RISC-V. Then this is converted into machine 
language in a binary format which is easily understood by the computer hardware. 
The RISC-V specifications have to be translated to hardware description language(HDL) to pass 
on layout. So, C Programming is executed and should get automatically executed by the 
hardware to get the output.

From a software application to hardware, the concept of macros can 
be understood in various contexts: 

1.Software Application:In software applications, macros are often used to automate 
repetitive tasks or to streamline complex operations. For example, in a spreadsheet program like 
Microsoft Excel, users can create macros to automate calculations, formatting, or data 
manipulation tasks. These macros can be recorded by the user performing a series of actions and 
then replayed to execute the same sequence of actions automatically. 

2. Operating System: Within an operating system, macros can be used to 
define system-wide settings or configurations. For instance, in Unix-like systems, 
shell scripts can include macros to simplify the execution of common tasks or to 
define environment variables that affect the behavior of various programs.

3. Programming Languages: In programming languages, macros are often 
used to define reusable code snippets or to create domain-specific languages. For 
example, in the C programming language, macros are defined using the #define 
directive and can be used to create constants, inline functions, or to implement 
conditional compilation.

5. Hardware Description Languages (HDLs):When it comes to 
hardware, macros are commonly used in Hardware Description Languages (HDLs) 
like Verilog or VHDL. In HDLs, macros, often referred to as macros or macros, are 
used to define reusable hardware components or configurations. These macros can 
represent complex digital circuits, such as adders, multiplexers, or even entire 
subsystems. HDL macros are instantiated within larger designs to create hierarchical 
structures and to facilitate modular design practices.
 
7. Electronic Design Automation (EDA) Tools: In the context of 
electronic design, macros play a crucial role in EDA tools such as synthesis and 
place-and-route tools. Macros in this domain represent predefined blocks of 
hardware that have been optimized for performance, power, or area. These macros 
can be instantiated multiple times within a design to achieve scalability and 
efficiency.

Overall, macros bridge the gap between software and hardware by providing a 
mechanism for abstraction, automation, and reusability in both domains. Whether 
in software applications, operating systems, programming languages, or hardware 
design, macros help streamline development processes and improve productivity.


Flow: Stopwatch app to Hardware 


Flow: ISA->HDL->Netlist->Physical design 

#Soc Design and Openlane

Introduction to all components of opensource digital asic design: 

To design an ASIC, we require RTL designs, EDA tools and PDK data.




1.RTL IP's (Register Transfer Level Intellectual Property): 
 
• RTL IP refers to pre-designed and pre-verified functional blocks or 
modules described at the Register Transfer Level (RTL), which is a level of 
abstraction in digital design representing the flow of data between 
registers in a digital circuit. RTL IP's are typically used as building blocks in 
the design of larger integrated circuits (ICs) or Systems-on-Chip (SoCs). 
Examples of RTL IP's include processor cores, memory controllers, interface 
controllers (e.g., USB, PCIe), and specialized accelerators (e.g., DSP, 
cryptography).

2. EDA Tools (Electronic Design Automation Tools):

• EDA tools are software applications used by semiconductor and electronic 
design engineers to design, verify, simulate, and test electronic systems 
and integrated circuits (ICs). These tools automate various stages of the 
design process, from logic design and synthesis to physical design, 
verification, and manufacturing. 

Common categories of EDA tools include: 

• RTL Design Tools: Used for designing and verifying digital logic at 
the Register Transfer Level (RTL). 
optimized for specific target technologies. 

• Synthesis Tools: Convert RTL descriptions into gate-level netlists 

• Simulation Tools: Verify the functional correctness of the design 
through simulation at various levels of abstraction (RTL, gate-level, 
transistor-level). 

• Place and Route Tools: Determine the physical layout of 
components on a chip and the routing of interconnects between 
them. 

• Timing Analysis Tools: Ensure that the design meets timing 
constraints and performance requirements. 

• Physical Verification Tools: Check the design for manufacturing
related issues such as design rule violations, layout errors, and 
electrical rule violations. 

3. PDK (Process Design Kit):
   
• A PDK is a collection of files and models provided by a semiconductor 
foundry that contains information about the manufacturing process 
technology used to fabricate integrated circuits (ICs). It includes data such 
as design rules, device models, parameterized cells (PCells), technology 
files, and simulation models required by electronic design automation 
(EDA) tools to design and verify ICs. Designers use PDKs to develop chip 
designs that are compatible with the manufacturing process offered by the 
foundry. PDKs are essential for ensuring that chip designs meet the 
fabrication requirements and constraints of the foundry's manufacturing 
process. 


In summary, RTL IP's are pre-designed functional blocks described at the Register 
Transfer Level, EDA tools are software applications used for electronic design 
automation, and PDKs are collections of files and models provided by semiconductor 
foundries that contain information about the manufacturing process technology used to 
fabricate integrated circuits. These components play crucial roles in the design, 
verification, and fabrication of electronic systems and ICs.




#Simplified RTL2GDS flow


1.Synthesis: In the synthesis stage, the RTL description is translated into a gate-level netlist 
using synthesis tools. These tools map the RTL code to standard cell libraries provided by the 
semiconductor foundry. The resulting gate-level netlist represents the circuit in terms of logic 
gates and their interconnections.



2. Floorplanning: Floorplanning involves partitioning the chip area into functional blocks and 
allocating resources such as memory, logic cells, and I/O pads. The goal is to optimize the 
physical layout of the chip to minimize signal delays, reduce power consumption, and meet 
performance targets.




Power planning is a crucial step in the RTL-to-GDS (Register Transfer Level to Graphic Data 
System) flow, particularly in the physical design stage of integrated circuit (IC) development. 
Power planning involves the distribution of power and ground signals throughout the chip to 
ensure reliable operation and efficient power delivery. In the power grid design stage, the chip's 
floorplan is overlaid with a grid of power and ground rails to distribute power and ground 
signals uniformly across the chip. Power planning tools determine the optimal placement of 
power and ground lines to minimize resistance, reduce voltage drop, and mitigate noise.


3.placement: In the placement stage, the synthesized and optimized logic cells are placed 
within the chip's floorplan. Placement tools determine the physical locations of logic cells to 
minimize wire lengths, reduce congestion, and satisfy timing constraints. Advanced placement 
algorithms consider factors such as signal timing, power distribution, and thermal effects. 


4. Clock Tree Synthesis (CTS): Clock tree synthesis involves the generation of a 
hierarchical clock distribution network to distribute clock signals uniformly across the 
chip. CTS tools optimize clock routing to minimize skew, ensure clock signal integrity, 
and meet timing requirements.


5. Routing: The routing stage involves the generation of physical metal interconnects 
(wires) to connect the placed logic cells according to the synthesized netlist. Routing 
tools handle the complex task of routing signals while considering design rules, signal integrity, and timing constraints. Global routing establishes the overall routing topology, 
while detailed routing handles the routing of individual metal tracks.


6.Sign off:Functional verification ensures that the design behaves correctly according 
to its specifications. Simulation-based techniques, such as RTL simulation 
and gate-level simulation, are used to verify the functionality of the design 
under various operating conditions and test scenarios. Functional 
coverage analysis is performed to ensure that all functional aspects of the 
design have been adequately exercised.




#Introduction to OpenLANE and strive chipsets

OpenLane is an automated RTL-to-GDSII (Register Transfer Level to Graphic Data System II) flow 
for designing integrated circuits. It encompasses a range of tools and scripts to automate 
various steps in the ASIC design process, from synthesis and placement to routing and timing 
analysis. OpenLane is built upon the OpenROAD framework, which provides an end-to-end 
design flow for digital ASICs. 
The openlane flow based on several components including OpenROAD, Yosys, Magic, 
Netgen, CVC, SPEF-Extractor, KLayout and a number of custom scripts for design 
exploration and optimization.





The objective of OpenLANE is to produce a clean GDSII (No LVS violations, No DRC 
violations, and no Timing violations) with no human intervention.

#Introduction to OpenLANE detailed ASIC design flow


1. Synthesis Exploration step involves generation of reports showing delay vs area

2.Design Exploration step is used to sweep the design configuration and it's useful 
to find best configuration for any given design.

3. OpenLANE Regression Testing

4.  Design for Test (DFT)

5.  Physical verification (DRC & LVS)

6.   Logic Equivalence Check (LEC) checks the logic synchronisation between physical 
implementation and the netlist.

7.Dealing with Antenna Rules violations


8. Static Timing Analysis (STA) ensures that the design meets timing requirements. 
STA evaluates the timing behavior of a digital circuit without considering dynamic 
factors such as signal transitions and clock skew. It determines whether the 
design meets setup and hold time constraints, maximum clock frequency, and 
other timing requirements. The input to STA includes the synthesized netlist of 
the design, and timing constraints.



#Getting familiar to open-source EDA tools:

 Openlane Directory structure in detail  

 • open-pdks contains scripts that makes the commerical PDK to also be compatible 
with the open-source EDA tool 

• sky130A pdk variant is made especially compatible for open-source tools. It 
contains libs.ref and libs.tech libs.ref contains all the process or technology 
specific files, example sky130_fd_sc_hd : Sky130nm Foundry Standard Cell High 
Density libs.tech has files specific for the tool (klayout,netgen,magic...) 

• skywater-pdk contains all Skywater 130nm PDKs


#Design Preparation Step

Openlane has multiple designs and we need to work on picorv32a inside a specific 
design folder there is a config.tcl which has the default settings on OpenLANE.

<img width="686" height="526" alt="image" src="https://github.com/user-attachments/assets/27b908e0-bedd-4b0e-beae-f4b2c0e030a8" />




The priority order for the Openlane settings are: sky130_xxxxx_config.tcl in 
OpenLane/designs/[design]/ config.tcl in OpenLane/designs/[design]/ default values in 
OpenLane/configuration/


Setup the design stage for the flow and to begin with synthesis of a design 

prep -design picorv32a 
The above command when executed, sets up the filesystem where the OpenLANE tools 
can dump the outputs. This creates a run/ folder inside the picorv32a directory which 
contains the command log files, results, and the reports dumped by each tool. The 
folder will be empty for now except for lef files generated by this design setup stage.

The cell LEF files .lef and technology LEF files .tlef merge to generate merged.lef inside 
run/tmp/ 




# Snapshots of files after design prep, run synthesis, and characterize 
synthesis results

Run synthesis with the command: run_synthesis  runs by yosys, RTL synthesis, ABC 
scripts (for technology mapping) and openSTA.


Results after synthesis is as follows.








Here the DFF count: sky130_fd_sc_hd__dfxtp_2 = 1613 
And total number of cells = 14876 

D flip-flop ratio = count of DFFs / total number of cells = 1613 / 14876 = 0.108429685 
(OR) 10.8429 % 

After running synthesis, inside the runs/[date]/results/synthesis is picorv32a_synthesis.v 
which is the mapping of the netlist to standard cell library using ABC. The 
runs/[date]/reports/synthesis will contain synthesis statistic reports and STA reports. The 
log files are: 




#Good floorplan vs bad floorplan and introduction to library cells

Chip Floor planning considerations 

Utilization factor and aspect ratio 

1. Define width and height of core and die 
Core: The core refers to the central functional area of the integrated circuit where 
the actual circuitry and logic reside. The width and height of the core typically 
refer to the dimensions of this functional area, which contains the active 
components of the chip, such as logic gates, memory cells, and other functional 
blocks. The width and height of the core are essential parameters that influence 
the overall size and aspect ratio of the chip.

3. Die: The die represents the individual unit of an integrated circuit that is 
fabricated on a semiconductor wafer during the manufacturing process. The die 
contains the entire functional circuitry of the chip, including the core, as well as 
additional features such as bonding pads, I/O interfaces, and metal layers for 
interconnections. The width and height of the die correspond to the dimensions 
of the rectangular or square-shaped semiconductor substrate on which the 
circuitry is fabricated.

In summary, the width and height of the core and die of an integrated circuit refer to 
the dimensions of the functional circuit area and the entire semiconductor substrate, 
respectively. These dimensions are critical parameters in IC design and manufacturing, 
ifluencing factors such as chip size, layout optimization, and packaging considerations.








Let's calculate the area occupied by the above netlist on a silicon wafer. Before that 
the wires are ignored and the flops and combinational logic are combined together to 
get the total area. So, here, the area will be 4 sq.units. 








Utilization factor = (4 x 1sq.unit) / (2 unit x 2 unit) = 1 
which means the core is completely occupied. In practical scenario, utilization is about 
50% 
Aspect ratio = Height / Width 
In this case, height and width are same, so the aspect ratio is 1 If the aspect ratio is 1 it 
shows that the chip is square, otherwise it is rectangle. 
Example: 






1. Utilization factor = (4 sq.units) / (8 sq.units) = 0.5 
Aspect ratio = 2 / 4 = 0.5


#Concept of pre-placed cells 

2. Define Locations of Preplaced Cells

Preplaced cells (also known as pre-placed instances or pre-placed blocks) are specific 
circuit elements within an integrated circuit design layout that are manually positioned 
in advance by the designer. The locations of preplaced cells are predetermined and fixed 
before the automated placement and routing stages of the design flow.

the locations of preplaced cells are manually determined by the designer to optimize 
layout, performance, and connectivity within an integrated circuit design. By strategically 
positioning these cells and aligning them with key design elements, designers can 
improve overall chip performance and manufacturability.

Consider the following netlist being divided into two sets of blocks with connectivity 
preserved.





So, if Block1 has to be used by a designer, it can be directly handed over since it is 
blackboxed. This block can be used across the designs. It means the block can be 
reused. 





#De-coupling capacitors
Surround pre-placed cells with decoupling capacitors




Consider the circuit below as a part of a block. Whenever the circuit switches, there is an 
amount of current demand. For example, if the AND gate switches from logic0 to logic1, the 
capacitance has to completely charge. The amount of charge will be sent from the supply 
voltage. And when the logic switches from logic1 to logic0, the capacitance discharges and 
it's the responsibility of the Vss to take that discharged current. 

In reality, when the Vdd supplies voltage to the circuit, there is a drop due to resistance, 
inductance and capacitance of the wire and supplied volatge is Vdd'





The Vdd' should be within the noise margin range which is from Vih to Voh. If it is present 
somewhere in the undefined region, then the logic 1 is unstable. This is because of the large 
physical distance from the main power supply to the circuit.



Solution to such problem is the addition of decoupling capacitors. We can consider 
decoupling capacitor as a huge capacitor completely filled with charge. the equivalent 
voltage across the capacitor is same as seen across the main supply voltage. The capacitor 
decouples the circuit from the main supply.



#Power Planning 

Consider the circuit as a macro and it demands more current. Say, it's used as a driver as well as load and the load should receive the same signal quality as the driver. 



Decoupling capactor is not feasible to be added all over the chip but only on the critical elements.



In the below picture, 1 means the capacitor is charged to V and 0 means the capacitor is discharged. 
If the wire bus is connected to an inverter, then it means that all the capacitors charged to V will 
discharge at the same time. Large number of elements switching to logic0 might cause Ground 
Bounce due to huge amount of current that needs to be sinked at the same time, and switcing to 
logic 1 might cause Voltage Droop due to insufficient current from the power source to all elements. 
Ground bounce and Voltage Droop might cause the voltage to not be within the noise margin range. 
The solution is to have multiple powersource taps (power mesh) where elements can source current 
from the nearest Vdd and sink current to the nearest Vss tap.




Instead of single power supply as before, there are multiple Vdd and Vss lines. If a logic demands 
current, it can tap current from the nearest power supply.



# Pin placement and logical cell placement blockage

Let's take below design as an example to be implemented. The connectivity information between the 
gates is coded usign VHDL or Verilog language and is called as netlist.


The input and output ports are placed on the left and right spaces between the core and the die. The 
placements of the ports depends on where the cells are placed. The clock ports are bigger in size 
than data ports since the clocks are driving the cells continuously. So, we need the least resistance 
paths for the clocks. Bigger the size, lesser the resistance.


Once pin/port placement is done, Logical Cell Placement Blockage is created to make sure that the 
APR tool does not place any cell on the pin locations.


# Steps to run floorplan using OpenLANE and view floorplan layout in Magic

1. Setting configuration variables: Before running floorplan, the configuration variables or 
switches must be set. These are present in openlane/configuration directory:



The README.md consists of all configuration variables for every stage and the tcl files contain the 
default OpenLANE settings. 
2. Default parameters are set for floorplan stage in floorplan.tcl in OpenLANE 
3. All configurations/switches accepted by the current run are from 
openlane/designs/[design]/config.tcl 
The priority order from highest to lowest is as follows: 
• openlane/designs/[design]/sky130A_sky130_fd_sc_hd_config.tcl 
• openlane/designs/[design]/config.tcl 
• openlane/configuration/floorplan.tcl






In OpenLANE flow, the vertical and horizontal metals are one more than what we specify. If vertical 
metal is specified as 4, then it'll be 5, same case for horizontal. 

4. Run floorplan on OpenLane: % run_floorplan
   
5. Floorplan output files are generated in this folder
   
openlane/designs/picorv32a/runs/date/results/floorplan/picorv32a.floorplan.def which is a 
design exchange format, containing the die area and positions. The die area in this file is in 
database units and 1 micron is equivalent to 1000 database units. Area of die = 
(554570/1000) microns * (565290/1000) microns = 311829.1653 um^2 

6. To view the layout after floorplan, we use magic tool 
Command: magic -T 
/home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs
.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read 
picorv32a.floorplan.def &



Press "s" to select whole die then press "v" to center the view 

Point the cursor to a cell then press "s" to select it, zoom into it by pressing "z" 

The IO pins are placed in a random equidistant mode as seen below based on the 
configuration (FP_IO_MODE = 1) set in openlane/configuration/floorplan.tcl



The components in the layout can be identified by using the "what" command in tkcon 
window after selecting it.


Standard cells are not placed but can be viewed at the bottom left corner of the layout


# Library Binding and Placement 

# Netlist binding and initial place design 
1. Bind netlist with physical cells 
Bind the netlist to physical cells with real dimensions. The physical cells come from a library 
that contains cells which can have different dimensions, various shapes of the cells, and delay 
information. Bigger cells have lesser resistance while the functionality is the same. This means 
that the library has many flavors of cells.

3. Placement:




Placement is done based on connectivity. For example, FF1 is close to Din1 pin and FF2 close 
to Dout1 pin and combinational cells placed nearer to FF1 and FF2. This is to reduce delay.


Optimize placement using estimated wire-length and capacitance 

This is the stage where we estimate wirelength and capacitance (C=EA/d) and insert repeaters based 
on that. If the wirelength is more, then to maintain signal integrity, we add repeaters to reduce 
resistance. Repeaters basically reconditions the original signal and transfers.




Congestion aware placement using RePlAce 

Run placement on OpenLane: % run_placement 
This commmand is a wrapper which does global placement (by RePlace tool), Optimization (by Resier 
tool), and detailed placement (by OpenDP tool).

Placement is done in two stages: 

• Global Placement : no legalization takes place and uses Half Perimeter Wirelength (HPWL) 
reduction model. 

• Detailed Placement : legalization happens where the standard cells are placed in stadard 
rows, and there will be no overlaps of the cells. 

The objective of placement is to converge the overflow value. If overflow value progressively reduces 
during the placement,then it implies that the design will converge and placement will be successful. 

After running the placement, output is generated in this folder 
/openlane/designs/picorv32a/runs/date/results/placement/picorv32a.placement.def 
Command: magic -T 
/home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/
magic/sky130A.tech lef read ../../tmp/merged.lef def read 
picorv32a.placement.def &




# Cell design and characterization flows 

All standards cells (AND, OR, BUFFER, INVERTER, flip-flops etc.) are present in standard cell library. 
The cells inside the library are of different flavors (different drive strengths, functionality, threshold 
voltage). If the cell size is more, then the drive strength is high to drive longer wires. If the threshold 
voltage is high, then it will take more time to switch than the one with lesser threshold voltage. 



• DRC & LVS Rules: tech files and poly substrate parameters 
• SPICE Models: Threshold, linear regions, saturation region equations with added foundry 
parameters, including NMOS and PMOS parameteres 
• User defined Spec: Cell height, cell width (drive strength), supply voltage, pin locations, metal 
layer requirement 
• The standard cell library developer must adhere to the rules given so that when the cell can 
be used on a real design without any errors 
• Circuit design is done modeling the pmos and nmos to meet input library requirement 
• Layout design is done using Euler's path and stick diagram on Magic layout too



Steps of characterization flow: 
1. Read the spice model files 
2. Read the extracted spice netlist 
3. Define/Recognise the buffer behavior 
4. Read the subcircuits 
5. Attach the necessary power sources 
6. Apply stimulus 
7. provide necessary output capacitance 
8. provide simulation command





Timing characterization 
Syntax and semantics of power.lib, timing.lib and noise.lib. These are necessary to understand the 
GUNA software workflow. 
We are taking inverters connected back to back as an example.


Timing thershold definitions: 


Two inverters in series, red is output of first inverter and blue is output of second inverter:



The red is input waveform and blue is output waveform of the buffer. The left side is rise delay and 
right side is fall delay. 
PROPOGATION DELAY= time(out_*_thr)-time(in_*_) 
TRANSITION DELAY=time(slew_high_*_thr)-time(slew_low_*_thr) 
Negative propagation delay is not expected. This means that the output comes before the input so 
it's important to choose correct threshold point to produce positive delay. Delay threshold is usually 
50% and slew rate threshold is usually 20%-80%.


# Design library cell using Magic Layout and ngspice 
characterization 
Labs for CMOS inverter ngspice simulations


IO placer revision 
Configuration settings in OpenLANE can be changed in the shell itself, on the fly. For example, to 
make IO_mode not to be "random equidistant", 
% set ::env(FP_IO_MODE) 2  
The IO pins will not be equidistant in mode 2 (default of 1). On re-running floorplan, we can see that 
the pins are placed based on of the Hungarian algorithms. The pins are stacked one over the other. 
However, changing the configuration on the fly will not change the runs/config.tcl, the configuration 
will only be available on the current session.







To echo current value of variable, 
echo $::env(FP_IO_MODE) 

# SPICE deck creation and simulation for CMOS inverter

SPICE deck comprises of connectivity information about the netlist, inputs to be provided to the 
simulation, information on tap points at which output will be taken and so on. Component values in 
SPICE DECK: For PMOS, W/L (0.375u/0.25u means width is 375nm and lengthis 250nm). PMOS 
should be wider (atleast 2x or 3x) than NMOS. PMOS hole carrier is slower than NMOS electron 
carrier mobility, so to match the rise and fall time, PMOS must be wider (less resistance thus higher 
mobility) than NMOS. But in this case, we are taking same sizes for both PMOS and NMOS. The gate 
voltage is normally a multiple of length (250nm) (in the example, gate voltage can be 2.5V)

SPICE deck: 
• component connectivity 
• component values 
• identify nodes 
• name nodes




SPICE deck netlist description: 

• Syntax for the PMOS and NMOS: [component name] [drain] [gate] [source] [substrate] 
[transistor type] W=[width] L=[length] 
• All components are described based on nodes and its values 
• .op is the start of SPICE simulation operation where Vin will be sweep from 0 to 2.5 with 
0.05V steps 
• tsmc_025um_model.mod is the model file containing the technological parameters for the 
0.25um NMOS and PMOS



The steps to follow for SPICE simulation, 
1. Go to ngspice simulator 
2. Source the .cir spice deck file 
3. Execute the spice file by command: run 
4. Execute command: setplot --> allows you to view any plots possible from the simulations 
specified in the spice deck 
5. Select the simulation desired by entering the simulation name in the terminal 
6. Execute command: display --> to see which nodes available for plotting 
7. Execute command: plot out vs in We can see the plot for above inputs. In this the width of 
both PMOS &NMOS is same.


Switching Threshold Vm 



1. The shapes are almost the same which means that CMOS is a robust device. 
2. Parameters that defines the robustness of CMOS 
o switching threshold, Vm. It is the point where the Vin = Vout and both PMOS & 
NMOS are in saturation region. These will be turned on and there is high chances for 
leakage. There is a high possibility that the current flows directly from VDD to GND. 
Due to this, short circuit kind of device is seen.



• Propagation delay: rise or fall delay

Static and dynamic simulation of CMOS inverter 

DC transfer analysis is used for finding switching threshold. Simulation is DC sweep from 0V to 2.5V 
with 0.05V steps: 
When a pulse is applied to the CMOS, transient analysis is used to find propagation delay.





Lab steps to gitclone vsdstdcelldesign


Instead of designing an inverter from scratch, a github repository where this is already done is 
cloned to observe the layout. 
1. Clone custom inverter standard cell design from github repository 
2. Change directory to openlane: cd ~/Desktop/work/tools/openlane_working_dir/openlane 
3. Clone the repository with custom inverter design: git clone https://github.com/nickson
jose/vsdstdcelldesign 
4. Copy tech file to the vsdstdcelldesign directory: cp 
/home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sk
y130A.tech 
/home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign/ 
5. Open custom inverter layout in magic: magic -T sky130A.tech sky130_inv.mag &
   
Snippet of commands executed:




Snippet of sky130_inv: 


# Inception of Layout CMOS fabrication process

CMOS Fabrication Process (16-Mask CMOS Process): 
1. Select a substrate

   
2. Create active region for transistors 
o Deposit Silicon Dioxide (SiO2) on the substrate 
o Deposit Silicon Nitride (Si3N4). It is a protection layer to prevent SiO2 layer to grow 
during oxidation 
o Deposit a layer of photoresist 
o Deposit mask-1 layer on top of photoresist. It covers the photoresist layer that must 
not be etched away (protects the two transistor active regions) 
o UV light is applied to remove unmasked portions 
o Remove mask-1 and photoresist layers 
o Place in furnace to grow the oxide in the other areas 
o Remove the Si3N4 layer using hot phosphoric acid to have only p-substrate and Sio2



3. N-Well and P-Well formation 
o Deposit photo resist layer to define the areas to protect 
o Deposit mask-2. Mask 2 protects the N-Well (PMOS side) while P-Well (NMOS side) is 
being fabricated then Mask 3 protects P-Well while N-Well is being formed 
o UV light is applied, and the exposed area of photoresist will be removed 
o Boron is used to form P-Well 
o Phosporus is used to form N-well 
o Place in furnace to diffuse boron and phosphorous to form wells. This process is 
called Twintub process.


4. Formation of gate terminal 
Gate terminal is where the threshold voltage is controlled.



o Deposit photo resist layer to define the areas to protect 
o Deposit mask-4 
o UV light is applied, and the exposed area of photoresist will be removed 
o Implant low energy boron at the surface of p-well using mask-4 to control the 
threshold 
o Implant phosphorous/arsenic for n-well using mask-5 
o Fix the oxide which is damaged by implantation steps by removing extra SiO2 using 
the hydroflouric acid and re-grow high quality SiO2 on p-substrate to contol the 
oxide thickness 
o Add polysilicon film 
o Add mask-6 and etch using photolithography 
o Etch off to form the gate terminal 


5. Lightly Doped Drain (LDD) formation 
Two reasons for LDD: hot electron effect & short channel effect 
o Mask 7 for NMOS (lightly doped N-type) 
o Mask 8 for PMOS (lightly doped P-type) 
o Heavily doped impurity (N+ for NMOS and P+ for PMOS) is for the actual source and 
drain but the lightly doped impurity will help maintain spacing between the source 
and drain and prevent hot electron effect and short channel effect. 
o To protect the lightly doped regions, add SiO2 and create spacers using plasma 
anisotropic etching


7. Source and Drain formation 
o Thin screen oxide is formed to avoid channeling. Channeling is when implantations 
dig too deep into substrate. 
o Mask-9 is for N+ implantation and Mask-10 for P+ implantation 
o The side wall spacers maintain the N-/P- while implanting the N+/P+ 
o High temperature annealing is done

8. Local interconnect formation 
o Contacts and interconnects are important to control the electrical characteristics by 
the designer. 
o Remove thin screen oxide to open up the source, drain and gate for building the 
contacts. 
o Titanium has less resistance and hence used 
o TiSi2 is used for local interconnects 
o Mask 11 is formed and TiN is etched off using RCA cleaning to create first level 
contact


9. Higher level metal formation 
o CMP (Chemical Mechanical Polishing) technique to planarize the surface 
o Create contact holes using photolithograhy process 
o Mask 12 is for first contact hole 
o Mask 13 is for first Aluminum contact layer 
o Mask 14 is for second contact hole 
o Mask 15 is for second Aluminum contact layer 
o Mask 16 is for making contact to topmost layer

# Lab introduction to Sky130 basic layers layout and LEF using 
inverter 









