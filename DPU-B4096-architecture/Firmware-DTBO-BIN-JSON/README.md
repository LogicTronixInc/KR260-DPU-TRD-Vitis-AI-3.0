# KR260 DPU TRD- Ready to use Firmware Files
**We have provided the ready to run/load fimrware files for B4096-DPU-TRD for KR260**
The provided firmware files are:
1. kr260-dpu-trd-b4096.bin - BIN file obtained from VIVADO Bitstream generation step. 
2. kr260-dpu-trd-b4096.dtbo - compiled device tree file.
3. pl.dtsi - Device tree generated from XSA. This file is not needed to copy to KR260, it is just for reference.
4. shell.json - json file. 

**You have to copy BIN, DTBO and JSON into KR260 board's /lib/firmware/xilinx/kr260-dou-trd-b4096 directory and then load it by xmutil loadapp command**

** Here is again the detail Hackster.io Tutorial:** https://www.hackster.io/LogicTronix/kria-kr260-dpu-trd-vivado-flow-vitis-ai-3-0-tutorial-0085fd



# Boot Log from KR260 board
We also have provided the boot log here , this boot log can be compared while running the resnet50 applicaiton on KR260 after loading the firmware.\
BOOT LOG :  [kr260-dpu-trd-vitis-ai-3.0-B4096-Resnet50-bootlog.log](https://github.com/LogicTronixInc/KR260-DPU-TRD-Vitis-AI-3.0/blob/master/DPU-B4096-architecture/Firmware-DTBO-BIN-JSON/kr260-dpu-trd-vitis-ai-3.0-B4096-Resnet50-bootlog.log) 

\
For any questions or queries, please write us at: info@logictronix.com

### LogicTronix is AMD-Xilinx Design Service Partner for FPGA Design & ML Acceleration! 

**Note: This repo does not mean to include production grade resources or files (only good for test and explore) , so for any real world solution and production grade deployment plan contact us!**

