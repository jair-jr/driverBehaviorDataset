# Driver Behavior Dataset

The dataset is a collection of smartphone sensor measurements for driving events. An Android application is used to record smartphone sensor data, like Accelerometer, Linear Acceleration, Magnetometer and Gyroscope, while a driver executed particular driving events.

We performed the experiment in 4 car trips of approximately 13 minutes each in average. The experiment conditions were the following:

1. The vehicle was a 2011 Honda Civic;
2. The smartphone was a Motorola XT1058 with Android version 5.1;
3. The smartphone was fixed on the car's windshield by means of a car mount, and was neither moved nor operated while collecting sensor data;
4. The motion sensors sampling rate varied between 50 and 200 Hz, depending on the sensor;
5. Two drivers with more than 15 years of driving experience executed the driving events; and
6. The weather was sunny and the roads were dry and paved with asphalt.

Our purpose was to establish a set of driving events that represents usual real-world events such as breaking, acceleration, turning, and lane changes. The table below shows the 7 driving events types we used in this work and their number of collected samples. We strived to collect a balanced number of samples for each driving event type. However, we discarded 11 lane change events due to errors during the experiment. Therefore, the number of these events is slightly unbalanced. We also made our best effort to evenly distribute event samples between both drivers.


| Driving Event Type           | # of samples |
| ---------------------------- | ------------ |
| Aggressive breaking          | 12 |
| Aggressive acceleration      | 12 |
| Aggressive left turn         | 11 |
| Aggressive right turn        | 11 |
| Aggressive left lane change  | 4  |
| Aggressive right lane change | 5  |
| Non-aggressive event         | 14 |
| **Total**                    | **69** |

### Dataset structure

 Each folder represent a car trip, and in each folder is possible to find 6 files:
 
* aceleracaoLinear_terra.csv - File with the Linear Acceleration in 3 axis.
* acelerometro_terra.csv - File with the Acceleration in 3 axis.
* campoMagnetico_terra.csv -  File with the Magnetometer readings in 3 axis.
* giroscopio_terra.csv - File with the Gyroscope readings in 3 axis.
* groundTruth.csv - File with the start and end timestamps for each event. 
* viagem.json - Info about the smartphone used.

The following fields are commom in the files:

* timestamp -  Timestamp when the record is taken.
* uptimeNanos - Time in nanoseconds since the smartphone start.

The *groundTruth.csv* file have the start and end of the events, and has the following fields:

* evento - Type of event.
* inicio - Start of the event in seconds.
* fim - End of the event in seconds

The fields *inicio* and *fim* are counted since the start of the trip, so if the **inicio** field is 2 and the **fim** field is 4.5, the event started in the second 2 of the trip and ended in the second 4.5.

### Related work
 
The folowing works used this data set:
 
[Análise de Perfil de Motoristas: Detecção de Eventos por meio de Smartphones e Aprendizado de Máquina](http://sbrc2016.ufba.br/downloads/WoCCES/154831.pdf)

If you use this dataset in your work, fell free to send a PR to keep this list updated.
 
 
 
 
 
 
 
 
 
 
 
 
 
 