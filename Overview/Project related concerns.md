## **General Concerns:**

- [X] 1) What is the total cost of the project?
      Ans) 1500 INR


## **Implementation Related Concerns:**


- [ ] 1)How to establish I2c connection between R-pi,arduino and magnetometer.

- [ ] 2)What is the data format of magnetometer ? are there libraries available for it ?

- [ ] 3)How to measure distance using rotary encoder? what would be the formula?

- [ ] 4)Are there other options for KEYES KY-040 ?

- [ ] 5)Where to place the rotary encoder? How to tackel the problem related to reading errors when vehicle makes a turn 
(possibly use to rotary encoders and chose smaller reading at every turn)

- [ ] 6) How to choose motor based on weight of vehicle? 

- [ ] 7) What mechanism to use for steering? and hence choose appropriate steering Motor.

- [ ] 8) If we use rack and pinion mechanism for steering, how will the front wheels return to its original/straight 
position after making the turn? (Use mechanism? or Use output of neural network like Gaussian steering?)

- [ ] 9) Which tiers to choose?

- [ ] 10) What will be the motor driver ratings?

- [ ] 11) How to control servo using motor driver? Any special caution needed? 

- [ ] 12) What will be the materials for chassis?

- [ ] 13) If materials of chassis is acrylic, where to purchase it and get laser cutting? (Ask Rahul)

- [ ] 14) What will be the shape and slots in chassis? (Body Design)

- [ ] 15) What should be capacity of LIPO? 

- [ ] 16) Should be use separate supply for electronics on board? Since all the motors can cause a 
lots of electrical noise.

- [ ] 17) How do we ensure that all electronics are safe from motor produced noise on power rails? 

- [ ] 18) How do we distribute the power to whole system?

- [ ] 19) How to make a simple Joystick to control steering during training? 
(Use a scrap Joystick or are there virtual options)



## **Concerns related to Software design**


- [ ] 1) What will be the structure of program on R-PI side?

- [ ] 2) What will be the structure of program on ANN side?
 
- [ ] 3) What are the Inputs to ANN?

- [ ] 4) What are the Outputs of ANN?

- [ ] 5) What are the terms and conditions of Mapbox?

- [ ] 6) What is the architecture of ANN?

- [ ] 7) What are the keywords of Mapbox  API for direction, turns, maneuver and bearing information?

- [ ] 8) How to parse JSON data, are there any libraries in Python?

- [ ] 9) How to load direction steps one-by-one?

- [ ] 10) Any Pre processing on image needed?

- [ ] 11) What to use for sign detection? (If using inception, then how to use it)

- [ ] 12) Are there any Encoding available to compress data for faster transfer between PI and PC?

- [ ] 13) How to do threading?

- [ ] 14) How to calibrate camera?

- [ ] 15) How to create Web socket?



