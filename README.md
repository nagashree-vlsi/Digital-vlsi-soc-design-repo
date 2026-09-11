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


<img width="464" height="370" alt="image" src="https://github.com/user-attachments/assets/2d0c2770-c195-488d-9ba7-01c9feef5465" />


The circled picture in the above image describes about the processor and its connectivity.


<img width="388" height="223" alt="image" src="https://github.com/user-attachments/assets/b0b1ed76-7357-4fa1-9d3b-df44c2d46e6a" />






The below picture refers to Package. The pin placements are determined by the Arduino board 
under the development. The connectivity between the chip and the package are illustrated 
through the wires which determines the transmission of signals in and out of the chip. 


<img width="793" height="311" alt="image" src="https://github.com/user-attachments/assets/02bd337f-df61-42bc-8b65-1f4df2b22952" />



Components: 

<img width="674" height="382" alt="image" src="https://github.com/user-attachments/assets/a0b3d8d2-612b-4594-9ea9-d0eae3dbd048" />


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


<img width="593" height="358" alt="image" src="https://github.com/user-attachments/assets/c1370656-627a-4e95-b83b-cc410e72446d" />


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


<img width="654" height="368" alt="image" src="https://github.com/user-attachments/assets/afa7f411-ab01-4d53-b35f-46d646198449" />


Flow: Stopwatch app to Hardware 


<img width="580" height="319" alt="image" src="https://github.com/user-attachments/assets/976ffa10-f021-4bfc-95d9-e58b82184994" />



Flow: ISA->HDL->Netlist->Physical design 

#Soc Design and Openlane

Introduction to all components of opensource digital asic design: 

To design an ASIC, we require RTL designs, EDA tools and PDK data.


<img width="737" height="370" alt="image" src="https://github.com/user-attachments/assets/5db814f9-cd05-4d56-81ba-95fe25a138cd" />





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


<img width="720" height="319" alt="image" src="https://github.com/user-attachments/assets/40a860c5-2089-478a-9483-964a7c3ae503" />


<img width="609" height="337" alt="image" src="https://github.com/user-attachments/assets/2e91327c-8fb5-4592-b698-96647da27b56" />



#Simplified RTL2GDS flow

<img width="724" height="350" alt="image" src="https://github.com/user-attachments/assets/7b40e715-d4af-417d-9e4b-f026034e1f82" />





1.Synthesis: In the synthesis stage, the RTL description is translated into a gate-level netlist 
using synthesis tools. These tools map the RTL code to standard cell libraries provided by the 
semiconductor foundry. The resulting gate-level netlist represents the circuit in terms of logic 
gates and their interconnections.

<img width="730" height="309" alt="image" src="https://github.com/user-attachments/assets/21b0a0b7-911a-4922-8982-69620573404d" />





2. Floorplanning: Floorplanning involves partitioning the chip area into functional blocks and 
allocating resources such as memory, logic cells, and I/O pads. The goal is to optimize the 
physical layout of the chip to minimize signal delays, reduce power consumption, and meet 
performance targets.


<img width="732" height="380" alt="image" src="https://github.com/user-attachments/assets/85a8689f-9b91-47da-a90e-c3fde785da86" />





Power planning is a crucial step in the RTL-to-GDS (Register Transfer Level to Graphic Data 
System) flow, particularly in the physical design stage of integrated circuit (IC) development. 
Power planning involves the distribution of power and ground signals throughout the chip to 
ensure reliable operation and efficient power delivery. In the power grid design stage, the chip's 
floorplan is overlaid with a grid of power and ground rails to distribute power and ground 
signals uniformly across the chip. Power planning tools determine the optimal placement of 
power and ground lines to minimize resistance, reduce voltage drop, and mitigate noise.

<img width="754" height="400" alt="image" src="https://github.com/user-attachments/assets/ca3a5b84-1cb5-424d-9e9e-1925be2c927d" />



3.placement: In the placement stage, the synthesized and optimized logic cells are placed 
within the chip's floorplan. Placement tools determine the physical locations of logic cells to 
minimize wire lengths, reduce congestion, and satisfy timing constraints. Advanced placement 
algorithms consider factors such as signal timing, power distribution, and thermal effects. 


<img width="734" height="377" alt="image" src="https://github.com/user-attachments/assets/b170139b-6952-45c7-9a72-c3c62daedcb4" />


<img width="731" height="394" alt="image" src="https://github.com/user-attachments/assets/ec7b158d-b159-48a5-8f88-94f05b2639d2" />


4. Clock Tree Synthesis (CTS): Clock tree synthesis involves the generation of a 
hierarchical clock distribution network to distribute clock signals uniformly across the 
chip. CTS tools optimize clock routing to minimize skew, ensure clock signal integrity, 
and meet timing requirements.


<img width="737" height="412" alt="image" src="https://github.com/user-attachments/assets/88197334-920f-4640-abac-8ea0ad04c4da" />




6. Routing: The routing stage involves the generation of physical metal interconnects 
(wires) to connect the placed logic cells according to the synthesized netlist. Routing 
tools handle the complex task of routing signals while considering design rules, signal integrity, and timing constraints. Global routing establishes the overall routing topology, 
while detailed routing handles the routing of individual metal tracks.


<img width="732" height="379" alt="image" src="https://github.com/user-attachments/assets/47c06e65-5bbd-4197-b893-ab6561887d8a" />



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


<img width="787" height="701" alt="image" src="https://github.com/user-attachments/assets/d69f9be0-1273-4244-8d66-b4926a61e6ae" />






The objective of OpenLANE is to produce a clean GDSII (No LVS violations, No DRC 
violations, and no Timing violations) with no human intervention.

#Introduction to OpenLANE detailed ASIC design flow


<img width="721" height="323" alt="image" src="https://github.com/user-attachments/assets/4063e60f-b428-4cf7-bd89-20ae20c09f31" />



1. Synthesis Exploration step involves generation of reports showing delay vs area


<img width="715" height="319" alt="image" src="https://github.com/user-attachments/assets/55c15e8c-8610-4de5-aa67-f1570732827a" />

2.Design Exploration step is used to sweep the design configuration and it's useful 
to find best configuration for any given design.


<img width="721" height="324" alt="image" src="https://github.com/user-attachments/assets/79bd660d-4f13-484b-a34f-7670d47e40b7" />


3. OpenLANE Regression Testing


<img width="730" height="375" alt="image" src="https://github.com/user-attachments/assets/4c27a448-8734-4153-a9a9-a8263b760886" />

4.  Design for Test (DFT)

   <img width="730" height="375" alt="image" src="https://github.com/user-attachments/assets/2b099717-912c-4d1c-a21c-a456d4b12223" />


6.  Physical verification (DRC & LVS)

   <img width="740" height="373" alt="image" src="https://github.com/user-attachments/assets/2399ce75-9b37-4f0f-b728-eeddfd9e2a89" />


8.   Logic Equivalence Check (LEC) checks the logic synchronisation between physical 
implementation and the netlist.

 <img width="715" height="310" alt="image" src="https://github.com/user-attachments/assets/ad5e048f-1f5d-48e2-8770-b0512cb0065d" />


7.Dealing with Antenna Rules violations


<img width="731" height="604" alt="image" src="https://github.com/user-attachments/assets/03a43ef5-1ef6-4e44-9342-8128ede6de46" />


<img width="684" height="314" alt="image" src="https://github.com/user-attachments/assets/bd652f4a-6fad-4216-9003-e665bdaed2a6" />


