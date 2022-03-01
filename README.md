# LVDS-Driver-Design-for-High-Speed-Application
This repository presents the design of LVDS Driver for High Speed Application. It is implemented on Synopsys Custom Compiler in 28nm technology node.<br/>
# Table Of Content <br/>
* [Abstract](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#abstract-)<br/>
* [Detailed Explanation with reference Block diagram](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#detailed-explanation-with-reference-block-diagram)<br/>
* [Tool used](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/edit/main/README.md#tool-used)<br/>

# Abstract <br/>
LVDS i.e. Low Voltage Differential Signaling is the interface used for high speed data transfer over transmission media such as coaxial cable or over PCB traces. It basically comprised of switched current sources which drives the transmission lines with differential signals. Salient features of this interface are low power operation, Noise rejection capability and reliable clock recovery at the receiver. This Driver circuit operates at 5V/3.3V of supply voltage. It consists of switched current sources and common mode feedback (CMFB) circuit to stabilize the output common mode voltage level. The design is implemented using Synopsys tool using 28 nm technology node. It also helps to reduce the no. of ports in multiport operation as multiport parallel data can be multiplexed, serialized and transmitted over a cable with LVDS Driver.<br/>
# Detailed Explanation with reference block diagram<br/>
this is 
# Tool used<br/>
*Synopsys Custom Compiler*:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.<br/>
*Synopsys Primewave*:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.<br/>
*Synopsys 28nm PDK*:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above circuit design.<br/>



# Netlist<br/>
You can view the circuit netlists [here](https://github.com/MadhuriKadam9/LVDS-Driver-Design-for-High-Speed-Application/tree/main/Netlist)<br/>
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
