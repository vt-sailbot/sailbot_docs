# <p style="text-align: center;"> GPS </p>

## **Summary**
This node is responsible for communicating back and forth between our GPS ([Sparkfun NEO-M8P-2](https://www.sparkfun.com/products/15005)) and using various filtering techniques to clean the data and make it less noisy. Our GPS gives us both position and velocity data by tracking satellites in the sky, so performance may vary depending on how cloudy it is.

In the future we may also want to look into RTK (real time kinematics) to increase our GPS accuracy, but even without that, our GPS module is really precise with 0.5 meter accuracy! RTK would be nice though because it allows us to apply less aggressive filtering techniques and still get good results.

## Command to Run the Node
``` sh
ros2 run gps gps
```

<br>
## Publishes to the Following Topics
- /position (NavSatFix from sensor_msgs)
- /velocity (Twist from geometry_msgs)