8. Static Timing Analysis (STA) ensures that the design meets timing requirements. 
STA evaluates the timing behavior of a digital circuit without considering dynamic 
factors such as signal transitions and clock skew. It determines whether the 
design meets setup and hold time constraints, maximum clock frequency, and 
other timing requirements. The input to STA includes the synthesized netlist of 
the design, and timing constraints.



#Getting familiar to open-source EDA tools:

 Openlane Directory structure in detail 


<img width="699" height="578" alt="image" src="https://github.com/user-attachments/assets/18b83f9f-a0c7-434d-be50-9d5a8b136f8d" />

 

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


<img width="773" height="127" alt="image" src="https://github.com/user-attachments/assets/3f75c84f-7a35-4c9e-9a26-0ba00d53de4b" />


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


<img width="723" height="409" alt="image" src="https://github.com/user-attachments/assets/e57434d0-fbfb-4dcf-bf54-42eee6bc03d8" />




<img width="753" height="393" alt="image" src="https://github.com/user-attachments/assets/2cf16634-d40d-46c4-b432-9108a179c05a" />



<img width="713" height="404" alt="image" src="https://github.com/user-attachments/assets/6e5003af-0a9b-460a-b383-94e112a7006c" />




Let's calculate the area occupied by the above netlist on a silicon wafer. Before that 
the wires are ignored and the flops and combinational logic are combined together to 
get the total area. So, here, the area will be 4 sq.units. 


<img width="775" height="356" alt="image" src="https://github.com/user-attachments/assets/8ce80db1-fed4-4a59-9137-b089d1d9d31d" />


<img width="747" height="452" alt="image" src="https://github.com/user-attachments/assets/e5b8748f-50ee-4cd6-a002-a22a7c71e0a5" />



<img width="767" height="365" alt="image" src="https://github.com/user-attachments/assets/6f11a6f1-935a-428e-ae13-3cbdc3de8738" />




<img width="692" height="414" alt="image" src="https://github.com/user-attachments/assets/5ec9b5ea-f2c0-4e69-9bc3-b49970b1f69f" />


Utilization factor = (4 x 1sq.unit) / (2 unit x 2 unit) = 1 
which means the core is completely occupied. In practical scenario, utilization is about 
50% 
Aspect ratio = Height / Width 
In this case, height and width are same, so the aspect ratio is 1 If the aspect ratio is 1 it 
shows that the chip is square, otherwise it is rectangle. 
Example: 


<img width="754" height="275" alt="image" src="https://github.com/user-attachments/assets/060d3c29-8f21-4d2c-85bb-7e4f832bcbf3" />





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


<img width="757" height="395" alt="image" src="https://github.com/user-attachments/assets/424338f5-553b-4ba7-bbe2-d73683286d6f" />


<img width="529" height="437" alt="image" src="https://github.com/user-attachments/assets/2e16f0a9-a199-47fc-830a-d1d8e86e7968" />



<img width="566" height="428" alt="image" src="https://github.com/user-attachments/assets/65a410db-5d94-4ffd-a67a-9fb903e14922" />




So, if Block1 has to be used by a designer, it can be directly handed over since it is 
blackboxed. This block can be used across the designs. It means the block can be 
reused. 



<img width="737" height="424" alt="image" src="https://github.com/user-attachments/assets/a15d647b-65a4-49f8-92a6-5827e5e8737e" />



#De-coupling capacitors
Surround pre-placed cells with decoupling capacitors


<img width="561" height="420" alt="image" src="https://github.com/user-attachments/assets/06a08c3c-3c75-44d9-80dc-0982894ed81b" />



Consider the circuit below as a part of a block. Whenever the circuit switches, there is an 
amount of current demand. For example, if the AND gate switches from logic0 to logic1, the 
capacitance has to completely charge. The amount of charge will be sent from the supply 
voltage. And when the logic switches from logic1 to logic0, the capacitance discharges and 
it's the responsibility of the Vss to take that discharged current. 

In reality, when the Vdd supplies voltage to the circuit, there is a drop due to resistance, 
inductance and capacitance of the wire and supplied volatge is Vdd'


<img width="657" height="465" alt="image" src="https://github.com/user-attachments/assets/cd8fa1ad-410c-482b-a2ee-ab23987ee550" />



<img width="646" height="285" alt="image" src="https://github.com/user-attachments/assets/dc884494-3143-4b5c-ae71-f48ee283b09b" />


The Vdd' should be within the noise margin range which is from Vih to Voh. If it is present 
somewhere in the undefined region, then the logic 1 is unstable. This is because of the large 
physical distance from the main power supply to the circuit.


<img width="658" height="454" alt="image" src="https://github.com/user-attachments/assets/07e41c75-2fd8-44f9-b3f6-a5d07138d179" />


Solution to such problem is the addition of decoupling capacitors. We can consider 
decoupling capacitor as a huge capacitor completely filled with charge. the equivalent 
voltage across the capacitor is same as seen across the main supply voltage. The capacitor 
decouples the circuit from the main supply.


<img width="436" height="233" alt="image" src="https://github.com/user-attachments/assets/cd91812f-8a0e-4dd2-8d4f-2de643761eaa" />


<img width="651" height="369" alt="image" src="https://github.com/user-attachments/assets/91dd65aa-46bd-4156-b414-fc74b16fde13" />

#Power Planning 

Consider the circuit as a macro and it demands more current. Say, it's used as a driver as well as load and the load should receive the same signal quality as the driver. 


<img width="364" height="351" alt="image" src="https://github.com/user-attachments/assets/7af8660b-de48-4ec3-bcb3-defa1859efb5" />


Decoupling capactor is not feasible to be added all over the chip but only on the critical elements.


<img width="427" height="377" alt="image" src="https://github.com/user-attachments/assets/1bd32906-63cc-465d-9a91-51538b1c0279" />


In the below picture, 1 means the capacitor is charged to V and 0 means the capacitor is discharged. 
If the wire bus is connected to an inverter, then it means that all the capacitors charged to V will 
discharge at the same time. Large number of elements switching to logic0 might cause Ground 
Bounce due to huge amount of current that needs to be sinked at the same time, and switcing to 
logic 1 might cause Voltage Droop due to insufficient current from the power source to all elements. 
Ground bounce and Voltage Droop might cause the voltage to not be within the noise margin range. 
The solution is to have multiple powersource taps (power mesh) where elements can source current 
from the nearest Vdd and sink current to the nearest Vss tap.


<img width="476" height="373" alt="image" src="https://github.com/user-attachments/assets/65938e5c-60b1-44de-bacf-61147bb59ba1" />



<img width="483" height="344" alt="image" src="https://github.com/user-attachments/assets/a74915ab-d0b8-4b5d-906b-f1bfe45c6f0b" />

Instead of single power supply as before, there are multiple Vdd and Vss lines. If a logic demands 
current, it can tap current from the nearest power supply.


<img width="470" height="379" alt="image" src="https://github.com/user-attachments/assets/159540ad-d2ff-4786-97d7-03106496d786" />


<img width="546" height="406" alt="image" src="https://github.com/user-attachments/assets/08b90114-9eff-4114-901e-870e5a55b1f6" />


# Pin placement and logical cell placement blockage

Let's take below design as an example to be implemented. The connectivity information between the 
gates is coded usign VHDL or Verilog language and is called as netlist.


