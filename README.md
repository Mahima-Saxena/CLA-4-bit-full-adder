# 4-Bit Static CMOS CLA Using Modified Circuits for Carry Propagate and Generate Terms
This repository presents the design of 4-bit CLA adder. Performance improvement of 4-bit CLA adder has been done by using AND and XOR of pass tarnsistor logic for generating carry propagate and carry generate terms . Design is implemented using Synopsis Custom Compiler on 28nm CMOS Technology.

 ## Table of Contents
- Abstarct
- Detailed Explanation with Reference circuit details
- Tool used
- Inverter
- AND and XOR implementation using pass transistor logic
- 4 bit Carry Look Ahead Adder
- Simulation Results
- Parameters calculated for 4 bit improved CLA
- Conclusion
- Author
- Acknowledgements
- References

 ## Abstract
Static CMOS logic based CLA adders are most common and widely used adder topology due to its high robustness and driving power. However, using complementary pair of N-channel CMOS (NMOS) and P-channel CMOS (PMOS) makes the number of transistors in circuit high. This high number of transistors accounts for high input impedance for signals. As a result, delay increases due to increased RC time  constant. However, an improvement can be achieved by utilizing a combination of static CMOS logic with other logic techniques. The propose design uses a  Pass Transistor Logic of AND and XOR Gates. In order to validate the performance of the proposed CLA circuit, verification has been done by conducting simulation using Synopsys Custom Compiler. The proposed design helps in decreasing the dealay and the tranistor count also decreases with in the design.

## Detailed Explanation with Reference circuit details
![adder_design](https://user-images.githubusercontent.com/100534193/156117492-64a3e9c8-d17d-4cb9-a584-3664cb83e580.png)

Conventional execution of CLA adder uses carry-generate (Gi) and carry-propagate terms (Pi). If the input bits are denoted as Ai and Bi, then Gi and Pi terms can be expressed as the following equations. 
Pi = Ai ⊕ Bi                                   (1)

Gi = Ai . Bi                                    (2)

Carry-out bits for CLA adder can be written in general as:
𝐶𝑖+1=𝐺𝑖+𝑃𝑖𝐶𝑖                                     (3)

Using equation (1), (2) and (3), carry-out equations for 4-bit CLA can be written as:

𝐶1=𝐺0+𝑃0𝐶0                                      (4)

𝐶2=𝐺1+𝑃1𝐶1= 𝐺1+𝑃1𝐺0+𝑃1𝑃0𝐶0                     (5)

𝐶3=𝐺2+𝑃2𝐶2= 𝐺2+𝑃2𝐺1+𝑃2𝑃1𝐺0+𝑃2𝑃1𝑃0𝐶0           (6)

𝐶4=𝐺3+𝑃3𝐶3=𝐺3+𝑃3𝐺2+𝑃3𝑃2𝐺1+𝑃3𝑃2𝑃1𝐺0+𝑃3𝑃2𝑃1𝑃0𝐶0 (7)

## Tools Used
- Synopsys Custom Compiler:  The Synopsys Custom Compiler design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.

- Synopsys Primewave:  PrimeWave Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

- Synopsys 28nm PDK:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

## Inverter
### Iverter Schematic
![not](https://user-images.githubusercontent.com/100534193/156118454-6998aad1-c245-4f46-a396-d2c9bb561720.png)

### Inverter Symbol
![not_symbol](https://user-images.githubusercontent.com/100534193/156118522-b3bdd11f-9a24-487d-8a98-b7428ae09ec0.png)

## AND Implemantaion using PTL
### AND Schematic
![image](https://user-images.githubusercontent.com/100534193/156124333-a6265fc3-ede1-47e2-bffd-8247b754d560.png)

### AND Symbol
![image](https://user-images.githubusercontent.com/100534193/156118907-8ad9b2ba-078b-46ae-83f4-d652c74a34e1.png)

## XOR implemantation using PTL
### XOR schematic
![image](https://user-images.githubusercontent.com/100534193/156124300-14d6f677-02ae-4384-b1cf-fce6a9cc834b.png)


### XOR Symbol
![image](https://user-images.githubusercontent.com/100534193/156119201-9fdfb233-018f-42e2-81ff-640fa1f8332d.png)

## 4 Bit CLA using PTL logic AND  and XOR Gates
### Schematic
![new](https://user-images.githubusercontent.com/100534193/156119550-f305849b-a863-4589-a6eb-efc3856ab90f.png)

## Simulation result
![waveform_ptl](https://user-images.githubusercontent.com/100534193/156119964-616f29a0-1ef9-4bd7-a1d7-b91abefe6377.png)


##  Parameters calculated for 4 bit improved CLA
- Propogation Delay
  Propagation delay of a logic gate is defined as the time it takes for the effect of change in input to be visible at the output. In other words, propagation delay is the time   required for the input to be propagated to the output. 
- Area 
  Area is calculated by the number of transistor present in the circuit.
- Average Power Dissipation 
  Power dissipation can be defined as the product of total current supplied to the circuit and the total voltage loss .
  
  |Propogation Delay(ns) | No of Transistors | Avg Power(uW) |
  |----------------------|-------------------|---------------|
  | 6.5                  |90                 |5.9            |
  
  
## Conclusion
The repository presents the design and simulation of 4 bit CLA adder on 28nm technology node of Synopsys. A improved version of CLA  design adopted was successfully done and 4 bit binary addition was verified from output waveforms.Since number of tranistors used are 90. Area gets reduce to large extent by using PTL logic for AND and XOR gates when compared with conventional static CMOS.All the Analysis is verified on 28nm technology node.

## Author
-  Mahima Saxena, BTech Electronics and commuincations, ABESEC, Ghaziabad, Uttar Pradesh.

## Acknowledgements
- Cloud Based Analog IC Design Hackathon
- Synopsys India
- Kunal Ghosh, Co-founder, VSD Corp. Pvt Ltd.
- Chinmay panda, IIT Hyderabad
- Sameer Durgoji, NIT Karnataka

## References
- Hossain, Muhammad Saddam; Arifin, Farhadur (2020). [IEEE 2020 Advanced Computing and Communication Technologies for High Performance Applications (ACCTHPA) - Cochin, India (2020.7.2-2020.7.4)] - A Proposed Design of Conventional 4-Bit Carry Look-Ahead Adder Improving Performance.
- Mehedi Hasan1, Moumita Sadia Islam, Muhtasim Rafid Ahmed “Performance Improvement of 4-Bit Static CMOSCarryLook-Ahead Adder Using Modified Circuits for CarryPropagate and Generate Terms” ISSN: 2326-9065.



      
