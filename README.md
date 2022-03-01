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
Static CMOS logic based CLA adders are most common and widely used adder topology due to its high robustness and driving power. However, using complementary pair of N-channel CMOS (NMOS) and P-channel CMOS (PMOS) makes the number of transistors in circuit high. This high number of transistors accounts for high input impedance for signals. As a result, delay increases due to increased RC time  constant. However, an improvement can be achieved by utilizing a combination of static CMOS logic with other logic techniques. The propose design uses a  Pass Transistor Logic of AND and XOR Gates. In order to validate the performance of the proposed CLA circuit, verification has been done by conduction simulation using Synopsys Custom Compiler. The proposed design helps in decreasing the dealay and the tranistor coynt also decreases with in the design
      
