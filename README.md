# Automated Parking System:     
## Project Description:        
Automated Parking systems are cost effective and also provide a hassle free experience compared to the traditional parking systems. They also reduce human effort by a great extent.      
To construct a prototype of an automated parking lot with the following features:      
1) Automated ENTRY and EXIT barriers      
2) Recording the number of cars entering and leaving the parking lot     
3) Displaying the free/occupied slots and guiding the user to an unoccupied parking space                  
## Why did I choose it?   
This project involves different functions and hence various components for all these functions. Therefore I can learn about various sensors and modules through a single project. I'll also get to learn how to interface these sensors and modules to the microcontroller and extracting and processing the information obtained from them.       
## Ideation:       
#### Pipeline:    
The pipeline can be broken into two parts:          
Pipeline 1: Sensors (To detect the presence of a car) --> Microcontroller --> Motor driver --> Motors (For opening/closing of the gates)  Pipeline 2: Sensors --> Microcontroller --> Wireless Communication Module --> User interface (To guide the user to an unoccupied parking space)      
##### Pipeline 1:   
In this part of the pipeline, we will require sensors for detecting a car entering/leaving the parking lot. The Entry/Exit of the parking lot will have barriers that open/close allowing cars to move in/out. So, we need to detect the motion/presence of an incoming car and send this information to the microcontroller, which will then guide the motor driver to operate the barrier. This can be acheived by:   
IR Transmitter and Receiver Module:          
The Transmitter-Receiver are placed in a single line and a communication is established between them. When this infrared signal is blocked by the car, the information is transmitted to the microcontroller which then drives the motors to open the gate. After the car passes the barrier, the communication between the transitter-receiver is setup again and the barrier closes. We can either introduce a delay after which the barrier has to close assuming an average time for the car to cross the barrier (or) we can have another IR Transmitter-Receiver pair across the barrier and the barrier closes after the car has crossed this pair of IR Module.    
Piezo Sensors:  A rather trivial approach for opening and closing the barriers is through piezo sensors. Piezo sensors detect the change in pressure. These piezo sensors are placed under the ramp and when a car passes through, they sense the change in pressure and this information is sent to the microcontroller. The microcontroller then drives the motor to open/close the barrier.      
##### Pipeline 2:     
This part of the pipeline deals with providing the parking lot information (free/occupied parking spaces) to the user. This will help guiding the user to a free parking space without any confusion, hence providing a hassle-free user experience.    
To achieve this, we need a sensor to detect the presence/absence of a car at a parking space. We can use Ultrasonic Sensors for this purpose. Each parking space has an ultrasonic sensor which detects if a car is present or not. This information is sent to the microcontroller and processed. The processed information is sent to the user via bluetooth. We use a bluetooth module to send this processed information from the microcontroller to the user interface indicating which parking space is unoccupied/occupied.        
## Components required, Feasibility and budget:      
| Component | Choice | Feasibility | Cost |       
|-----------|--------|-------------|------|       
| Sensor (for detecting the moving car) | IR Sensor Module | IR sensor modules are cheap and reliable and have great adaptive capability to ambient light. These are easy to use and interface and also consume less power | 50-200 INR|      


## Debugging:    
