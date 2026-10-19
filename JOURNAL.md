---
title: "6 Axis Robot Arm"
author: "Joshua Rambiya"
description: "Robot arm that uses 3 stepper motors for the base joints and 3 BLDCs with FOC for the wrist joints."
created_at: "2026-10-10"
---

# October 11: Wrist Complete

I'm working from the end effector down, so starting with the wrist. I finished the differential mechanism on the wrist and the pulleys for channeling the string into the differential mechanism
Tomorrow I'm going to try to finish at least the first arm link. I'll also print out the initial versions of the wrist mechanism.

<img width="1160" height="760" alt="image" src="https://github.com/user-attachments/assets/a5a5beb4-c2a2-4ef6-a270-5db7dc4dc6f0" />

**Total time spent: 2 hours 40 minutes**


# October 12: First link done & wrist built

Built the wrist. Had a few issues with tolerances but not an extraordinary amount. While designing the wrist, I originally planned to have the first arm link attach on the inside of the wrist assembly,
but after printing it I realized that the holes were too close to the top of the assembly, so it would limit the mechanisms rotation. I want each DOF to have at least 180 degrees of rotation 
so I just designed the first link to be on the outside instead.

<img width="1216" height="804" alt="image" src="https://github.com/user-attachments/assets/ac566e7d-dc4a-486f-b13d-f85c10c6c2f1" />


**Total time spent: 1 hour 59 minutes**

# October 13: First and Second links completely CADed

Figured out how the rigging works for the wrist actuation. For the rolling contact joint that I'm using for the elbow, I'm having a bit of trouble mating it correctly in the CAD so its a little bit off, but its okay. I'm going to start printing the parts soon, but I still need to design a spot for the encoders. Also I still need to CAD the base of the entire thing. The base will house all of the stepper motors for the elbow and base joints. Also I did the calculations for the elbow and base torques and I will need approximately 1.7Nm for the base and 0.9Nm for the elbow. This is a high end estimate since the CAD I'm assuming is lighter than the real thing (also I may have gotten the math wrong who knows, so better safe than sorry) Since the stepper motors I'm using have 42Ncm (0.42Nm) of torque I'm going to have a 4:1 ratio on the base and a 2:1 ratio on the elbow joint.

<img width="1216" height="804" alt="image" src="https://github.com/user-attachments/assets/c1d3ac3e-1216-40a9-b753-ec6528b5ea6d" />
<img width="1920" height="1574" alt="image" src="https://github.com/user-attachments/assets/0670b0aa-80cf-454f-9db4-30263ef488f2" />

I also added the channels for the capstan mechanism for the base joint.

<img width="1312" height="942" alt="image" src="https://github.com/user-attachments/assets/23a7c9c1-8137-46e3-93a0-063a01d26e0f" />


**Total time spent: 3 hours 43 minutes**


# October 16: Built first and second link

I forgot to devlog for the past 2 days, but I still worked on the project, I finished the entire CAD and tested to make sure the encoder geometry worked because I have had issues with the magnet not sensing in the past. It works great though. I printed out all the parts and am about halfway done with assembly. I think its possible to get this wrapped up in the next 2 days assuming I have little to know issues. The two sliders on the first link are binding a bit though so I might need to redesign that. I also have to do the rigging and I am not looking forward to that.

<img width="1920" height="1440" alt="image" src="https://github.com/user-attachments/assets/12fd5f37-781a-4d36-b8f3-92c417e051b5" />
<img width="1842" height="870" alt="image" src="https://github.com/user-attachments/assets/0e3afcb9-1e0c-4843-87c6-eefb5f20cf74" />

**Total time spent: 7 hours 11 minutes**


# October 17: Rigging

This thing is genuine ragebait. I spend the past hour trying to flip a pulley around and then two of the wrist degrees of freedom don't work because I didn't spool in enough string. I know what I need to do tomorrow though, I basically will have to redo the entire rigging. Its going to be a long day.

<img width="1500" height="2000" alt="image" src="https://github.com/user-attachments/assets/797b353b-3b3a-46b0-93a2-4eacf36271c0" />

**Total time spent: 5 hours 12 minutes**

# October 18: Hardware Done

I have become too familiar with the smell of superglue. I had to redo basically all of the rigging I did yesterday, making sure this time to add string onto the spools. That took way too long already but that was only half the battle. Then I had to attach it to the base, a process that included 4 more strings to rig. That process was a lot smoother though, and everything actually looks really good.
The bevel gears on the wrist and the rolling contact joint rigging sometimes slip, so I might have to put a dab of superglue on those. The rigging on the turret slips to the point of the turret not working, so I'm going to have to redo that entire rigging, but its only one string so it shouldn't be too bad. 
I tested the stepper motors and the wires that came with them for some reason have the phases out of order which is weird, maybe it was meant for something else non Arduino related. I'm going to have to cut those and solder them though. I tested with some other wires that I knew did work. However, my calculations used the stall torque of the motors which was really dumb on my end I don't know how I missed that but oh well. Surprisingly, the joints still mostly work, its only that it stalls out when its fully extended and the base tries to go up, but that's easily solvable in code, and I'm almost never going to have to fully extend anyway. 

<img width="1440" height="1920" alt="image" src="https://github.com/user-attachments/assets/26e2bdc8-e927-43ab-8e9b-47c3af25376b" />

https://github.com/user-attachments/assets/15947638-a03b-4767-99b3-7de28c2206a6

**Total time spent: 5 hours 30 minutes**
