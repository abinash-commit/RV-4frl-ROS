# RV-4frl-ROS
Connecting and Operating the RV-4FRL from Rviz.

Get the melfa ros2 driver from 
https://github.com/Mitsubishi-Electric-Asia/melfa_ros2_driver.git

Create a new ros workspace create a src folder put the melfa ros2 driver in ur src.
Colcon build ur workspace and source.

This workspace have content for various type of mitsubushi ARMs, we are going to use for RV-4FRL.
(u can clear out the workspce from other for ease of reading)

Setup the program in Teach Pendant 

'''
Servo On
Open "ENET: 192.168.0.100" As #1 'Insert your Linux Machine IP address in this line. Open stores the IP address into variable 1.
Mxt 1,1,10 'The first 1 refers to the IP address from the line above. 
           'The second 1 configures Mxt to expect Joint commands. 
           'The 10 refers to a 10ms low pass filter.
End 
'''
