# LVDS-Driver-Design-for-High-Speed-Application
This repository presents the design of LVDS Driver for High Speed Application. It is implemented on Synopsys Custom Compiler in 28nm technology node.<br/>
# Table Of Content <br/>
* [Abstract](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#abstract-)<br/>
* [LVDS Application Block diagram](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#lvds-application-block-diagram)<br/>
* [Tool used](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#tool-used)<br/>
* [LVDS Driver Circuit Simulation and Waveforms in Synopsys Custom Compiler](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#lvds-driver-circuit-simulation-and-waveforms-in-synopsys-custome-compiler)<br/>
* [Netlist and Primesim Log](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#netlist-and-primesim-log)<br/>
* [Future Scope](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#future-scope)<br/>
* [Authoured By](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#authoured-by)<br/>
* [Acknowledgements](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#acknowledgements)<br/>
* [References](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#references)<br/>
# Abstract <br/>
LVDS i.e. Low Voltage Differential Signaling is the interface used for high speed data transfer over transmission media such as coaxial cable or over PCB traces. It basically comprised of switched current sources which drives the transmission lines with differential signals. Salient features of this interface are low power operation, Noise rejection capability and reliable clock recovery at the receiver. This Driver circuit operates at 5V/3.3V of supply voltage. It consists of switched current sources and common mode feedback (CMFB) circuit to stabilize the output common mode voltage level. The design is implemented using Synopsys tool using 28 nm technology node. It also helps to reduce the no. of ports in multiport operation as multiport parallel data can be multiplexed, serialized and transmitted over a cable with LVDS Driver.<br/>

# LVDS Application Block diagram <br/>
<img width="592" alt="Block Dig" src="https://user-images.githubusercontent.com/88900482/156181453-21946fee-9b2e-4dda-aa0b-55ee094b5067.PNG">

Serializer is a Mixed Block which uses LVDS Driver. It's Block diagram is shown above. It consists of PISO digital Block which will convert parallel data from multiple inputs to the serial bit stream as D_in and Dbar_in. These two are 180 degree out of phase with each other. These opposite serial bit streams are then given to the LVDS driver. LVDS Driver will convert these signals into low voltage differential signals as Vo+ and Vo-. 

## Advantages of Differential Signalling
<img width="759" alt="Diff_signalling" src="https://user-images.githubusercontent.com/88900482/156188112-05d1e8a0-d7af-4891-a0ab-a052dc7c646e.PNG">

Differential Signals when passed over the transmission line, noise will be added in both the signals in same phase. So when differential output voltage is taken i.e. Vout = Vo+ - Vo- , it will be noise free. Thus Diffrential signalling has noise rejection capability. 

## LVDS Driver Vlotage levels and Timing Diagram
<img width="764" alt="vlg_timing_wf" src="https://user-images.githubusercontent.com/88900482/156192010-b04212ee-aec7-4587-b7a0-d169070e4c3c.PNG">

Above diagram shows a typical LVDS signal voltage and timing diagram, where output common mode voltage level is 1.2V and Vodiff = Vo+ - Vo- = 350mV

# Tool used<br/>
*Synopsys Custom Compiler*:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.<br/>
*Synopsys Primewave*:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.<br/>
*Synopsys 28nm PDK*:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above circuit design.<br/>

# LVDS Driver Circuit Simulation and Waveforms in Synopsys Custom Compiler
## LVDS Driver Schematic
![Lvds_schematic](https://user-images.githubusercontent.com/88900482/156196568-b9438feb-731f-4d61-bf11-17b1f5ee8c91.PNG)

![Shematic2](https://user-images.githubusercontent.com/88900482/156196642-685d7f9c-6c82-4a18-b57a-9edcec9e194b.PNG)

## LVDS Driver Symbol
![LVDS_symbol](https://user-images.githubusercontent.com/88900482/156196799-1e33f85d-640d-4fe4-a395-5870557f59ad.PNG)

![sybol2](https://user-images.githubusercontent.com/88900482/156196835-071843da-1da1-4dfb-bbac-23113692b8ed.PNG)

## LVDS Driver Symbol Testbench
![symbol-tb](https://user-images.githubusercontent.com/88900482/156197209-969c7a3e-e336-4650-8035-62ef3aad7548.PNG)

## LVDS Driver Transient Analysis at 20Mbps Data Rate, Vdd=1.8V and CL=1pF
![Waveforms-full](https://user-images.githubusercontent.com/88900482/156197973-15a0cff5-23cd-40c9-8ffd-1c3f1e50061e.PNG)

![Waveforms](https://user-images.githubusercontent.com/88900482/156198073-47398322-ba98-4fc5-8949-05044dfe2d78.PNG)

![wave-ungroup](https://user-images.githubusercontent.com/88900482/156198116-85ff412c-318b-4c8e-84fb-6e412d3f317b.PNG)

## LVDS Driver Transient Analysis at 20Mbps Data Rate, Vdd=1.2V and CL=0.1pF
<img width="958" alt="Wave-0 1pf" src="https://user-images.githubusercontent.com/88900482/156198304-c27c667d-2511-428b-99e5-271e8d3965a3.PNG">

<img width="949" alt="ungr-0 1pf" src="https://user-images.githubusercontent.com/88900482/156198326-a4ba0037-0987-481d-bfdc-62601ea38c87.PNG">

# Netlist and Primesim Log <br/>
You can view the circuit netlists [here](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/blob/main/LVDS_netlist.spi)<br/>
You can view the Primesim log [here](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/blob/main/LVDS_netlist.spi)<br/>

# Future Scope
LVDS Driver circuit can be redesigned and optimised to get Voap-p = 400 mV which is presently getting as 700 mV.  

# Authoured By <br/>
Mrs. Madhuri Kadam, ME in Electronics and Telecommunication Engineering, Mumbai <br/>
Assistant Professor, Shree L. R. Tiwari College of Engineering, Mira Rd

# Acknowledgements <br/>
[1. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)<br/>
[2. Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)<br/>
[3. Synopsys India](https://www.synopsys.com/)<br/>

# References <br/>
[1]  Hari Shanker Gupta, RM Parmar and R K Dave, “High Speed LVDS     Driver for SERDES ,” IEEE Conference Proc., July 2009.

[2]   G. A. Graceffa, U. Gatti, C. Calligaro, “A 400 Mbps Radiation Hardened By Design LVDS Compliant Driver and Receiver,” IEEE Conference Proc., July 2016. 

