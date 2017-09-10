> Arduino collects data from GPS, distance encoder, 3 ultrasonics and processes it to retrive meaningful data 
  and keep it ready to be passed to raspberry pi on demand via i2c protocol.
  
> Raspberry pi requests data from arduino and magnetometer via i2c and formats it into numpy array of data.

> Raspberry pi takes a snap of road via camera and appends this data to the numpy data_array.

> Raspberry pi transmits the data stream via wifi to PC to be processed via neural networks.

> The program on PC meanwhile has fetched a map from routing api (like OSRM or Mapbox) for a specified route and processed the response     via json parser to get essential data like steps, manuvers, distances, etc.
  
> This data is used to fetch one step from map at a time and added to the data from raspberry pi to be fed into an ANN.

> The image classifier (probably will use insception) looks at upper half of image data and detects road signs and gives out what is         detected.

> The steering directions given out via ANN and the road signs detected is used to finalize the driving command.

> driving command is sent to Raspberry pi .

> Raspberry pi sends these commands to motor drivers and hence drives the vehicle. 
