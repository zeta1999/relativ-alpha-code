# Relativ Alpha Code
This Repo is a collection of Arduino Sketches and Documents for the Relativ Alpha Code Testers community. We are busy testing out various different sensor technologies because time moves on, and technology moves on with it. Our lovely old MPU-6050 based tracker may be solid as a rock, but the tech is showing its age. This is where we begin to make our future happen...

At the moment, we are doing well. Pretty much all of the sketches actually work!

This is often not the case, because it is all very much alpha code, and all very much in development.

Our software is thankfully hardware agnostic, meaning that you can use *any* of our trackers and/or sensors with it. It just expects to get a stream of Quaternions, and it doesn't care who or what is sending them down the wire.

Unfortunately, the choice of Sensor chip that we are currently alpha testing has been rather fluid of late. Not long ago, we were using the MPU-9250 - but just as we started to get it to play nicely and do what we required we realised that its manufacturers had obsoleted it and stopped production. So we looked for a better alternative.

We moved onto boards based on the BNO055 chip. Yes, the BNO080 is supposedly better, but it didn't seem to have as many resources available. Adafruit had a really solid library for the BNO055, so we were up and running in next to no time. We are now testing out the various different BNO055 boards, as oddly enough, each one has its own unique feature set.

---

## Trackers based on the MPU-9250 sensor chip

### 9DoF_Tracker
The 9DoF_Tracker is one of our first sketches based on the MPU-9250 sensor chip. It was a really early version, and although it worked, it was really jumpy...

### 9DoF_Tracker2
The 9DoF_Trackers sketch updates the original sketch and appears to eliminate the jumpiness. However, you do apparently need a more powerful Arduino board to run it. On a Nano, it is still jumpy. On an STM32 Black Pill, it runs really well. We assume that this is evidence of the difference between an I2C clockspeed of 100kHz and 400kHz.

Please test this sketch if you can, and see what your impressions of it are.
This sketch should be headset ready, if you have a 9250 board (or a 9255 board, if you follow the instructions on the Wiki). 

---

## Trackers based on the BNO055 sensor chip

### Relativ-BNO055-01
The Relativ-BNO055-01 sketch is a 9DoF tracker based on the BNO055 sensor. You will need to install the Adafruit Unified Sensor Library and the Adafruit BNO055 Library to get it working. It uses the small, blue, rectangular, GY-BNO055 breakout boards that are widely available online. It was developed and tested using an STM32 but should work on other Arduino boards.

The Relativ-BNO055-01 sketch is pretty much ready to test in your headset right now, if you have a BNO055 board

The main actor in the Alpha development is Justin