<img width="449" height="417" alt="image" src="https://github.com/user-attachments/assets/25877ee6-0d35-4c20-aaee-1f21a8219128" />

The input and output ports are placed on the left and right spaces between the core and the die. The 
placements of the ports depends on where the cells are placed. The clock ports are bigger in size 
than data ports since the clocks are driving the cells continuously. So, we need the least resistance 
paths for the clocks. Bigger the size, lesser the resistance.

<img width="554" height="304" alt="image" src="https://github.com/user-attachments/assets/e80f3ce7-b974-438e-8567-332ed4f8eee0" />


Once pin/port placement is done, Logical Cell Placement Blockage is created to make sure that the 
APR tool does not place any cell on the pin locations.

<img width="574" height="405" alt="image" src="https://github.com/user-attachments/assets/0c5a7959-6744-460c-87c8-498d9e1d8ced" />


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


<img width="620" height="460" alt="image" src="https://github.com/user-attachments/assets/33bc22b1-6cde-4afd-817f-386b73257e43" />





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


<img width="577" height="333" alt="image" src="https://github.com/user-attachments/assets/76c3b188-c047-4c18-a6d8-cb6e5e7f885f" />


Press "s" to select whole die then press "v" to center the view 

Point the cursor to a cell then press "s" to select it, zoom into it by pressing "z" 

The IO pins are placed in a random equidistant mode as seen below based on the 
configuration (FP_IO_MODE = 1) set in openlane/configuration/floorplan.tcl


<img width="593" height="400" alt="image" src="https://github.com/user-attachments/assets/cf6040ea-d785-40c4-86aa-a5c331feacce" />


The components in the layout can be identified by using the "what" command in tkcon 
window after selecting it.


<img width="534" height="294" alt="image" src="https://github.com/user-attachments/assets/6147a94f-cb45-4f7b-81c7-17e3b9438338" />

Standard cells are not placed but can be viewed at the bottom left corner of the layout


# Library Binding and Placement 

# Netlist binding and initial place design 
1. Bind netlist with physical cells 
Bind the netlist to physical cells with real dimensions. The physical cells come from a library 
that contains cells which can have different dimensions, various shapes of the cells, and delay 
information. Bigger cells have lesser resistance while the functionality is the same. This means 
that the library has many flavors of cells.

3. Placement:


<img width="695" height="309" alt="image" src="https://github.com/user-attachments/assets/60e8b41f-536d-4768-ad19-58bd743cf92d" />



Placement is done based on connectivity. For example, FF1 is close to Din1 pin and FF2 close 
to Dout1 pin and combinational cells placed nearer to FF1 and FF2. This is to reduce delay.


<img width="687" height="223" alt="image" src="https://github.com/user-attachments/assets/3b25a072-3d2a-4311-8f65-a049e8314839" />

Optimize placement using estimated wire-length and capacitance 

This is the stage where we estimate wirelength and capacitance (C=EA/d) and insert repeaters based 
on that. If the wirelength is more, then to maintain signal integrity, we add repeaters to reduce 
resistance. Repeaters basically reconditions the original signal and transfers.


<img width="691" height="421" alt="image" src="https://github.com/user-attachments/assets/9f436459-9e57-4952-bfb2-b916e68a7e0d" />



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


<img width="700" height="352" alt="image" src="https://github.com/user-attachments/assets/911fbdcd-0cf7-44d0-a3d9-9ce9576df989" />



# Cell design and characterization flows 

All standards cells (AND, OR, BUFFER, INVERTER, flip-flops etc.) are present in standard cell library. 
The cells inside the library are of different flavors (different drive strengths, functionality, threshold 
voltage). If the cell size is more, then the drive strength is high to drive longer wires. If the threshold 
voltage is high, then it will take more time to switch than the one with lesser threshold voltage. 


<img width="699" height="435" alt="image" src="https://github.com/user-attachments/assets/f2a09c4d-b2e7-4d1a-a757-09a7b902e6d8" />


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



<img width="611" height="581" alt="image" src="https://github.com/user-attachments/assets/04eafb91-7218-47df-afd6-47bcac58592c" />



Timing characterization 
Syntax and semantics of power.lib, timing.lib and noise.lib. These are necessary to understand the 
GUNA software workflow. 
We are taking inverters connected back to back as an example.


<img width="677" height="214" alt="image" src="https://github.com/user-attachments/assets/cf8d42ed-8faa-48c0-9877-f4e51e0b7821" />


<img width="592" height="321" alt="image" src="https://github.com/user-attachments/assets/204f2a62-a3b8-4488-88d3-bdeba2a4e8fd" />


Timing thershold definitions: 


<img width="463" height="360" alt="image" src="https://github.com/user-attachments/assets/468c6eeb-eb53-42ce-99d7-0608bf182a4b" />

Two inverters in series, red is output of first inverter and blue is output of second inverter:


<img width="660" height="401" alt="image" src="https://github.com/user-attachments/assets/c49b2dde-64f1-42ca-8d08-2ccb1225f4e9" />


The red is input waveform and blue is output waveform of the buffer. The left side is rise delay and 
right side is fall delay. 
PROPOGATION DELAY= time(out_*_thr)-time(in_*_) 
TRANSITION DELAY=time(slew_high_*_thr)-time(slew_low_*_thr) 
Negative propagation delay is not expected. This means that the output comes before the input so 
it's important to choose correct threshold point to produce positive delay. Delay threshold is usually 
50% and slew rate threshold is usually 20%-80%.


<img width="677" height="365" alt="image" src="https://github.com/user-attachments/assets/072364d7-8007-4d17-80fd-ddb7176f466e" />


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



<img width="669" height="427" alt="image" src="https://github.com/user-attachments/assets/56a381e9-8acd-4f0d-ba18-49d3fe767464" />





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


<img width="689" height="356" alt="image" src="https://github.com/user-attachments/assets/9dd9f678-f6a0-4922-bb93-12a3680dd9ba" />



SPICE deck netlist description: 

• Syntax for the PMOS and NMOS: [component name] [drain] [gate] [source] [substrate] 
[transistor type] W=[width] L=[length] 
• All components are described based on nodes and its values 
• .op is the start of SPICE simulation operation where Vin will be sweep from 0 to 2.5 with 
0.05V steps 
• tsmc_025um_model.mod is the model file containing the technological parameters for the 
0.25um NMOS and PMOS


<img width="686" height="324" alt="image" src="https://github.com/user-attachments/assets/25fc565c-acf8-4beb-9a55-2c0afe093668" />



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


<img width="621" height="394" alt="image" src="https://github.com/user-attachments/assets/b16348d9-14f1-4a23-ba78-7fad52e71c24" />


Switching Threshold Vm 


<img width="654" height="393" alt="image" src="https://github.com/user-attachments/assets/62e8991b-2434-40c1-99f6-c835a0bd2717" />


1. The shapes are almost the same which means that CMOS is a robust device. 
2. Parameters that defines the robustness of CMOS 
o switching threshold, Vm. It is the point where the Vin = Vout and both PMOS & 
NMOS are in saturation region. These will be turned on and there is high chances for 
leakage. There is a high possibility that the current flows directly from VDD to GND. 
Due to this, short circuit kind of device is seen.


<img width="626" height="420" alt="image" src="https://github.com/user-attachments/assets/f3f64d6c-54b1-4cbf-95c4-c47e0fe70efc" />


• Propagation delay: rise or fall delay

Static and dynamic simulation of CMOS inverter 

