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
|----> PL.DTSI \
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
|----> PL.DTSI \
|----> Boot LOG from KR260 \
| \
|\
|--Images

**Note: for running above firmware file the petalinux BSP project have to be build with above XSA and DPU driver needs to have enabled as mentioned at Hackster.io tutorial above!**

## How to run Resnet50 on above linked Petalinux Boot Image?
In the liked boot image there is also "resnet50 application" included while building image. You can follow these steps for runnign the resnet50 application.
```
xilinx-kr260-starterkit-20222:~# ls
app
xilinx-kr260-starterkit-20222:~# cd app/
xilinx-kr260-starterkit-20222:~/app# ls
img  model  samples
xilinx-kr260-starterkit-20222:~/app# 
xilinx-kr260-starterkit-20222:~/app# 
xilinx-kr260-starterkit-20222:~/app# cp model/resnet50.xmodel .
xilinx-kr260-starterkit-20222:~/app# ls
img  model  resnet50.xmodel  samples
xilinx-kr260-starterkit-20222:~/app# 
xilinx-kr260-starterkit-20222:~/app# 
xilinx-kr260-starterkit-20222:~/app# env LD_LIBRARY_PATH=samples/lib samples/bin/resnet50 img/bellpeppe-994958.JPEG
score[945]  =  0.992235     text: bell pepper,
score[941]  =  0.00315807   text: acorn squash,
score[943]  =  0.00191546   text: cucumber, cuke,
score[939]  =  0.000904801  text: zucchini, courgette,
score[949]  =  0.00054879   text: strawberry,
xilinx-kr260-starterkit-20222:~#
```

## VIVADO DPU-TRD Block design:
![KR260-DPU-TRD](https://github.com/LogicTronixInc/KR260-DPU-TRD-Vitis-AI-3.0/blob/master/Images/KR260-DPU-TRD-Hackster-LogicTronix.png) 

\
For any questions or queries, please write us at: info@logictronix.com

### LogicTronix is AMD-Xilinx Design Service Partner for FPGA Design & ML Acceleration! 

**Note: This repo does not mean to include production grade resources or files (only good for test and explore) , so for any real world solution and production grade deployment plan contact us!**

