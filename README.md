# Table of Contents

* [Introduction](#introduction)
* [Air Quality Dataset](#air-quality-dataset)
* [Energy Applicances Weather Dataset](#energy-applicances-weather-dataset)
* [Optical Interconnection Dataset](#optical-interconnection-dataset)
* [Parkinsons Telemonitoring Dataset](#parkinsons-telemonitoring-dataset)

# Introduction
Located in this repository is four pre-cleaned multivariate time series datasets that have been formatted for usage with the jespipe application. Each directory in this repository is dedicated to a specific dataset, but you can read through this README file to gather info about the mentioned datasets or you can go to each datasets' respective directory and read through the .txt file.

# Air Quality Dataset
### Source: 
* https://archive.ics.uci.edu/ml/datasets/Air+Quality#

### Features in the CSV (in order from left to right): 
* True hourly averaged concentration CO in mg/m^3 (reference analyzer)
* True hourly averaged overall Non Metanic HydroCarbons concentration in microg/m^3 (reference analyzer)
* True hourly averaged Benzene concentration in microg/m^3 (reference analyzer) 
* PT08.S2 (titania) hourly averaged sensor response (nominally NMHC targeted)
* True hourly averaged NOx concentration in ppb (reference analyzer)
* PT08.S3 (tungsten oxide) hourly averaged sensor response (nominally NOx targeted) 
* True hourly averaged NO2 concentration in microg/m^3 (reference analyzer) 
* PT08.S4 (tungsten oxide) hourly averaged sensor response (nominally NO2 targeted)
* PT08.S5 (indium oxide) hourly averaged sensor response (nominally O3 targeted) 
* Temperature in C
* Relative Humidity (%) 
* Absolute Humidity
* PT08.S1 (tin oxide) hourly averaged sensor response (nominally CO targeted) 

### Notes: 
* PT08.S1 (tin oxide) is the feature to predict
* Dataframe total shape is (9357, 13)
* The local intrinsic estimation value is 5.8476

# Energy Applicances Weather Dataset
### Source: 
* http://archive.ics.uci.edu/ml/datasets/Appliances+energy+prediction

### Features in the CSV (in order from left to right): 
* Appliances - energy use in Wh 
* Lights - energy use of light fixtures in the house in Wh 
* T1 - Temperature in kitchen area, in Celsius 
* RH_1 - Humidity in kitchen area, in % 
* T2 - Temperature in living room area, in Celsius 
* RH_2 - Humidity in living room area, in % 
* T3 - Temperature in laundry room area 
* RH_3 - Humidity in laundry room area, in % 
* T4 - Temperature in office room, in Celsius 
* RH_4 - Humidity in office room, in % 
* T5 - Temperature in bathroom, in Celsius 
* RH_5 - Humidity in bathroom, in % 
* T6 - Temperature outside the building (north side), in Celsius 
* RH_6 - Humidity outside the building (north side), in % 
* T7 - Temperature in ironing room , in Celsius 
* RH_7 - Humidity in ironing room, in % 
* T8 - Temperature in teenager room 2, in Celsius 
* RH_8 - Humidity in teenager room 2, in % 
* T9 - Temperature in parents room, in Celsius 
* RH_9 - Humidity in parents room, in % 
* To - Temperature outside (from Chievres weather station), in Celsius 
* Pressure (from Chievres weather station), in mm Hg 
* RH_out - Humidity outside (from Chievres weather station), in % 
* Wind speed (from Chievres weather station), in m/s 
* Visibility (from Chievres weather station), in km 
* rv1  Random variable 1, nondimensional 
* rv2 Random variable 2, nondimensional 
* Tdewpoint (from Chievres weather station), in Celsius

### Notes: 
* Two random variables have been included in the data set for testing the regression models and to filter out non predictive attributes (parameters)
* Tdewpoint is the feature to predict
* Dataframe total shape is (19735, 28)
* The local intrinsic estimation value is 9.35095

# Optical Interconnection Dataset
### Source: 
* https://archive.ics.uci.edu/ml/datasets/Optical+Interconnection+Network+

### Features in the CSV (in order from left to right): 
* Node number - The number of the nodes in the network. (8x8 or 4x4).
* Thread number - The number of threads in each node at the beginning of the simulation.
* Spatial distribution - The performance of the network is evaluated using synthetic traffic workloads. Uniform (UN), Hot Region (HR), Bit reverse (BR) and Perfect Shuffle (PS) traffic models have been included. I have encoded them into unique integer [0,3] in that order.
* Temporal distribution - Temporal distribution of packet generation is implemented by independent traffic sources. They utilized client server traffic (i.e., a server node sends packets to respond to the reception of packets from clients) and asynchronous traffic (i.e., initially, all nodes generate traffic independently of the others; as time progresses, traffic generation at the source/destination nodes depends on the receipt of messages from destination/source nodes).
* T/R - Message transfer time (T) Uniformly distributed with mean in range from 20 to 100 clock cycles. Thread run time (R) Exponentially distributed with a mean of 100 clock cycles.
* Processor utilization - The average processor utilization measures the percent of time that threads are running in the processor. 
* Channel waiting time - Average waiting time of a packet at the output channel queue until it is serviced by the channel. 
* Input waiting time - Average waiting time of a packet until it is serviced by the processor.
* Channel utilization - The percent of time that the channel is busy transferring packets to the network. 
* Network response time - The time between a request message is enqueued at the output channel and the corresponding data message is received in the input queue.

### Notes: 
* Network response time is the feature to predict
* Dataframe total shape is (640, 10)
* The local intrinsic estimation value is 2.7109 

# Parkinsons Telemonitoring Dataset
### Source: 
* http://archive.ics.uci.edu/ml/datasets/Parkinsons+Telemonitoring

### Features: 
* subject# - Integer that uniquely identifies each subject 
* age - Subject age 
* sex - Subject gender '0' - male, '1' - female 
* test_time - Time since recruitment into the trial. The integer part is the number of days since recruitment. 
* motor_UPDRS - Clinician's motor UPDRS score, linearly interpolated 
* total_UPDRS - Clinician's total UPDRS score, linearly interpolated 
* Jitter(%),Jitter(Abs),Jitter:RAP,Jitter:PPQ5,Jitter:DDP - Several measures of variation in fundamental frequency 
* Shimmer,Shimmer(dB),Shimmer:APQ3,Shimmer:APQ5,Shimmer:APQ11,Shimmer:DDA - Several measures of variation in amplitude 
* NHR,HNR - Two measures of ratio of noise to tonal components in the voice 
* RPDE - A nonlinear dynamical complexity measure 
* DFA - Signal fractal scaling exponent 
* PPE - A nonlinear measure of fundamental frequency variation 

### Notes: 
* PPE is the feature to predict
* Dataframe total shape is (5875, 22)
* The local intrinsic estimation value is 4.7380 
