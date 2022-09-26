# Hardware Assembly

Acquire all the components in the Bill of Materials, and laser cut the acrylic sheet to fabricate mounting platforms for electronics using the provided [CAD files](https://github.com/Shathushan-Sivashangaran/XTENTH-CAR/tree/main/hardware/CAD_files). Use screws, nuts, washers, standoffs and velcro fasteners to complete the build.

1. Remove the stock Electronic Speed Controller (ESC), wireless receiver and antenna plastic housing from the chassis. Disconnect the DC brushless motor from the stock ESC, and steering servo motor from the wireless receiver.

2. Mount the VESC, ZED 2 stereo camera and SMALLRIG NP-F battery adapter plate to the laser cut base plate using screws, nuts and washers. Mount the USB 3.0 hub and NVIDIA Jetson Orin AGX Developer Kit using velcro fasteners. The VESC and USB 3.0 hub are mounted on the underside of the plate, and the other components are mounted on the top. Attach four 8" standoffs to the base plate to fasten to the roof plate.

3. Remove two screws each from the front and back of the chassis and replace with 6" standoffs. Screw the assembled base plate to the standoffs to mount it to the chassis.

4. Add bullet adapters to the DC brushless motor and connect it to the VESC. The white cable from the motor connects to cable A from the VESC, the yellow cable to B and blue cable to C.

5. Add 3 header pins to one end of the PPM extension cable and connect it to the steering servo motor. Connect the opposite end to the VESC PPM slot. Use a 1' micro USB cable to connect the VESC to the USB hub.

6. Mount the YDLIDAR G2 and data/power chip to the laser cut roof plate, and screw it to the standoffs attached to the base plate.

7. Connect the sensor USB cables to the USB hub.

8. Add the Traxxas 5000mAh 11.1V 3-cell LiPo battery to the chassis, and connect it to the VESC using the male TRX to female XT90 adapter.

9. Add the NP-F970 8800mAh battery to the SMALLRIG NP-F battery adapter plate, and connect it to the NVIDIA Jetson Orin AGX Developer Kit using a 5.5mm x 2.5mm 1' DC power cable.

10. Boot the Jetson Orin. Attach keyboard, mouse and monitor to install XTENTH-CAR software.

Disconnect and remove the batteries when not in use.



