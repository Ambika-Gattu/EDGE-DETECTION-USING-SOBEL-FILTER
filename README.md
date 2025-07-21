# EDGE-DETECTION-USING-SOBEL-FILTER
This project implements a real-time edge detection system using the Sobel filter, fully developed in Verilog HDL and deployed on a Xilinx Zynq-7000 SoC evaluation board. It enables high-speed image preprocessing with minimal latency through pipelined, parallel architecture and is cross-verified using MATLAB simulations.
<br>
<br>
Why Only the Sobel Filter?<br>
The Sobel filter is specifically chosen for its balance between edge sensitivity, noise suppression, and computational simplicity. Compared to other filters (like Prewitt or Roberts):<br>
Sobel incorporates a smoothing effect, reducing sensitivity to image noise<br>
It offers stronger gradient magnitude, especially for vertical and horizontal edges<br>
The integer-only kernel structure allows efficient hardware implementation<br>
It provides good localization and detection accuracy for real-time use-cases<br>
Ideal for FPGA, where resource utilization and speed are critical<br>
The Sobel filter is thus an optimal trade-off between precision and real-time feasibility, making it ideal for hardware-accelerated vision systems.<br>

Project Objectives:<br>
Implement the Sobel filter in Verilog HDL<br>
Deploy and validate on Zynq-7000 FPGA board<br>
Achieve real-time, low-latency processing with efficient resource use<br>
Validate results using MATLAB for correctness<br>
Optimize for timing, power, and performance in embedded vision applications<br>

Hardware Platform:<br>
Target Board: Xilinx Zynq-7000 SoC<br>
This board features a dual-core ARM Cortex-A9 processor alongside programmable logic (PL), allowing:<br>
Deployment of the Sobel filter in PL for real-time acceleration<br>
Integration potential with ARM-side applications (e.g., camera interfacing, data transfer)<br>
AXI-stream support for clean module interfacing<br>
High I/O bandwidth and flexible memory interfaces<br>

Tools & Technologies<br>
Verilog HDL<br>
Xilinx Vivado Design Suite (synthesis, implementation, simulation)<br>
MATLAB – for reference simulation and result comparison<br>
Zynq-7000 SoC FPGA <br>
Optional:Vivado Simulator (for waveform analysis)<br>

MATLAB Validation<br>
To verify the correctness of the hardware implementation, the same edge detection operations were carried out in MATLAB. This ensures that the FPGA output aligns with the expected filter behavior.<br>
Input images are preprocessed in MATLAB<br>
Output edges are compared against the hardware-generated results<br>
Pixel-by-pixel comparison used for accuracy evaluation<br>

FPGA Implementation Summary<br>
Metric               Result<br>
LUT Utilization      ~5%<br>
Flip-Flops (FF)      ~1%<br>
DSP/BRAM Usage       ~1%<br>
IO Usage             ~8%<br>
Timing Violations    None<br>
Power Consumption    ~21W (99% dynamic)<br>

Conclusion<br>
The Sobel filter was selected and implemented on FPGA due to its accuracy, noise robustness, and hardware-friendly design. This Verilog-based edge detection system performs well under resource constraints while maintaining high responsiveness. The Zynq-7000 SoC platform enables future integration with ARM-side applications for complete embedded vision pipelines.<br>
This design is suitable for deployment in robotics, medical imaging, surveillance, and autonomous systems requiring low-latency, hardware-level image preprocessing.<br>