DC transfer analysis is used for finding switching threshold. Simulation is DC sweep from 0V to 2.5V 
with 0.05V steps: 
When a pulse is applied to the CMOS, transient analysis is used to find propagation delay.


<img width="676" height="409" alt="image" src="https://github.com/user-attachments/assets/e7cb10f4-7186-4311-9b32-501a5df26837" />




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


<img width="699" height="351" alt="image" src="https://github.com/user-attachments/assets/f7de82ee-dae3-4141-bc0f-6dbc57492f17" />

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


<img width="695" height="337" alt="image" src="https://github.com/user-attachments/assets/dbc0a0b4-5b76-461f-863d-2ea67024eb4f" />


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


<img width="475" height="294" alt="image" src="https://github.com/user-attachments/assets/827178ab-b965-4372-b455-7ec4254b778c" />


9. Higher level metal formation 
o CMP (Chemical Mechanical Polishing) technique to planarize the surface 
o Create contact holes using photolithograhy process 
o Mask 12 is for first contact hole 
o Mask 13 is for first Aluminum contact layer 
o Mask 14 is for second contact hole 
o Mask 15 is for second Aluminum contact layer 
o Mask 16 is for making contact to topmost layer

# Lab introduction to Sky130 basic layers layout and LEF using inverter

<img width="772" height="476" alt="image" src="https://github.com/user-attachments/assets/fcf0d307-8e5a-4d39-8be3-b52b27351d54" />

In sky130A, the first layer is local-interconnect layer or local-i and then the m1, m2 and so on. Power 
and Ground lines are in m1. When polysilicon crosses ndiffusion the it is NMOS and if polysilicon 
crosses pdiffusion then it is PMOS is created. The output of the layout is the LEF file. It is used by the 
router in APR to get the location of standard cell pins to route them properly. So it is basically the 
abstract form of layout of a standard cell. 
Commands in tkcon window for spice extraction of the custom inverter layout: 
1. extract all 
2. ext2spice cthresh 0 rthresh 0 --> this extracts the parasitic information 
3. ext2spice

Sky130 Tech File Labs
1. Lab steps to create final SPICE deck using Sky130 tech 
The default SPICE deck file using Sky130 is as seen in the previous section. Now we modify 
the file to plot a transient response. The final SPICE deck file is as below.


Command to load spice file for simulation in ngspice: 
ngspice sky130A_inv.spice 
Generate a graph using: 
plot y vs time a
2. Lab steps to characterize inverter using sky130 model files
<img width="776" height="398" alt="image" src="https://github.com/user-attachments/assets/0b0f33f2-e5cf-4895-80e1-4d329724d82f" />
Using the above transient plot, we will now characterize the slew rate and propagation delay: 
Maximum voltage = 3.3V 80% of maximum voltage = 2.64V 20% of maximum voltage = 
0.64V 50% of maximum voltage = 1.65V 
o Rise Transition (output transition time from 20% to 80%): 
▪ Tr_r = 2.20278ns - 2.15946ns = 0.04332ns 
image
o Fall Transition (output transition time from 80% to 20%): 
▪ Tr_f = 4.06818ns - 4.04073ns = 0.02745ns 
image
o Rise Delay (delay between 50% of input and 50% of output) that is time taken for 
output to rise to 50% and time taken for input to fall to 50%: 
▪ D_r = 2.18381ns - 2.15003ns = 0.03378ns
o Fall Delay (delay between 50% of input and 50% of output) that is time taken for 
output to fall to 50% and time taken for input to rise to 50%: 
▪ D_f = 4.05402ns - 4.0501ns = 0.00392ns

3. Lab introduction to Sky130 pdk's and steps to download labs 
Commands to download and view the corrupted skywater process magic tech file and other 
files to perform drc corrections: 
o Command to download the lab files: wget 
http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz 
o Extract it: tar xfz drc_tests.tgz 
o Change directory into the lab folder: cd drc/drc_tests 
o List all files: ls -al 
o Command to open magic tool: magic -d XR

4. Lab introduction to Magic and steps to load Sky130 tech-rules 
Useful websites: 
Magic Technology File Format Manual - This site explains about tech files. All technology 
specific information comes from a technology file. This file includes information as layer 
types, electrical connectivity, design rules, rules for mask generation, rules for extracting 
netlists etc. 
Rules for SkyWater SKY130 PDK 
Steps: 
o Open magic with met3.mag as input

<img width="487" height="263" alt="image" src="https://github.com/user-attachments/assets/e74d8692-3160-4a0d-93e3-f8c48799cc5b" />

o In this view, we see a number of independent layouts containing some DRC errors 


5. Lab exercise to fix poly.9 error in Sky130 tech-file
   In tkcon window: load poly
   


o Let's look at rule poly.9 As described in Rules for SkyWater SKY130 PDK, Poly resistor 
spacing to poly or spacing (no overlap) to diff/tap should be atleast 0.48um.
<img width="565" height="461" alt="image" src="https://github.com/user-attachments/assets/03131778-2507-4973-82ed-40b23197fafe" />
That's not the case here, so we have to fix the tech file to include this DRC.

o Open sky130A.tech file in drc_tests directory. The included rules for poly.9 are only 
for the spacing between the n-poly resistor with n-diffusion and the spacing between 
the p-poly resistor with diffusion. We will now add new rules for the spacing between 
the poly resistor with poly non-resistor. Highlighted in green below are the two newly 
added rules. First one is the rule for the spacing between the p-poly resistor with poly 
non-resistor and the next one is the rule for spacing between n-poly resistor with 
poly non-resistor. The allpolynonres is a macro under alias section of techfile.

<img width="628" height="207" alt="image" src="https://github.com/user-attachments/assets/20d06a1d-bfd7-4610-8e99-23d5fabdc7c6" />

<img width="580" height="313" alt="image" src="https://github.com/user-attachments/assets/4d63ff50-db72-472d-b593-4fe33e659176" />
o In tkcon window: tech load sky130A.tech to check drc in tkcon window: drc check 
The new DRC rules will now take effect.

<img width="628" height="498" alt="image" src="https://github.com/user-attachments/assets/0e9a3557-e29e-4b27-ad15-c972af6227f3" />

6. Lab exercise to implement poly resistor spacing to diff and tap 
To fix what is hown in below pic, modify the tech file to include not only the spacing between 
npolyres with N-substrate diffusion in poly.9 but also between npolyres and all types of 
diffusion.

Pre-layout timing analysis and importance of good clock tree

Lab steps to convert grid info to track info


sky130_inv.mag contains all information like PG information, port information, logic etc. OpenLANE is 
a PnR tool and a PnR tool does not require all the information present in .mag file. The only 
information that we'll be needing is the boundary, power and ground rails, and the inputs & outputs. 
This is the reason of using .lef files. So the objective is to extract the LEF file from Magic file and plug 
into picorv32a design. 
From PnR point of view, there are few guidelines to be followed while making standard cell, 
• The input and output ports lies at the intersection of the horizontal and vertical tracks 
(ensure the routes can reach that ports). 
• The width of the standard cell must be odd multiple of the tracks horizontal pitch and height 
must be odd multiples of tracks vertical pitch 
Tracks refer to the horizontal and vertical metal layers on which routing occurs. The grid formed by 
the intersection of horizontal and vertical tracks creates a routing grid, also known as a routing 
matrix. The 
~/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/openlane/sky130_fd_sc_hd/trac
ks.info contains track information. 
Before changing grid:

