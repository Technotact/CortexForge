# CortexForge
Distributed Runtime Infrastructure for Cortex-M Compute (64 node Hardware Cluster)  

Hardware Cluster : 32× NXP FRDM-MCXN236 + 32× NXP FRDM-MCXA153  

This project is under development.  
Estimated duration of this project is 6 ~ 8 months starting October, 2026.  
All Hardware MCU's have been procured.  
NUC needs to be procured along with some other accessories.  

Current Status : Hardware is being assembled along with some 3d printed server racks.  

What this looks like from the hardware side->  
1. Both the MCXN 236 board and the MCXA 153 board has dual USB board, where one facilitates a MCU-Link(on Board) and the other one facilitates a USB CDC port in direct communiucation with the MCU.   
2. Idea is to connect all the 64 MCU's individually via the MCU Link to the Asus/Intel NUC via USB. This might look crazy but is likely possible.  
3. Another Idea is to divide this in group's of 16 forming a total of 4 groups. This group clusters will be primarily administered by something like a Beagly AI or some similar SBC and in turn this will be connected to the ASUS/Intel NUC.  
4. From the USB-CDC port side, the idea is to interconnect all of the 64 devices over a bus over a virtual address type thing via this port, with a dynamic master to slave concept or peer to peer communication based on some scheduler with a primary external controller that will be connected to the NUC or the SBC's talked about, but there are chances this would not work out. In that case we need to figure out on interconnecting them.  

Future integrations from the Hardware perspective->  
1. Integration of Saleae Logic Analysers and Power profilers to a dedicated pins but since they will be more in number, through the idea of signal multiplexers without corruption. This would completely work out since i have built a somolar system previously.  
2. This would in turn provide HIL Testbeds for almost every applications.  

What the final goal look's like  
1. Honestly the end goal of this project is not know to me.  
2. This project was inspired from the Kubernetes style of nodes in distributed systems.  
3. Likely there will be Zephyr Integration or something similar very soon once the hardware is fully live to administer the system.  
4. Plans are ther to use LVGL or some other graphics library.  

