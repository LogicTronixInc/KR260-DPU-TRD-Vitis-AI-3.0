# Overview of Machine Learning in Kria Robotics Kit, KR260
**For running any Machine Learning model or examples in AMD-Xilinx MPSoC or Versal Platforms/boards, we have to create a "DPU-TRD" or DPU design in VIVADO or Vitis , create the Bootable OS in Petalinux , boot it on board and load the machine learning model and app for running!**

***This Git repo includes the resources for "DPU TRD or how to create DPU design for running ML in Kria KR260 board" and run the basic Resnet50 example on the board. We can run any Vitis AI model zoo examples in the KR260 after following this git repo or hacskter tutorial.***

# KR260-DPU-TRD-Vitis-AI-3.0
This is also resource file repository of KR260-DPU-TRD-Vitis-AI-3.0 Vivado flow detail tutorial at Hackster.io! \
**Hackster.io Tutorial:** https://www.hackster.io/LogicTronix/kria-kr260-dpu-trd-vivado-flow-vitis-ai-3-0-tutorial-0085fd

## Tools required for following above hackster.io tutorial
1. VIVADO/Vitis 2022.2 
2. Petalinux 2022.2 

## Download the Boot image for KR260 and Run ML demo:
**Do you want to download and directly run the ML demo in KR260 board without folowing above hackster.io tutorial? If you want to run the B4096 (larger DPU architecture) or B512 (smaller DPU) firmware based DPU example in your KR260 then you can download following SD image, burn it on SD card, boot it on KR260 and then copy the B4096 or B512 firmware.** 
\
The SD image is created in Petalinux 2022.2 so update the kria boot firmware accordingly by following Kria-SoMs-Wiki page!
**SD Image Link:** [KR260-DPU-TRD-2022.2 (Vitis AI 3.0) SD Image](https://drive.google.com/file/d/1tRdoWkcW5G6yxVE_5qjON5FfCq9IKS6E/view?usp=sharing)


## Repository Hierarchy

|--**DPU-B512-architecture** \
| \
|--- **VIVADO-Design**\
|---> VIVADO-Tcl-file\
|---> VIVADO-Block-Design-PDF\
|---> VIVADO-XSA-File\
| \
|---**Firmware-DTBO-BIN-JSON** \
|----> DTBO \
|----> BIN \
|----> JSON \
|----> Boot LOG from KR260 \
| \
| \
|--**DPU-B4096-architecture**\
| \
|--- **VIVADO-Design** \
|---> VIVADO-Tcl-file \
|---> VIVADO-Block-Design-PDF \
|---> VIVADO-XSA-File \
| \
|---**Firmware-DTBO-BIN-JSON** \
|----> DTBO \
|----> BIN \
|----> JSON \
|----> Boot LOG from KR260 \
| \
|\
|--Images

**Note: for running above firmware file the petalinux BSP project have to be build with above XSA and DPU driver needs to have enabled as mentioned at Hackster.io tutorial above!**

## VIVADO DPU-TRD Block design:
![KR260-DPU-TRD](https://github.com/LogicTronixInc/KR260-DPU-TRD-Vitis-AI-3.0/blob/master/Images/KR260-DPU-TRD-Hackster-LogicTronix.png) 

\
For any questions or queries, please write us at: info@logictronix.com

### LogicTronix is AMD-Xilinx Design Service Partner for FPGA Design & ML Acceleration! 

**Note: This repo is not mean to include production grade resource , so for any real world solution and production grade contact us!**