<img width="778" height="379" alt="image" src="https://github.com/user-attachments/assets/8fcf2450-8298-41a5-a61b-5ffb95310abc" />

After changing grid values: 

<img width="768" height="246" alt="image" src="https://github.com/user-attachments/assets/dc9ae7bc-bb8d-4d00-a92c-9c9a732a1afa" />

Second requirement is satisfied in below picture. 

<img width="789" height="353" alt="image" src="https://github.com/user-attachments/assets/89361025-7746-44ed-b895-5e5b30e8d04a" />

Lab steps to convert magic layout to std cell LEF 

LEF (Library Exchange Format) file is a standard file format used to describe the physical layout and 
characteristics of standard cell libraries or macro libraries. LEF files contain detailed information 
about the geometric shapes, sizes, layers, and other physical properties of individual cells or macros 
within the library. The instructions to set the port definitions are in this site 
Next, save the .mag file with a new filename. In the tcon terminal: lef write  
It will generate a LEF file with the new filename. 

Introduction to timing libs and steps to include new cell in synthesis 

Inside pdks/sky130A/libs.ref/sky130_fd_sc_hd/lib/ are the liberty timing files for SKY130 PDK which 
contains the timing and power parameters for each cell needed in STA. It can either be slow, typical, 
fast with different supply voltages (1v80, 1v65, 1v95). These are called PVT corners. The library name 
sky130_fd_sc_hd__ss_025C_1v80 describes the PVT corner as slow-slow (delay is maximum), 25° 
Celsius temperature, at 1.8V power supply. Timing and power parameter of a cell is obtained by 
simulating the cell in a variety of operating conditions (different corners) and these data are 
represented in the liberty file. The liberty file characterizes all cells and is used during ABC mapping 
during synthesis stage which maps the generic cells to the actual standard cells available in the 
liberty file.

1. Copy the extracted lef file sky130_vsdinv.lef and the liberty files sky130*.lib from 
/openlane/vsdstdcelldesign/libs to the src directory of picorv32a.

2.Add the folowing to config.tcl inside the picorv32a: 
<img width="774" height="110" alt="image" src="https://github.com/user-attachments/assets/2a5bdbf7-b1a0-42a2-baa4-137e62847b8c" />

This sets the liberty file that will be used for ABC mapping of synthesis (LIB_SYNTH) and for 
STA (_FASTEST,_SLOWEST,_TYPICAL) and also the extra LEF files (EXTRA_LEFS) for the 
customized inverter cell.

