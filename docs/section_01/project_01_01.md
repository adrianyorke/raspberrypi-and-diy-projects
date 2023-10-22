# Project 01.01 - step-by-step procedure for flashing led light Raspberry Pi

![image](https://github.com/adrianyorke/raspberrypi-and-diy-projects/assets/115374818/aec01774-cd41-48e8-87e9-04dd38dbd5f4)

## Step 1: Needed Components

![image](https://github.com/adrianyorke/raspberrypi-and-diy-projects/assets/115374818/b0ce094c-5a26-4f9a-9ea0-95b2850135aa)

For the build, you will need the following:

- 1 x Raspberry Pi
- 1 x USB cable
- 1 x LED
- 1 x Breadboard
- 1 x SD Card and adapter (4GB minimum)
- 1 x LAN cable
- 1 x 50-ohm resistor
- 2 x Jumper wires



## Step 2: Building the Circuit

![image](https://github.com/adrianyorke/raspberrypi-and-diy-projects/assets/115374818/9b35a060-d61c-4ee0-bf84-74dd27c85a70)

Every LED has two sides - one negative and one positive. Choose the negative one and using the resistor, connect it up to GND (pin 6). The other end goes to pin 18. Feel free to use the picture as a reference.



## Step 3: Setting Up the Raspberry

![image](https://github.com/adrianyorke/raspberrypi-and-diy-projects/assets/115374818/9757e8ca-f26a-4c0f-a893-5771dc88487b)

Enter the following command:

```
sudo apt-get install python
```

or

```
sudo apt-get install python3
```

(depending on the version that you choose)



## Step 4: Writing the Program</h3>

![image](https://github.com/adrianyorke/raspberrypi-and-diy-projects/assets/115374818/4e43dd28-870d-4e3e-b0fc-69d2cc9c1053)

You need to use a simple text editor called nano, so enter the command sudo nano <b>file-name.py</b>

* Where file-name is a name of your choice. Remember it, we will need it later!


Paste the following code in the newly-created file:

```

import RPi.GPIO as GPIO

import time

GPIO.setmode(GPIO.BCM)

GPIO.setwarnings(False)

GPIO.setup(18,GPIO.OUT)

print "LED on"

GPIO.output(18,GPIO.HIGH)

time.sleep(1)

print "LED off"

GPIO.output(18,GPIO.LOW)

```


## Step 5: Running the Program</h3>

![image](https://github.com/adrianyorke/raspberrypi-and-diy-projects/assets/115374818/a96e7e48-c88b-45bc-b909-f9e55e46e7de)

![image](https://github.com/adrianyorke/raspberrypi-and-diy-projects/assets/115374818/dd75c8cc-deee-485d-87be-cce2931311f9)



