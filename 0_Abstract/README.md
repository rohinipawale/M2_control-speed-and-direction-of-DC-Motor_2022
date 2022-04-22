Before starting any project it always goes smoother when you take the time to clearly define the features/requirements. After a lot of thought and conversations with others, I came up with the following list of features:

A single input for motor direction
A single input for PWM (motor speed/torque)
Commutate the motor windings based on hall sensor feedback
Keep track of position through hall sensor feedback and communicate position to external microcontroller
Inputs for optional quadrature encoder
A “sample and hold” input to save the position at an instant in time into a buffer (for synchronizing multiple motors/controllers)
Some kind of communication protocol to communicate with external microcontroller
Works with 3.3v or 5v control circuitry and 8-36v motor power
As fast as possible using pin change interrupts and hardware communication
At the heart of this control board is an atmega328p microcontroller running at 16MHz, the same as used on the Arduino Uno, and programming is accomplished via an external ISP programmer. I played around with the idea of using a smaller/cheaper microcontroller, but after including all the features above I ended up using all but 3 of the available pins on the 328. Plus, going with the standard Arduino chip has the benefit of familiarity for me and many others.

