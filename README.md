# LVDS-Driver-Design-for-High-Speed-Application
This repository presents the design of LVDS Driver for High Speed Application. It is implemented on Synopsys Custom Compiler in 28nm technology node.<br/>
# Table Of Content <br/>
* [Abstract](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#abstract-)<br/>
* [LVDS Application Block diagram](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#lvds-application-block-diagram)<br/>
* [Tool used](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#tool-used)<br/>

# Abstract <br/>
LVDS i.e. Low Voltage Differential Signaling is the interface used for high speed data transfer over transmission media such as coaxial cable or over PCB traces. It basically comprised of switched current sources which drives the transmission lines with differential signals. Salient features of this interface are low power operation, Noise rejection capability and reliable clock recovery at the receiver. This Driver circuit operates at 5V/3.3V of supply voltage. It consists of switched current sources and common mode feedback (CMFB) circuit to stabilize the output common mode voltage level. The design is implemented using Synopsys tool using 28 nm technology node. It also helps to reduce the no. of ports in multiport operation as multiport parallel data can be multiplexed, serialized and transmitted over a cable with LVDS Driver.<br/>

# LVDS Application Block diagram <br/>
<img width="592" alt="Block Dig" src="https://user-images.githubusercontent.com/88900482/156181453-21946fee-9b2e-4dda-aa0b-55ee094b5067.PNG">

Serializer is a Mixed Block which uses LVDS Driver. It's Block diagram is shown above. It consists of PISO digital Block which will convert parallel data from multiple inputs to the serial bit stream as D_in and Dbar_in. These two are 180 degree out of phase with each other. These opposite serial bit streams are then given to the LVDS driver. LVDS Driver will convert these signals into low voltage differential signals as Vo+ and Vo-. 

## Advantages of Differential Signalling
<img width="759" alt="Diff_signalling" src="https://user-images.githubusercontent.com/88900482/156188112-05d1e8a0-d7af-4891-a0ab-a052dc7c646e.PNG">

Differential Signals when passed over the transmission line, noise will be added in both the signals in same phase. So when differential output voltage is taken i.e. Vout = Vo+ - Vo- , it will be noise free. Thus Diffrential signalling has noise rejection capability. 

# Tool used<br/>
*Synopsys Custom Compiler*:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.<br/>
*Synopsys Primewave*:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.<br/>
*Synopsys 28nm PDK*:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above circuit design.<br/>



# Netlist<br/>
You can view the circuit netlists [here](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/blob/main/LVDS_netlist.spi)<br/>
# Author<br/>
Mrs. Madhuri Kadam, ME in Electronic and Telecommunication Engineering at Sardat Patel Institute of Technology, Mumbai <br/>
# Acknowledgements <br/>
[Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)<br/>
[Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)<br/>
[Synopsys India](https://www.synopsys.com/)<br/>
# Reference <br/>
[1]  Hari Shanker Gupta, RM Parmar and R K Dave, “High Speed LVDS     Driver for SERDES ,” IEEE Conference Proc., July 2009.
[2]   G. A. Graceffa, U. Gatti, C. Calligaro, “A 400 Mbps Radiation Hardened By Design LVDS Compliant Driver and Receiver,” IEEE Conference Proc., July 2016. 
http://www.ijeert.org/pdf/v2-i6/25.pdf <br/>
