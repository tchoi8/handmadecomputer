A 1-bit computer has all the fundamental abilities of the traditional computing device. It can perfom **artithmetic**, add two single digit numbers and return a two digit output. It has a **clock** that creates a square wave oscillation, turning on and off an LED at varying speed. And it has **memory**, a latch that can store 1-bit of information, a zero or a one. 

 
![](https://farm6.staticflickr.com/5744/20578210488_c5016e6191_b.jpg =600x)
</br>
[Video]([Video](https://vimeo.com/136769465)
 

This version of **1 Bit Computer** is made of NAND logic gates. 
![](https://farm6.staticflickr.com/5667/20256616333_9961ff1b9b_b.jpg =600x)

NAND logic is a short name for **not** AND gate. A and B are inputs which can be either zero or one, and Y is the logical output. In the Van Diagram, every shape is colored except the intersecting region. This means the result is true for every input configuration **except** when both inputs are true.  

![](https://farm1.staticflickr.com/768/20256748743_ee1b9d967b_b.jpg =600x)


For AND Gate, if you are shaking 100 hands all at the same time, the result is true, or 1.

![](https://farm4.staticflickr.com/3886/14560630744_fac16725f9_b.jpg =600x)

In NAND Gate, if you are declined for date by 100 person at the same time, the result is true. 

NAND logic we are using only two inputs and and only when all of the inputs are false, or 0, the result is true, or 1. 


By combining NAND gate, we can make every other logic gates. This is called Universal Gate, because along with NOR gate, NAND can be combined to make every kind of logic. 

 
![](https://farm1.staticflickr.com/620/20773146321_b0c6b10767_o.jpg =600x)

It uses two TTL NAND Logic Chips, which are Integrated Circuit Chip that's designed to perform logical operations of NAND logic gate. The same concept can be made with Transistor, Vacuum tubes as well as with few lines of code in most programming languages. 

![](https://farm1.staticflickr.com/774/20812984222_590f7b06e4_b.jpg =600x)


With XOR and AND gate combined, we can make an Adder. Adder adds numbers. So in the world of Binary numbers, where every number is made of Zero and One, the output of the addition would be 10, not ten but One Zero. 
</br>
0+0=0</br>
0+1-1 </br>
1+0=1 </br>
1+1=10 </br>

The last condition where 1+1 carries over the number to the next digit is the case of AND gate, and the first digit acts like XOR gate. By combining both logic gates, we can make an adding machine which is called Half Adder.  

![](https://farm6.staticflickr.com/5795/20812986422_ee5529c19d_b.jpg =400x)

The second functionality of computer is to store data and remember information in bits. We are going to create the most primitive form of Computer Memory, Input, which is Set, can turn on and off the LED output, which is Q bar. If Reset is turned on, switch is assigned to 1, next time the Set is made 1, the LED output will remain lit even when S is no longer  a latch works by connecting output of the NAND logic gate to input of another NAND logic gate. This is a sequential circuit, which the output is affected by the input that was previously made. So the two inputs are called Set and Reset because it can be used interchangeably, thus a circuit like this is called Flip-flops as well. 

![](https://farm6.staticflickr.com/5800/20822480345_604712427c_b.jpg =400x)

Binary clock simply switch between Zero and One which is visible to us by LED not lit and then LED lit. The clock cycles is determined by how fast the clock switches between Zero and One. Unlike other circuits for the 1-bit computer, clock is made possible by utilizing a resistor and a capacitor and an electrical quality named as the Schmitt-Trigger. Basically, Output of NAND gate is connected via a variable resistor, which changes the amount of resistance between the input and output and connected to one of the input which is also connected to the Capacitor to the ground. The other input is connected to the Voltage, which eliminate the second input having 0 or False as the signal, turning NAND gate. The Input and Output of this gate is designed to have different value, but it's delayed by the resistor and capacitor. The Schimitt-Trigger makes enables the logic gate to remain unaffected until  is con input




Also [how to make Adder, Memory](https://farm8.staticflickr.com/7251/14007688534_adb24c48f8_k.jpg) with the logic gates. 
 

Making process 

- [Pictures](https://www.flickr.com/photos/80913365@N04/20093606613)
- [Teaching](https://www.flickr.com/photos/80913365@N04/20526747300)
-  Binary Logic Worksheet ![](https://farm8.staticflickr.com/7230/13984125176_91ccb45b3a_o.jpg =600x)


And out of NAND logic gates, you can make a 1 bit computer! 
[Here](https://github.com/tchoi8/handmadecomputer/tree/master/Binary/NAND)

 
