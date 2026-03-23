# Morse-Code-Decoder
Just as the name suggests it is a simple morse code decoder I put together inspired by cryptography and its application using digital and analog electronics.The circuit consists of an RC low pass filter,IC 74HC14 and an Arduino which uses __non-blocking logic__ to differentiate between dots,dashes or pauses.

The network consistes of a push button which is pressed and released by the user to send desired signal.This rocky analog signal is smoothened by a **low pass RC filter** with a value of time constant chosen through experimentation such that it filters out noise caused due to sudden presses or breadboard interference.
The signal is then passed onto the __74HC14__ which is a classic __hex-Schmitt trigger__ circuit(has __hysterisis__).The idea behind using this is to further clean the edges of the signal so that it may be purely digital when fed into the Arduino.
The Arduino uses a __struct look up table__ to assign alphabets for each symbolic representation.The code follows morse code standards that specify the duration and relative duration of each of the symbols.
Inspired by the intersection of early telecommunications and cryptography, this project demonstrates how analog signal conditioning (RC filtering and Hysteresis) acts as a physical layer of security/reliability before digital processing.
