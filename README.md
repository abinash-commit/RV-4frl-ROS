# RV-4frl-ROS
Connecting and Operating the RV-4FRL from Rviz.

Get the melfa ros2 driver from 
https://github.com/Mitsubishi-Electric-Asia/melfa_ros2_driver.git  
  
Create a new ros workspace create a src folder put the melfa ros2 driver in ur src.  
Colcon build ur workspace and source.

This workspace have content for various type of mitsubushi ARMs, we are going to use for RV-4FRL.  
(u can clear out the workspce from other for ease of reading)

## Connecting ur robot to ROS 
Connect ur robot to ur linux system with lan cable and setup the IPV4 manually, we are gonna use this IP from now on.   
Keep the gateway and mask same as ur robot.  
![Screenshot from 2025-06-21 11-59-02](https://github.com/user-attachments/assets/7eba99e3-4232-4ae1-9a80-b0e4ebf2daaa)

## Robot IP   
U can get the robot ip gateway and mask from the teach pendant "param" option.   
![image](https://github.com/user-attachments/assets/e34d2e45-d141-4b90-9026-c3965d7c7560)

For ip use "NETIP"  
For gateway "NETGW"  
For mask "NETMSK"


## Robot Code
Setup the program in Teach Pendant, change the IP address to ur linux system IP.   
```
Servo On
Open "ENET: 192.168.0.100" As #1 'Insert your Linux Machine IP address in this line. Open stores the IP address into variable 1.
Mxt 1,1,10 'The first 1 refers to the IP address from the line above. 
           'The second 1 configures Mxt to expect Joint commands. 
           'The 10 refers to a 10ms low pass filter.
End 
```

## Code Run TEACH
Switch to Auto Mode, go to RUN>OPERATION select ur programm, turn servo ON and hit "START".   

## Launch ur ROS file
For our RV-4frl we are gonna launch   
```

```

