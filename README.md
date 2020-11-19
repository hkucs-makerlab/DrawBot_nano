GRLB-Scara for cnc-shield.v4 Nano based on GRLB 0.9j.

The servo drive is controlled by the command "M3 Sx" (x sets the angle, changes: 0-1000) and "M5: on pin Z +. It is recommended to use a separate + 5V power supply for the servo drive, since there is no separate power supply on the cnc-shield v.4 board. voltage regulator, but the built-in nano v3 is used, which is not designed for a constant load of the servo motor.

Added the ability to calibrate DrawBot with the "$ M" command. Calibration is performed from a 45-degree shoulder position and theta ($ 30) and psi ($ 31) parameters are calculated and saved.

[![Калибровка](https://github.com/akv47/DrawBot_nano/blob/main/pic/calibration.jpg)]

For compilation, you need to use the light and fast core GyverCore https://alexgyver.ru/gyvercore/ (developed by AlexGyver and Egor 'Nich1con' Zaharov), since on the original Nano_V3 core (ATmega328p) the size of the binary file will exceed the size of the controller's flash memory.

[![Смотреть демо](https://github.com/akv47/DrawBot_nano/blob/main/pic/video.jpg)](https://youtu.be/JfaiAnQvb0s)

Added parameters:

$ 28 = 200.0 (Shoulder of the arm from the side of the stepper motors)

$ 29 = 200.0 (Shoulder of the arm from the side of the handle)

$ 30 = 45.720 (angle theta)

$ 31 = 92.030 (corner psi)

After changing the parameters, you need to reset the arduino by hardware.

Complete list of LaserGRBL parameters:

$0=10 (Step pulse time)

$1=254 (Step idle delay)

$2=0 (Step pulse invert)

$3=3 (Step direction invert)

$4=0 (Invert step enable pin)

$5=1 (Invert limit pins)

$6=0 (Invert probe pin)

$10=3 (Status report options)

$11=0.010 (Junction deviation)

$12=0.002 (Arc tolerance)

$13=0 (Report in inches)

$20=0 (Soft limits enable)

$21=0 (Hard limits enable)

$22=1 (Homing cycle enable)

$23=3 (Homing direction invert)

$24=250.000 (Homing locate feed rate)

$25=1000.000 (Homing search seek rate)

$26=0 (Homing switch debounce delay)

$27=1.000 (Homing switch pull-off distance)

$28=200.000 ()

$29=200.000 ()

$30=45.720 ()

$31=92.030 ()

$100=48.800 (X-axis travel resolution)

$101=48.800 (Y-axis travel resolution)

$102=48.800 (Z-axis travel resolution)

$110=2000.000 (X-axis maximum rate)

$111=2000.000 (Y-axis maximum rate)

$112=800.000 (Z-axis maximum rate)

$120=100.000 (X-axis acceleration)

$121=100.000 (Y-axis acceleration)

$122=250.002 (Z-axis acceleration)

$130=320.000 (X-axis maximum travel)

$131=220.000 (Y-axis maximum travel)

$132=200.000 (Z-axis maximum travel)
