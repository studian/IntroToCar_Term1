# SDC_Basic_Term1

# Joy Ride - Part 3: Parallel Parking
In this section you will write a function that implements the correct sequence of steps required to parallel park a vehicle.

**Note** for this segment the vehicle's maximum speed has been set to just over 4 mph. This should make parking a little easier.

![](https://upload.wikimedia.org/wikipedia/commons/2/26/ParallelParkingAnimation.gif)

## HTML Code
``
%%HTML
<button id="launcher">Launch Car Simulator</button>
<script src="setupLauncher.js"></script>
``

## Python3 Code
``
# CODE CELL
#
# Write the park function so that it actually parks your vehicle.

from Car import Car
import time

def park(car):
    # TODO: Fix this function!
    #  currently it just drives back and forth
    #  Note that the allowed steering angles are
    #  between -25.0 and 25.0 degrees and the 
    #  allowed values for gas are between -1.0 and 1.0
    
     # left turn, back
    car.steer(25)
    car.gas(-1.0)
    time.sleep(3.0) 

    # stop
    car.gas(0)
    
    # right turn, back
    car.steer(-25)
    car.gas(-0.5)

    # forward
    car.gas(1.0)
    time.sleep(0.2)

    # forward 
    car.gas(0.035)
    time.sleep(5.0)
    
    # stop
    car.steer(0)
    car.gas(0)
    time.sleep(5.0)    
    

car = Car()
park(car)
``
