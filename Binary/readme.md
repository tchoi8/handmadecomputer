[⇐ INTERFACE](https://github.com/tchoi8/handmadecomputer/blob/master/Interface/readme.md)

A *1 Bit Computer* has the fundamental abilities of the traditional computer. It can perfom artithmetic, add two single digit numbers and return a two digit output. It has a clock that creates a square wave oscillation that turns an LED on and off at varying speed. And it has memory, a latch that can store 1-bit of information, zero or one. 

 
![](https://farm6.staticflickr.com/5744/20578210488_c5016e6191_b.jpg =600x)


[Video](https://vimeo.com/136769465)
 

This version of *1 Bit Computer* is made of NAND logic gates. 
![](https://farm6.staticflickr.com/5667/20256616333_9961ff1b9b_b.jpg =600x)

NAND is short for *not* AND logic. Here A and B are inputs, either of which can be zero or one, and Y is the logical output. In the venn diagram above, depicting possible input state configurations, every shape is colored except the intersecting region. This means the result is true in every case *except* when both inputs are true.  

Before we get into the details of *1 Bit Computer*, let's return to the idea of zero and one, binary numbers, and their boolean logic.

 ![](https://dl.dropboxusercontent.com/u/53638/true-false.jpg)


By combining NAND gates in various arrangements we are able to make every other logic pattern. This is called the *universal gate*, because along with the NOR gate, NAND can be combined to map any input instruction to any output. 

![](https://farm6.staticflickr.com/5820/20361778943_2ee62221a9_b.jpg =600x)
 
![](https://farm1.staticflickr.com/620/20773146321_b0c6b10767_o.jpg =600x)

This 1 bit computer uses two TTL NAND logic chips, which are integrated circuit chips designed to perform NAND operations. The same logic could be implemented with transistors, vacuum tubes, or few lines of code in most programming languages.

![](https://farm1.staticflickr.com/774/20812984222_590f7b06e4_b.jpg =600x)

 You can click on the switches to see the Half Adder working, it adds one digits of number.  ```[This is where interactive component comes in.]``` 
 
![](https://farm6.staticflickr.com/5717/20990175911_2ceb98c8c6_b.jpg =400x)

With XOR and AND gates combined, we can make an adder. Adders add numbers. So in the world of binary numbers, where every number is made of zeros and ones, the output of the addition would be 10, not ten but "one, zero." 
</br>
0+0=0</br>
0+1=1 </br>
1+0=1 </br>
1+1=10 (2 in decimal notation) </br>

![](https://farm6.staticflickr.com/5826/21055702651_1ff54a87e9_b.jpg =600X)


In the last case, where the sum of 1+1, 10 requires we carry the 1 over to the next place, the next digit is fed to the AND gate, and the first digit acts like an XOR gate. By combining both logic gates, we can make an adding machine, called a *half adder*.  

![](https://farm6.staticflickr.com/5795/20812986422_ee5529c19d_b.jpg =400x)

The second basic computing operation is data storage, remembering information in bits. We are going to create the most primitive form of computer memory, where an input *set* can turn on or off an LED output, *Q bar*. If the reset switch is then toggled, *switch* is assigned to 1, and next time the *set* is made 1 and the LED output will remain lit even when *set* is no longer pressed. A latch works by connecting output of the NAND logic gate to input of another NAND logic gate. This is a sequential circuit, in which the output is affected by the input that was previously made. So the two inputs are called *set* and *reset* because they can be used interchangeably. A circuit like this is called a flip-flop as well. 

![](https://farm6.staticflickr.com/5800/20822480345_604712427c_b.jpg =400x)

```[You can turn the knob to change the frequency.]``` 
The binary clock simply switches between zero and one, visible to us as 'LED not lit,' and then 'LED lit.' The period in which the LED blinks, or the clock cycle, is determined by how fast the circuit switches between zero and one. The clock is made possible by utilizing the electrical properties of the specific kinds of NAND logic gate chips (CD4093 or 74132) called the *Schmitt-Trigger* which delays the response time of the logic based on a threshold. By creating a network of variable resistor and capacitor between the input and output of the logic, NAND gate oscillates between Zero and One to produce constant frequency, also know as a clock signal.  


Also [how to make Adder, Memory](https://farm8.staticflickr.com/7251/14007688534_adb24c48f8_k.jpg) with the logic gates. 
 

### Extras

Making process 

- [Pictures](https://www.flickr.com/photos/80913365@N04/20093606613)
- [Teaching](https://www.flickr.com/photos/80913365@N04/20526747300)
-  Binary Logic Worksheet ![](https://farm8.staticflickr.com/7230/13984125176_91ccb45b3a_o.jpg =600x)


And out of NAND logic gates, you can make a 1 bit computer! 
[Here](https://github.com/tchoi8/handmadecomputer/tree/master/Binary/NAND)

[CPU DUMPLING SHOP ⇒](https://github.com/tchoi8/handmadecomputer/blob/master/Dumpling/readme.md)
