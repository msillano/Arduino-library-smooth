# Arduino-library-smooth
This library allows to get accurate analog values, using a moving average  over ADC reading.
The smooth values are more precises, car the average reduces the influence of random errors (sampling ADC error: +/- 1 bit).
More reading are used for the average, more higth is the precision of the average, but the use of moving averages introduces a delay in readings, so every application need the rigth balance between precision and delay.

-  The constructor gets 2 parameters: the number or readings used for the average (max 30) and the reference voltage  (in mV, default 5000) used by the ADC. 
-  The method Smooth.put() adds a reeding to a circular buffer storing last readings.
-  The method Smooth.avg() returns the reedings average as a float.
-  The method Smooth.get() returns the reedings average in mV, as a Int.
-  The method Smooth.peek() returns the last value in mV, as a Int.


