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
- Conclusion
- Author
- Acknowledgements
- References

 ## Abstract
Static CMOS logic based CLA adders are most common and widely used adder topology due to its high robustness and driving power. However, using complementary pair of N-channel CMOS (NMOS) and P-channel CMOS (PMOS) makes the number of transistors in circuit high. This high number of transistors accounts for high input impedance for signals. As a result, delay increases due to increased RC time  constant. However, an improvement can be achieved by utilizing a combination of static CMOS logic with other logic techniques. The propose design uses a  Pass Transistor Logic of AND and XOR Gates. In order to validate the performance of the proposed CLA circuit, verification has been done by conduction simulation using Synopsys Custom Compiler. The proposed design helps in decreasing the dealay and the tranistor count also decreases with in the design.

## Detailed Explanation with Reference circuit details
![image](https://user-images.githubusercontent.com/100534193/156115970-3bf837e2-0bdc-41d6-aa33-54bfb50d0964.png)

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


      