3. Run docker and prepare the design picorv32a. Plug the new lef file to the OpenLANE flow. 
docker 
./flow.tcl -interactive 
package require openlane 0.9 
prep -design picorv32a 
set lefs [glob $::env(DESIGN_DIR)/src/*.lef] 
add_lefs -src $lefs

4. Next run_synthesis. sky130_vsdinv cell is successfully included in the design
   
<img width="775" height="237" alt="image" src="https://github.com/user-attachments/assets/1d880afd-7ad3-49dd-809e-895bf22d5728" />

<img width="648" height="129" alt="image" src="https://github.com/user-attachments/assets/7245b8c6-797a-4b3f-817a-4b499fa32665" />

Delay tables 

Whenever the enable pin is 1, only then the CLK will propogate to Y in case of AND gate and 
whenever the enable pin is 0, only then the CLK will propogate to Y in case of OR gate, as shown 
below. When the enable is 1, the CLK will not propagate and there won't be any short circuit power 
consumption and switching power consumption when such elements are used in clock tree. This 
method is referred to as the clock gating technique. 

Consider the below clock tree structure. 
<img width="767" height="222" alt="image" src="https://github.com/user-attachments/assets/7f1a8f10-7317-49e0-8afa-dd5def7b2f89" />

Buffers on different levels have different capacitive loads and buffer sizes but as long as they have 
the same loads and sizes in the same level, the total delay for each clock tree path will be the same 
thus skew will remain zero. Practically, different levels can have varying input transition and output 
capacitive load and hence varying delay. 
Delay tables are used to capture the timing model of each cell and is included inside the liberty file. 
The main factor in delay is the output slew. The output slew depends on capacitive load and input 
slew. The input slew is a function of previous stage buffer's output capacitive load and input slew 
and has its own transition delay table. 

<img width="779" height="377" alt="image" src="https://github.com/user-attachments/assets/183e4515-6dee-4494-9bc6-bacd726d5b2b" />

At level 2, both the buffers have identical delays with same transition times, load capacitances, and 
buffer sizes. Consequently, the skew is maintained at 0.If this is not the case, then the skew will be 
negative leading to timing violations. While these considerations may seem insignificant when 
analyzing the delay of just two buffers, their significance is high in designs featuring millions of cells. 
Failing to adhere to these guidelines during clock tree creation can lead to numerous timing-related 
complications. 
Terminologies: 
• CTS is the process of designing a clock distribution network to minimize skew and ensure 
synchronous operation of the circuit 
• Skew refers to the variation in clock signal arrival times 
• Latency is the delay experienced by the clock signal 
• Slew rate is the rate of change of the signal's voltage over time 

Lab steps to configure synthesis settings to fix slack 

Currently, tns = -711.59 wns = -23.89 Chip area for module picorv32a = 147712.9184 
Next step is to see if synthesis can be more timing-driven.

1. Check synthesis strategy and other timing related variables and modify accordingly 
SYNTH_STRATEGY of delay 0 means the tool will focus more on optimizing the delay, index 
can be 0, 1, 2, or 3 where 3 is the most optimized for timing at the cost of area. 
SYNTH_BUFFERING of 1 ensures buffer will be used on high fanout cells to reduce wire delay. 
SYNTH_SIZING of 1 will enable cell sizing where cell will be upsized or downsized as needed 
to meet timing. SYNTH_DRIVING_CELL is the cell used to drive the input ports and is vital for 
cells with a lot of fan-outs since it needs higher drive strength.


2. Run synthesis again and it is seen that area is increased but there is no negative slack 
tns = 0 wns = 0 Chip area for module picorv32a = 209181.872




3. Run floorplan and placement 
If any error comes related to macro placement, temporary solution is to comment 
basic_macro_placement inside the OpenLane/scripts/tcl_commands/floorplan.tcl (this is okay 
since we are not adding any macro to the design).

init_floorplan 
place_io 
global_placement_or 
detailed_placement 
tap_decap_or 
detailed_placement 

After successful run, runs/[date]/results/placement/picorv32a.placement.def will be created.


<img width="769" height="465" alt="image" src="https://github.com/user-attachments/assets/b79d087f-d30b-4b9e-acdc-1bccd8c0327a" />

Search for instance of cell sky130_vsdinv inside the DEF file after placement stage: cat 
picorv32a.placement.def | grep sky130_vsdinv 
Select a single sky130_vsdinv cell instance from the list dumped by grep (e.g. 41096). On 
tkcon, command % select cell 41096 then ctrl+z to zoom into that cell. As shown below, our 
customized inverter cell sky130_myinverter is sucessfully placed. Use expand on tkon to show 
the footprint of the cell and notice how the power and ground of sky130_vsdinv overlaps the 
power and ground pins of its adjacent cells.


<img width="781" height="246" alt="image" src="https://github.com/user-attachments/assets/09f4ef68-dccf-4dce-85c4-037a0704fddc" />


<img width="780" height="420" alt="image" src="https://github.com/user-attachments/assets/d911cd14-c4e6-4465-bc30-27d0433988e9" />


<img width="775" height="334" alt="image" src="https://github.com/user-attachments/assets/1e928c78-fcbd-4121-80a6-269aa85da2a9" />

# Timing analysis with ideal clocks using openSTA 

Setup timing analysis and introduction to flip-flop setup time

Consider an ideal clock where clock tree is not built and perform timing analysis to understand the 
parameters. Later the same can be done using real clocks. Specifications are as mentioned in the 
picture. Clock frequncy (F) is 1GHz and clock period (T) is 1ns.


<img width="622" height="433" alt="image" src="https://github.com/user-attachments/assets/7c2d5330-5b7e-4bdf-b3e8-9913e855a2a2" />



<img width="771" height="311" alt="image" src="https://github.com/user-attachments/assets/91b1dc04-22e2-4074-9f62-a4bfeaf22599" />

Setup timing analysis equation is: 
Θ < T - S 
Θ = Combinational delay which includes clk to Q delay of launch flop and internal propagation delay 
of all gates between launch and capture flop 
T = Time period, also called the required time 
S = Setup time. As demonstrated below, signal must settle on the middle (input of Mux 2) before 
clock tansists to 1 so the delay due to Mux 1 must be considered, this delay is the setup time.


Introduction to clock jitter and uncertainty

Clock is beign created by PLL (Phase Locked Loop). So, this clock source is expected to send clock 
signal at 0, T, 2T etc. Even these clock sources might or might not be able to provide a clock exactly 
at Tns because of its own in-built variation. That is called as the jitter. Jitter can be manifested as 
short-term fluctuations in the timing of signal transitions, resulting in deviations from the expected 
clock or data timing.


<img width="781" height="431" alt="image" src="https://github.com/user-attachments/assets/ded3846b-46c8-4e40-8170-f1de34035ef2" />


<img width="780" height="141" alt="image" src="https://github.com/user-attachments/assets/736e3950-87b6-4ca2-b63e-e00636932120" />

So, a more realistic equation for setup time is, 
Θ < T - S - SU 
SU = Setup uncertainty due to jitter which is temporary variation of clock period. This is due to non
idealities of PLL/clock source.


<img width="771" height="502" alt="image" src="https://github.com/user-attachments/assets/7612cb55-e0b2-4f50-b088-cfa5dc086f0c" />

# Clock Tree Synthesis TritonCTS and signal integrity 

Clock tree routing and buffering using H-Tree algorithm 

Consider the clock port that goes to the flip-flops highlighted in the picture. The purpose is to 
connect the port to the clock pins of the flip-flops based on the connectivity information. If we 
blindly connect as shown in the picture below, then t2>t1 and the difference t2-t1 is nothing but 
the skew. Clock skew refers to the variation in arrival times of the clock signal at different points 
within a synchronous digital system. In simpler terms, it is the difference in propagation delay 
experienced by the clock signal as it travels along different paths within the system. Clock skew can 
occur due to various factors such as differences in wire lengths, variations in signal routing paths, 
variations in buffer delays, and other physical and environmental factors. These variations can lead to 
some parts of the system receiving the clock signal earlier or later than others. Minimizing clock skew 
is essential to ensure proper synchronization of signals and reliable operation of the digital circuit. 
Ideally, the skew should be zero.


<img width="779" height="378" alt="image" src="https://github.com/user-attachments/assets/5c675630-6510-4957-9b51-4091305bd6c3" />


<img width="771" height="425" alt="image" src="https://github.com/user-attachments/assets/45d800b4-29d9-4d56-9dd8-e6f663ec4695" />

In the above scenario, the skew is not less/zero, so it is a bad tree. 
H-Tree is the solution. It analyses the clock route by calculating the distance from the source to all 
the endpoints and deciding on a midpoint to start building tree from that point. In this case, the 
clock reaches at all the endpoints at almost the same time.


<img width="777" height="478" alt="image" src="https://github.com/user-attachments/assets/94f09b5a-e5be-4e47-a753-046294597a97" />

We expect that whatever input is provided, that should be reproduced at the output. However, due 
to the inherent resistance and capacitance in physical wires, the signal may experience attenuation or 
distortion, hindering its proper transmission to the output. To address this, repeaters or buffers are 
inserted along the path to ensure signal integrity and reliable transmission.

The key difference between repeaters used in clock paths and those used in data paths lies in their 
rise and fall times. Clock buffers have same rise and fall times, ensuring uniform signal propagation 
throughout the clock distribution network. In contrast, data buffers exhibit varying rise and fall times, 
which may differ based on the characteristics of the data being transmitted and the components 
involved in processing it.

Crosstalk and clock net shielding 

Clock nets are critical nets in the design because clock tree is built is such a fashion that the skew is 
zero. There is a phenomenon called crosstalk where a signal transmitted on one channel 
unintentionally interacts with or interferes with signals on adjacent channels leading to distortion, 
noise, timing errors etc. If this happens on clock routes, then the clock tree structure will be 
deteriorated. So all the clock nets are shielded. By shielding, the clock nets are protected. If there is a 
wire adjacent to such shields, then there exists a huge coupling capacitance cauign two issues. One is 
glitch and the other is delta delay. 

Whenever there is a switching activity happening on the aggressor, the coupling capacitance is so 
strong that it directly affects the net sitting close to it called the victim net. the victim net is without 
any shielding. As a result, there is a dip in the voltage, resulting in glitch.


<img width="778" height="429" alt="image" src="https://github.com/user-attachments/assets/5c0cef51-bf39-4a1e-8a0f-a488917d8d91" />

Shielding basically protects the victim nets by breaking the coupling capacitance between the 
aggressor and the victim. These shielding nets are either Vdd or Vss. The shields do not switch, so 
the victim will not switch.


<img width="778" height="451" alt="image" src="https://github.com/user-attachments/assets/e1c930df-c1ec-4955-b177-28974d62e574" />

Lab steps to run and verify CTS using TritonCTS 

After ECO of cell sizing, currently the timing is as follows. 
image
The slack might increase or decrease as we move forward in the PnR flow. For OpenLANE to use the 
current netlist, 
image
write_verilog filename overwrites the current verilog file in the specified location. 
Then, 
run_floorplan 
run_placement 
Then run cts using the command run_cts. Before that we need to check the default setting s that 
CTS uses. 
image
In CTS stage, clock buffers get added.

OpenLANE takes the procs 
from ~/Desktop/work/tools/openlane_working_dir/openlane/scripts/tcl_commands. 
These procedures will then call OpenROAD to run the actual tool.

For example, run_cts can be found in the file /OpenLane/scripts/tcl_commands/cts.tcl, this 
tcl procedure will call OpenROAD and will call /OpenLane/scripts/openroad/cts.tcl which 
contains the OpenROAD commands to run TritonCTS. 
Inside the /OpenLane/scripts/openroad/cts.tcl contains the configuration variables for CTS 
such as: 
CTS_CLK_BUFFER_LIST = list of clock buffers used in clock tree branches (sky130_fd_sc_hd__clkbuf_1 
sky130_fd_sc_hd__clkbuf_2 sky130_fd_sc_hd__clkbuf_4 sky130_fd_sc_hd__clkbuf_8) 
CTS_ROOT_BUFFER = clock buffer used for the root of the clock tree and is the biggest clock buffer 
to drive the clock tree of the whole chip (sky130_fd_sc_hd__clkbuf_16) 
CTS_MAX_CAP = maximum capacitance of the output port of the root clock buffer

Timing analysis with real clocks using openSTA 

Setup timing analysis using real clocks 
Now the clock tree is built and timing analysis is done on real clocks. 


<img width="773" height="338" alt="image" src="https://github.com/user-attachments/assets/79af1415-0c61-47cd-9b8c-1d8dd2aefb71" />


delta1 = launch flop clock network delay delta2 = capture flop clock delay 
delta2=capture flop clock delay


<img width="779" height="374" alt="image" src="https://github.com/user-attachments/assets/a5dcbcde-fbb6-488f-81da-ee082b339f73" />

Any design satisfying Slack = Data required time - Data arrival time is ready to work in 
the given frequency. If this equation is violated , then slack will become negative. We expect slack to 
be 0 or positive.

Hold timing analysis using real clocks 

Hold analysis refers to the delay/time required by the MUX2 model within the flip-flop to transfer 
data outside. It denotes the duration during which the launch flop must retain data before it reaches 
the capture flop. Unlike setup analysis, which spans two rising clock edges, hold analysis occurs on 
the same rising clock edge for both the launch and capture flops. A hold violation occurs when the 
path is too fast, impacted by factors including combinational delay, clock buffer delays, and hold 
time. Notably, parameters such as time period and setup uncertainty hold no significance, as both 
launch and capture flops receive identical rising clock edges during hold analysis.


<img width="782" height="373" alt="image" src="https://github.com/user-attachments/assets/dad55ce1-4393-4528-97c9-bfa9ba71bd9d" />


<img width="775" height="400" alt="image" src="https://github.com/user-attachments/assets/e6ae2dd3-3d01-423d-9c00-635feae89e78" />

Skew = Launch Clock Network Delay - Capture Clock Network Delay 

Lab steps to analyze timing with real clocks using OpenSTA 

The objective is to analyse the clock tree. Entering into openroad instead of invoking a separate 
OpenSTA tool. In openroad, timing analysis is done in a different way, where a db is created from lef 
& def and used. 

1. To create the db, read lef
   

<img width="767" height="133" alt="image" src="https://github.com/user-attachments/assets/a7ad0ee9-782a-4251-9b6f-9f9c4a9dbff6" />

2. Read def from cts stage


<img width="762" height="214" alt="image" src="https://github.com/user-attachments/assets/5105d1fa-6c2f-4f9d-9c5f-ff668897d9ef" />

3. Create db


<img width="771" height="241" alt="image" src="https://github.com/user-attachments/assets/96959330-370b-4f31-a456-b977c7ac3c85" />

4. Read the db, verilog file, libraries, sdc


<img width="748" height="242" alt="image" src="https://github.com/user-attachments/assets/d9305e2b-06d1-4ced-a2a1-45fe8aa15d1f" />

5.Check timing 


<img width="775" height="558" alt="image" src="https://github.com/user-attachments/assets/108d49e2-8d4e-4257-812e-41f54c73d5ab" />



<img width="776" height="766" alt="image" src="https://github.com/user-attachments/assets/99c55bb8-5181-4902-b9b4-5da7b368c85d" />

Lab steps to execute OpenSTA with right timing libraries 

TritonCTS is built to optimise based on one corner but the libraries that are included in the previous 
section for timing analysis are min and max corners. This kind of analysis is not accurate. So, exit and 
re-enter openroad and check timing only for typical corner. 

 
In this typical scenario, slack is met in both setup and hold analysis. 


<img width="772" height="281" alt="image" src="https://github.com/user-attachments/assets/b08515f5-c875-4905-82cc-2a2429bdda78" />


<img width="772" height="301" alt="image" src="https://github.com/user-attachments/assets/7b070a5a-2f5d-4fa4-9454-d58b712221d3" />

When CTS is built, skew values is tried to be met by inserting buffers from the CTS_CLK_BUFFER_LIST. 
We can also modify this list based on requirements. 
When TritonCTS is building the clock tree, it tries to use each buffer listed 
in $::env(CTS_CLK_BUFFER_LIST) (sky130_fd_sc_hd__clkbuf_1 
sky130_fd_sc_hd__clkbuf_2 sky130_fd_sc_hd__clkbuf_4 
sky130_fd_sc_hd__clkbuf_8) from smallest to largest until the target skew is met. Target skew is 
stored in $::env(CTS_TARGET_SKEW). The STA result shows that sky130_fd_sc_hd__clkbuf_1 is the 
mostly used buffer, we can also change the $::env(CTS_CLK_BUFFER_LIST) to use other buffers 
and observe the effect on STA and area. 
Use tcl lreplace command to modify $::env(CTS_CLK_BUFFER_LIST) 
image
The $::env(CURRENT_DEF) used by CTS is the DEF file of the previously run CTS, but the DEF file 
we want for CTS is the placement's DEF file. So change the $::env(CURRENT_DEF) to point to 
placement DEF file then run_cts. 
Observe the resulting post-CTS STA compared to previous run since we modified the clock buffer. 
Only buf_2 clock buffer is used now compared to buf_1 used in previous run. The WNS is better now 
since we used bigger clock buffers.

Final steps for RTL2GDS using tritonRoute and openSTA 

Routing and design rule check (DRC) 

Introduction to Maze Routing 
Routing is to find the best possible connection/route between two points. There are many routing 
algorithms like Steiner Tree algorithm, Line Search algorithm etc. and one such is Maze Routing - 
Lee's Algorithm (Lee 1961) 
Consider and example of connecting two points 1 & 2. Point 1 will act as a source and 2 will act as a 
target. The requirement is to find the best possible path or the shortest possible path to connect 1 & 
2 will less or no zig-zag routes. Mostly the routes are L-shaped. From algorithmic point of view, the 
software has to search and connect the two points. From physical designer point of view, it is a 
physical path/wire establishment for signals to travel between components.

Lee's maze routing algorithm, is a popular pathfinding algorithm used in maze routing, which is a 
type of routing problem where the goal is to find a path from a source to a destination in a maze
like grid. The Lee algorithm is particularly well-suited for routing on grids or mesh-based structures 
in integrated circuit design. 
Algorithm steps: 
1. Initialization: The algorithm starts by initializing a routing grid or matrix representing the 
maze. Each cell in the grid can be one of several states: obstacle, empty, source, destination, 
or visited. The source cell is marked with a value of 0, indicating that it is the starting point.


<img width="439" height="282" alt="image" src="https://github.com/user-attachments/assets/400e66e8-c00e-4ec7-8924-cd6e8cf966f1" />

2. Wave Expansion: The algorithm performs a wave expansion from the source cell, spreading 
outwards in all directions. At each step, the algorithm examines neighboring cells (up, down, 
left, and right) and assigns them a value one greater than the minimum value of their 
neighboring cells (excluding obstacles). This process continues until the destination cell is 
reached or until no more cells can be visited.


<img width="437" height="367" alt="image" src="https://github.com/user-attachments/assets/7f0b6fdf-2d78-4c4b-8476-4bf102e501e1" />

3. Backtracking and Path Reconstruction: Once the destination cell is reached, the algorithm 
traces back the path from the destination to the source by following the values in each cell. 
This results in the shortest path from the source to the destination. There might be multiple 
paths but the best path that the tool will choose is one with less bends. The route should not 
be diagonal and must not overlap any blockage/obstruction such as macros or HIPs.


<img width="432" height="358" alt="image" src="https://github.com/user-attachments/assets/91bf7586-892e-4fc4-8c76-895b7fdd82ac" />

Design Rule Check 

When routing, it's not merely about connecting two points; we must also adhere to specific rules. 
These rules, for example, mention that when constructing two wires, there must be a minimum 
spacing or distance between them, minimum wire width, minimum wire pitch etc. Hence, DRC 
cleaning is done to ensure the=at the routes can be fabricated and printed in silicon faithfully. 
image
Signal short is also one of the critical issues as it causes functionality failure. It can be eliminated by 
moving the route to next layer with vias. This can lead to more DRCs (via width, via spacing, higher 
metal layer must be wider than lower metal layer etc.).

<img width="772" height="483" alt="image" src="https://github.com/user-attachments/assets/86245737-ffc9-436a-9f8d-fddb92dff112" />


<img width="777" height="390" alt="image" src="https://github.com/user-attachments/assets/4c5fb4a7-3ba3-4fd9-a6e8-56daa24b1466" />


Power Distribution Network and routing 
Lab steps to build power distribution network 
1. Go to openlane directory 
2. docker 
3. ./flow.tcl -interactive 
4. package require openlane 0.9 
5. prep -design picorv32a -tag 19-03_16-40 (this is the folder till cts has been done) 
6. echo $::env(CURRENT_DEF) /openLANE_flow/designs/picorv32a/runs/19-03_16
40/results/cts/picorv32a.cts.def 
7. To generate PDN: gen_pdn


Lab steps from power straps to std cell power    

The power and ground rails have a pitch of 2.72um and hence the reason reason why the custom 
inverter cell has a height of 2.72um, else the power and ground rails will not be able to power the 
cell. Looking at the LEF file runs/[date]/tmp/merged.lef, it is noticed that all cells are of height 
2.72um and only width differs. 
As shown below, power/ground pads -> power/ground ring-> power/ground straps -> 
power/ground rails to power up the standard cells. 


<img width="773" height="371" alt="image" src="https://github.com/user-attachments/assets/0b1092d6-9ec6-40e6-baf3-163c23c340d3" />

Basics of global and detail routing and configure TritonRoute 

TritonRoute is the engine that is used for routing. run_routing command does routing in 
OpenLANE. 


<img width="783" height="324" alt="image" src="https://github.com/user-attachments/assets/49c0ab97-7aa3-4210-a22a-b388f7f30c6f" />


<img width="776" height="281" alt="image" src="https://github.com/user-attachments/assets/caf18197-67ff-4d65-925f-f9f80f1a37e2" />

In the VLSI flow, the routing stage is highly critical and can be executed using either open-source or 
commercial tools. This stage is divided into two phases: 
1. Global Route / Fast Route: 
o This is accomplished using fast routing techniques where the area to be routed is 
partitioned into tiles or rectangles. Global routing establishes the initial framework 
for routing paths. 
2. Detail Route: 
o This phase involves meticulous tracking routing techniques to complete the routing 
process. Detailed routing fine-tunes and finalizes the paths to ensure proper 
connectivity and compliance with design constraints.

TritonRoute features 

TritonRoute feature 1 - Honors pre-processed route guides: 
M1 preferred direction is vertical and M2 preferred direction is horizontal. Whenever the tool 
encounters a non preferred direction route, then it divides the route into unit width. This is called 
splitting. The divided unit width sections that fall in the same line of preferred direction routes are 
merged. The edges which are parallel to the preferred routing direction are bridged with the upper 
layer, process caled as bridging. Non preferred routing guides are now converted into preferred 
routing guides of M2.


<img width="777" height="484" alt="image" src="https://github.com/user-attachments/assets/4ac749d3-c7eb-44af-a4cb-ddda03eaea8d" />

TritonRoute feature 2 - Inter-guide connectivity: 
M1 and M2 are connected at the purple colour areas. The tool will understand that there is overlap 
area, then it will add via to connect M1 & M2.


<img width="769" height="379" alt="image" src="https://github.com/user-attachments/assets/01388bf0-d5fa-49c3-a83c-67c85032f0b4" />

TritonRoute feature 3 - intra- & inter-layer routing: 
The preferred direction of the M1 layer is vertical, resulting in lines oriented vertically. The dashed 
lines are referred to as panels, with each routing guide assigned to a specific panel. When routing 
occurs within even-index panels, it's termed as intra-layer parallel panel routing. Initially, routing 
takes place simultaneously in all even-index panels, followed by routing in odd-index panels. This 
routing remains confined within a particular layer. Routing progresses from lower to upper layers, 
ensuring the orderly flow of routing operations.


<img width="775" height="383" alt="image" src="https://github.com/user-attachments/assets/b57b2bfc-f24d-456f-8edf-cb97a4235b58" />

TritonRoute method to handle connectivity 


<img width="772" height="212" alt="image" src="https://github.com/user-attachments/assets/1426c5ef-9870-4a2a-bdaa-0e09c8213f44" />


<img width="769" height="360" alt="image" src="https://github.com/user-attachments/assets/b38c3289-1323-4894-8556-92bef433a2e6" />

The Goal of MILP (Mixed Integer Linear Programming) algorithm is to find the optimal solution to 
connect two Access point cluster.


<img width="771" height="472" alt="image" src="https://github.com/user-attachments/assets/a9921dca-24cb-4804-8b8e-e4b2bc7e1dc5" />

In the above algorithm, for each access point, cost is found. Then, a minimum spanning tree between 
access points and cost. So, the algorithm says that minimal and most optimal point is nedded 
between two APCs.

Final files list post-route 

With run_routing command, routing got completed. Both global routing (fast routing) and detail 
routing are done. It takes multiple iterations to bring down the DRC violations to 0. routing strategy 
was set to 0. In the intial iteration, the violation count was close to 25000 and at the 34th iteration, 
the violations got resolved and became 0. The entire routing operation took nearly 25 minutes. 


<img width="773" height="471" alt="image" src="https://github.com/user-attachments/assets/c9222495-de94-43d5-81e2-d4f325c48138" />

A DEF file will be formed in runs/[date]/results/routing/picorv32.def. Open the DEF file of 
routing stage in Magic.


<img width="779" height="458" alt="image" src="https://github.com/user-attachments/assets/377da648-e002-4ef4-9551-f7d7ab6f9dbb" />

Parasitic extraction: 
OpenLane does not have any spef extraction tool, so we use a separate tool present in work/tools/ 
directory. 
1. Go to /home/vsduser/Desktop/work/tools 
2. Inside that there is a folder named SPEF_EXTRACTOR 
3. SPEF_EXTRACTOR contains a list of files, out of which there is a python file called main.py. It 
helps to generate the SPEF provided there are lef & def files 
4. To create SPEF file python3 main.py 
/home/vsduser/work/tools/openlane_working_dir/openlane/designs/picorv32
a/runs/26-03_05-49/tmp/merged.lef 
/home/vsduser/work/tools/openlane_working_dir/openlane/designs/picorv32
a/runs/26-03_05-49/tmp/routing/picorv32a.def 
5. spef will be saved in the same location as def 
file. /home/vsduser/work/tools/openlane_working_dir/openlane/designs/picor
v32a/runs/26-03_05-49/tmp/routing 
image
The last stage will be to extract the GDSII file ready for fabrication run_magic 
This uses Magic to stream the GDSII file runs/26-03_05-49/results/magic/picorv32a.gds. 
This GDSII file can then be read by Magic: 
image
The PnR flow is done



















































   

   
   








































   


















