# Exp-01-INTRODUCTION-TO-ARDUINO-IDE

INTRODUCTION TO ARDUINO & IDE


AIM: To familiarize the operation of Arduino uno and understand the operation of IDE 
EQUIPMENT/ COMPONENTS REQUIRED:
	Hardware: Arduino uno 
	Software: Arduino IDE 
THEORY:
Arduino is an open source electronics prototyping platform composed of a microcontroller, a Programming language, and an IDE. Arduino is a tool for making interactive applications, designed to simplify this task for beginners.
The first thing you need to do if you want to work with Arduino is to buy an Arduino board and a standard USB cable (A-to-B plug if you are using an Arduino Uno). Well, of course you will need more than this if you want to build any reasonable useful application, but for the moment you’ll just work with the bare essentials. Arduino runs on Windows, Mac OS X, and Linux, so there’s a version of Arduino for you whatever your OS. Go to the Arduino software web site at http://arduino.cc/en/Main/Software and download the version of the software compatible with your system. If after reading the following sections you are still having trouble with the installation, you can have more detailed information at http://arduino.cc/en/Guide/HomePage.

You need to install the Arduino drivers before you can start working with your board. Assuming you are installing an Arduino Uno, follow these steps:
. Plug your board to your computer, and wait for Windows to start the driver installation process. 
. Click Start menu and open the Control Panel.
. Go to System and Security, then System and then Device Manager.
. Find the Arduino Uno port listed under Ports (COM & LPT).
. Right-click on it, and choose “Update Driver Software,” selecting “Browse my Computer for Driver Software.”
. Finally, navigate and select the Arduino Uno’s driver file named ArduinoUNO.inf located in the Drivers folder of the Arduino software folder you have just downloaded. Windows will successfully install the board now.

BOARD SELECTION :
 

[My image](username.github.com/repository/img/image.jpg)
FIGURE -01





PORT SELECTION 


 
FIGURE-02


ARDUINO INPUT AND OUTPUT PINS
The Arduino Uno has 14 digital input/output pins and six analog input pins, as shown in Figure. As mentioned, these pins correspond to the input/output pins on your ATmega microcontroller. The architecture of the Arduino board exposes these pins so they can be easily connected to external circuits. Arduino pins can be set up in two modes: input and output. The ATmega pins are set to input by default, so you don’t need to explicitly set any pins as inputs in Arduino, although you will often do this in your code for clarity.


 

FIGURE-03








FIGURE-04



Figure -04 shows various symbols associated with IDE 

 

FIGURE -03
Figure -03 shows the functional view of serial monitor with a baud of 9600.

THE LOOP() FUNCTION
The loop() function is run continuously in an endless loop while the Arduino board is powered. Thisfunction is the core of most programs.
In this example, you turn pin 13’s built-in LED on using the function digitalWrite() to send a HIGH (5V) signal to the pin. Then you pause the execution of the program for one second with the function delay(). During this time, the LED will remain on. After this pause, you turn the LED off, again using the function digitalWrite() but sending a LOW (0V) signal instead, and then pause the program for another second. This code will loop continuously, making the LED blink.
void loop() {
digitalWrite(13, HIGH);
delay(1000);
digitalWrite(13, LOW);
delay(1000);
}
This code would not actually be seen as a valid C++ program by a C++ compiler, so when you click Compile or Run, Arduino adds a header at the top of the program and a simple main() function so the code can be read by the compiler.
Variables
In the previous example, you didn’t declare any variables because the sketch was rather simple. In morecomplex programs, you will declare, initialize, and use variables.
Variables are symbolic names given to a certain quantity of information. This means you will associate a certain piece of information with a symbolic name or identifier by which you will refer to it.
Variable Declaration and Initialization
In order to use a variable, you first need to declare it, specifying at that moment the variable’s data type.
The data type specifies the kind of data that can be stored in the variable and has an influence in the amount of memory that is reserved for that variable.
As Arduino language is based on C and C++, the data types you can use in Arduino are the same
allowed in C++. Table 1-2 lists some of the data types you will use throughout this book. For a complete listing of C++ data types, you can refer to C++ reference books and Internet sites.
Arduino Fundamental Data Types
Name Description Size Range
char Character or small integer 1byte Signed: -128 to 127
Unsigned: 0 to 255
Boolean
 Boolean value (true or false) 1byte True or false
int Integer 4bytes Signed: -2147483648 to 2147483647
Unsigned: 0 to 4294967295
long Long integer 4bytes Signed: -2147483648 to 2147483647
Unsigned: 0 to 4294967295
float Floating point number 4bytes +/- 3.4e +/- 38 (~7 digits)
double Double precision floating point number 8bytes +/- 1.7e +/- 308 (~15 digits)
When you declare the variable, you need to write the type specifier of the desired data type followed
by a valid variable identifier and a semicolon. In the following lines, you declare an integer, a character,
and a Boolean variable:
int myInteger;
char myLetter;
boolean test;
This code has declared the variables, but their value is undetermined. In some cases, you want to declare the variable and set it to a default value at the same time. This is called initializing the variables. If you want to do this, you can do it in the following way:
int myInteger = 656;
char myLetter = 'A';
boolean test = true;
By doing this, your three variables are set to specific values and you can start using them from this moment on.
In other cases, you want to declare the variables first and initialize them later. You will see this happening frequently, as it’s necessary when you want to declare the variable as global but its value depends on other variables or processes happening within the setup(), draw(), or other functions.
int myInteger;
char myLetter;
boolean test;
setup(){
myInteger = 656;
myLetter = 'A';
test = true;
}
Variable Scope
When you declare your variables, the place you do it within the code will have an impact on the scope in which the variable will be visible. If you declare your variable outside of any function, it will be considered a global variable and will be accessible from anywhere in the code. If you declare your variable within a function, the variable will be a local variable and will only be accessible from within the same function. Let’s do an example from the Blink sketch.
int ledPin = 13;
void setup() {
pinMode(ledPin, OUTPUT);
int myOtherPin = 6;
pinMode(myOtherPin, OUTPUT);
}
void loop() {
digitalWrite(ledPin, HIGH); // set the LED on
delay(1000); // wait for a second
digitalWrite(ledPin, LOW); // set the LED off
delay(


RESULTS:
Functioning of arduino uno and IDE is studied.


