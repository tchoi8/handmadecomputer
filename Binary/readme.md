[⇐ INTERFACE](https://github.com/tchoi8/handmadecomputer/blob/master/Interface/readme.md)

```
- Beginning work on this chapter on a separate branch, some plans on [Issue 7](https://github.com/tchoi8/handmadecomputer/issues/7)
- Actively responding to [Issue 8](https://github.com/tchoi8/handmadecomputer/issues/8)
```

#What is a Computer?

"Now let's make a computer! Wait, what is a computer?

Well, that's a little difficult to explain, even for experts, but let's start by giving an ostensible definition, specifying a system which can "compute" something.

Ok... but what does it mean to be "computed"?

Oddly enough, the widely accepted meaning of a [computable talk](https://en.wikipedia.org/wiki/Computable_function) is the intuitive one: any operation which is capable of being reliably carried out by a machine according to a specific sequence of instructions or algorithm. If that seems circular, it's because the fundemental limits of computation are still largely unknown (and potentially unknowable), therefore any axiomatic description of universal computation remains hypothetical.

But we see algorithms all around us, repeated patterns of action and process. Surely we can describe some of these mechanisms?

Alan Turing's work prior to WWII was focused on just this question. Turing developed a framework which he called automatic machines, known today as *turing machines*, to encode mechanistic processes as general symbolic expressions.

Turing along with Alonzo Church, the creator of λ-calculus, concurrently [postulated](https://en.wikipedia.org/wiki/Church%E2%80%93Turing_thesis) that the set of all automatic machines had equivalent functional capabilities. In affect, that the operation of any computing machine could be replicated by a turing machine, thus formalizing the notion of *turing completeness* and offering the possibility of building a general, stored-program computer.

This device fed an arbitrary length of ticker tape with a series of discrete symbols through a reading window...

and debate continues as to whether all physical processes are computable.

[turing machine & turing completeness, shannon & information theory?]

Here we'll be building a simple computer with three capabilities.

Computers can do arithmetic operations (adding, multiplying, etc.),

they can remember information, like the inputs and outputs of those arithmetic operations, or a specific sequence of arithmatic.

Lastly, computers can keep time, so they can carry out the operations above in the sequence they've remembered.

Computers, even in its simpliest form will have all of these functionalities. We are going to use electronics to make it into a circuit".

```abstraction and repetition to make a computer```

```real world > zero and one, encoding & symbolic logic -- shannon and bool -- dawn and dusk -- digital computer is new```

```city and human computation, analog computing is the default form of computation > we want to represent the analog world with zero and one because efficiency of info - send message over distance, imagine sending messages from one city to another```

#Electronic friends!


 
Until this point, the computers we talked about have been purely symbolic, it existed in ideas. We can begin to make it with electronic circuits. 

![](https://c1.staticflickr.com/1/611/22340720565_92eea56285_b.jpg)

The circuits need batteries to work. 

- Voltage 
- Current 
- The potential difference between the voltages. 
- 5 Volt circuit 

 

![](https://c1.staticflickr.com/1/687/22314996206_cd76e47522_b.jpg)

This is a LED, Light Emitting Diode. It lights up brightly when an electrical signal goes through two metal rods. The metal part is conductive, the electrical current pass through it. If we connect LED into a battery, and if it's connected in the right side, it will light up. The battery is charged with energy which go through the 


This is a switch, which we use as an Input for our circuit. Switch allows us to change the connection between two points. 
![](https://c1.staticflickr.com/1/778/22327706442_cc76cd5161_b.jpg)

This switch controls the connection between the middle pin and two pins by it's side. It's always connected to one of them. It's just like how our Input is either always Zero or One. 

 

![](https://c1.staticflickr.com/1/671/20574668810_9c957dfff4_o.jpg)

``` Transistor here. probably not Mr.Tr. make it gender neurtral.]```
   Take some information from this page on [transistor](https://github.com/tchoi8/handmadecomputer/tree/iss7/TTL)
   
   ![](https://c1.staticflickr.com/1/765/21717941984_3b2b774410_b.jpg)
   
 
#Binary logic 



``` Break from the technical details, change tones slightly. Brief mention of Claude Shannon's paper on switching circuits and George Boole' logic. Explain Binary with Thumbs up & down and Venn Diagram. Also introduce Integrated Circuit and the idea of abstraction here.``` 


Before we get into the details of *1 Bit Computer*, let's return to the idea of zero and one, binary numbers, and their boolean logic.



NAND is short for *not* AND logic. Here A and B are inputs, either of which can be zero or one, and Y is the logical output. In the venn diagram above, depicting possible input state configurations, every shape is colored except the intersecting region. This means the result is true in every case *except* when both inputs are true.  
 ![](https://c1.staticflickr.com/1/613/21839648508_2346bd533a_o.jpg =600x)


It's exhauting to go through these logic stuff, but believe me, it's like climbing a mountain. You will get a great view in the end!  
 
 
By combining NAND gates in various arrangements we are able to make every other logic pattern. This is called the *universal gate*, because along with the NOR gate, NAND can be combined to map any input instruction to any output. 

![](https://dl.dropboxusercontent.com/u/53638/nands.jpg)
 
 
![](https://farm6.staticflickr.com/5717/20990175911_2ceb98c8c6_b.jpg =400x)

With XOR and AND gates combined, we can make an adder. Adders add numbers. So in the world of binary numbers, where every number is made of zeros and ones, the output of the addition 1 + 1 would be 10, not ten but "one, zero" or two. 
 
```0+0=0 Zero plus Zero is Zero.``` 

```0+1=1 Zero plus One is One.``` 

```1+0=1 One plus Zero is One.``` 

```1+1=10 One plus One is Two.```

However, this is read 'One Zero' in Binary numbers, not Ten as in Decimal numbers. It's value is the same as Two in Decimal numbers. 

![](https://farm6.staticflickr.com/5826/21055702651_1ff54a87e9_b.jpg =600X)


![](https://c1.staticflickr.com/1/579/21841043889_33c3084915_b.jpg =600x)

```Probably need to start explaining about Integrated Circuits here```


#1-bit computer



![](https://c1.staticflickr.com/1/693/22351355391_b0efee23d7_b.jpg)

  
In the last case where we add 1+1, the sum (10) requires we carry the 1 over to the next place, the next digit is fed to the AND gate, and the first digit acts like an XOR gate. By combining both logic gates, we can make an adding machine, called a *half adder*. It's called *half* adder because it can only add the first digits. A *full adder* can add higher digits with numbers carrying on from the previous digits. ```this part is going to be easier to understand through illustration```

![](https://farm1.staticflickr.com/774/20812984222_590f7b06e4_b.jpg =600x)
 

```You can click on the switches to see the half adder working, it can add two bits together yielding a two digit binary number.```

The second basic computing operation is data storage, remembering information in bits. We are going to create the most primitive form of computer memory, where an input *set* can turn on or off an LED output, *Q bar*. If the reset switch is then toggled, *switch* is assigned to 1, and next time the *set* is made 1 the LED output will remain lit, even when *set* is no longer pressed.

A latch works by connecting output of the NAND logic gate to input of another NAND logic gate. This is a sequential circuit, in which the output is affected by the input that was previously made. So the two inputs are called *set* and *reset* because they can be used interchangeably. A circuit like this is called a flip-flop. 

![](https://farm6.staticflickr.com/5795/20812986422_ee5529c19d_b.jpg =400x)

The last component, the binary clock, simply switches between zero and one, visible to us as 'LED not lit,' and then 'LED lit.' The period in which the LED blinks, or the clock cycle, is determined by how fast the circuit switches between zero and one. The clock is made possible by utilizing the electrical properties of the specific kinds of NAND logic gate chips (CD4093 or 74132) called the *Schmitt-Trigger* which delays the response time of the logic based on a threshold. By creating a network of variable resistor and capacitor between the input and output of the logic, NAND gate oscillates between Zero and One to produce constant frequency, also know as a clock signal.

![](https://farm6.staticflickr.com/5800/20822480345_604712427c_b.jpg =400x)

[interactive version](http://codepen.io/hxrts/full/NGPLJV/)

[codepen](http://codepen.io/hxrts/pen/NGPLJV/)

```[You can turn the knob to change the frequency.]``` 

![](https://farm1.staticflickr.com/620/20773146321_b0c6b10767_o.jpg =600x)




A *1 Bit Computer* has the fundamental abilities of the traditional computer. It can perfom artithmetic, add two single digit numbers and return a two digit output. It has a clock that creates a square wave oscillation that turns an LED on and off at varying speed. It also has memory, a latch that can store 1-bit of information, zero or one. 

 
![](https://farm6.staticflickr.com/5744/20578210488_c5016e6191_b.jpg =600x)

[Video](https://vimeo.com/136769465)
 
```This version of *1 Bit Computer* is made of NAND logic gates.```


This 1 bit computer uses two TTL NAND logic chips, which are integrated circuits designed to perform NAND operations. The same logic could be implemented with transistors, vacuum tubes, or few lines of code in most programming languages.

Also [how to make Adder, Memory](https://farm8.staticflickr.com/7251/14007688534_adb24c48f8_k.jpg) with the logic gates. 



#Summary

This is how computers work on the conceptual level. However, 1-bit computer can not do alot of useful computation, and it can't even be programmed per se. Thus we need to look at how modern computers use abstraction and repeptition of Logic to make something that is arguably close to Computer".
 


Now we are going to run up and down in the levels of abstraction to the realm of logic. 
 
 
![](https://dl.dropboxusercontent.com/u/53638/abstraction.png)


### Extras

Making process 

- [Pictures](https://www.flickr.com/photos/80913365@N04/20093606613)
- [Teaching](https://www.flickr.com/photos/80913365@N04/20526747300)
-  Binary Logic Worksheet ![](https://farm8.staticflickr.com/7230/13984125176_91ccb45b3a_o.jpg =600x)


And out of NAND logic gates, you can make a 1 bit computer! 
[Here](https://github.com/tchoi8/handmadecomputer/tree/master/Binary/NAND)

[CPU DUMPLING SHOP ⇒](https://github.com/tchoi8/handmadecomputer/blob/master/Dumpling/readme.md)


![](https://c2.staticflickr.com/6/5760/22350581051_2b5ec9f2a1_b.jpg)
![](https://c2.staticflickr.com/6/5621/22153093839_b292654f96_b.jpg)
