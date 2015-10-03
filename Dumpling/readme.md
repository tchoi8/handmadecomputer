[⇐ ZERO & ONE / BINARY](https://github.com/tchoi8/handmadecomputer/blob/master/Binary/readme.md)

![](https://farm1.staticflickr.com/586/20286266173_8bfb8c0128_b.jpg =200x)

"Well, that kind of makes sense, right?" 


![](https://farm1.staticflickr.com/696/20719423348_6d895e5e3f_b.jpg =200x)

"Not really..." 

Building the *1 Bit Computer* doesn't yet show us how your laptop or smartphone actually work. Instead, it demonstrates how binary numbers and boolean logic can be configured to create more complex components. On their own these components aren't capable of computing in anything particularly useful, but a computer is said to be [*turing complete*](https://en.wikipedia.org/wiki/Turing_completeness) if it includes *all* of them, at which point it has the extraordinary ability to carry out *any* possible computation.

So how do we get from adding 2 bits together to a system you might be more familiar with? Modern computers are very powerful and can compute millions or billions of bits of information in a fraction of a second, far more than our *1 Bit Computer*. You can still build one of these by assembling the proper hardware and installing the operating system. With some help from the [internet](https://pcpartpicker.com/), or an experienced friend, everyone can buy a CPU, graphics card, RAM and build their own computer. However, today it's rare for people to build their own devices because pre-assembled laptops, desktops, and mobile computers are now so readily accessible. 

There are still a few missing links between our 1-bit toys and the parts you can buy off the shelf. We now know how to perform a binary computation and store the result, but as a user our interest is generally the context in which we perform that computation, the computer program. This is where the most important component of the computer comes in, the CPU (or Central Processing Unit).

The CPUs found in many of our devices today use what's called a *Von Neumann architecture*, named after the mathematician and polymath [John von Neumann](https://en.wikipedia.org/wiki/John_von_Neumann) credited with its invention[2]. A key scientific figure in the Manhattan Project, Von Neumann joined the US Army Ballistic Research Laboratory's program to develop the first electronic general purpose computation device, ENIAC (Electronic Numerical Integrator And Computer), whose initial program was a numerical simulation of the sustained hydrogen fusion reactions needed for second generation nuclear weapons. The ENIAC machine, however, was only programmable through manual switching, which could take weeks of preperation and debugging. This lead Von Neumann and his team to design a second machine, EDVAC (Electronic Discrete Variable Automatic Computer), the first device capable of using a stored-memory program, or what we now call *software*. Though computer technology has advanced dramatically since then, the conceptual framework of the modern CPU has remained largely unchanged since 1945.

![](https://farm6.staticflickr.com/5827/20311593064_44718b69c4_b.jpg =600x)

[Image source](https://en.wikipedia.org/wiki/Von_Neumann_architecture#/media/File:Von_Neumann_Architecture.svg)

The Von Neumann architecture has two major components, the *arithmetic logic unit* (ALU) and a *control unit* which conducts information flow within the ALU. Depending on the program, the control unit may also communicate with the computer memory if given an instruction to do so, after which the result of an arithmetic operation can then be communicated through the output channel. Von Neumann's innovation with this architecture was to allow data and memory to be treated interchangeably, using the software to shape the operational conditions of each computation. This storage functionality, recalling information as an instruction, is what distinguishes the computer from electronic calculators and takes us from our 1-bit computer to a generalized, programmable computer. 

 
"But all this talk is making me hungry. I'm really craving some dumplings!"

![](https://farm1.staticflickr.com/646/20719119500_7c8baf02f1_z.jpg =300x)

At the [School for Poetic Computation](http://sfpc.io/)[1], we like to have dumplings for lunch. C & C Prosperity Dumpling is right around the corner from our space in the Lower East Side. I walk in to the shop super hungry, ready for some sizzling dumplings.

![](https://farm1.staticflickr.com/726/20286138513_9e77baf055_b.jpg =300x)

After looking at the menu, I decide to get pork and chive. I ask the cashier at the counter for 5 boiled dumplings and give her $2. She writes down my order on a piece of paper, drops a few dumpings into the boiling pot, and puts the receipt on the counter next to all the previous orders.

![](https://farm1.staticflickr.com/710/20719118860_dc7ed0b3b2_b.jpg =300x)

The cashier alternates between taking orders from the people in line behind me and packing up orders as they're finished.

While I wait impatiently for my food, I peer into the back to see the chefs making all the dumplings from scratch. There's a person peeling onions, and someone cutting chives.
 
![](https://farm6.staticflickr.com/5747/20899984062_b7d9bd86c1_b.jpg =300x)
 
Another person is folding the dumplings with the filling inside.

![](https://farm1.staticflickr.com/664/20914465181_c424e1e81a_b.jpg =300x)

As a man carries a tray of freshly wrapped dumplings from the kitchen to replace an empty sheet, the woman behind the counter informs him they're running low on vegetable dumplings.

She then scoops a few milk-white packets out of the pot. I wonder if that might be my order...
 
![](https://farm1.staticflickr.com/691/20286546343_58ed41741b_b.jpg =300x)

A moment later she yells my number, packs everything into a container, and hands it to me.
 
![](https://farm6.staticflickr.com/5788/20720686570_9025eb3d88_b.jpg =300x)

Oh yeah! Dumpling time!

![](https://farm1.staticflickr.com/578/20909824495_8d0b39aa90_b.jpg =300x)

While I eat, I think about how the dumpling shop is a useful metaphor for understanding the central processing unit. 

![](https://farm6.staticflickr.com/5773/20825301555_0ecf439c0a_b.jpg =600x)

At the CPU Dumpling Shop, whenever a customer orders food their order is considered a single instruction set. The customer communicates this input the cashier (CU), who organizes the instructions and passes orders to the kitchen (ALU) about what dumplings to make as needed.

While the employees all know how to perform a variety of tasks, the chef knows recipes for several types of dumplings and the cashier knows where to find extra takeout containers, they don't need to continually think about every step of each task. Instead, they concentrate on single procedure, or program, recalling the information required for other tasks only when they receive a new instruction. They remember where ingredients are stored and how to make different recipes by storing them in their long term memory whereas a single customer's order is only held in their working memory for a few minutes and then forgetten.

![](https://farm1.staticflickr.com/743/20774209011_a520def1b5_o.jpg =300x)

####Finite-state machine

![](https://farm6.staticflickr.com/5715/20893802212_7ed4646651_h.jpg =600x)

This device is named "Finite-state machine"[2] because the entirety of its possible operation is limited to a finite number of configurations or memory states. I built it to better understand the CPU's important components.

#####Input & Output

The four buttons in the front are the inputs which you can use to enter four bits of information. If the button is pressed, the information is 1 or High and an LED right in front of the button lights up immediately.

The four LEDs on the back are the outputs. This is where information stored in the the RAM (Random Access Memory) is made visible. It's the visual output for the finite state machine.  

#####RAM 
The RAM is a [74189 chip](http://pdf.datasheetcatalog.com/datasheet/fairchild/74F189.pdf), 64-Bit Random Access Memory. More on the nature of RAM on the next chapter on the [RAM City](https://github.com/tchoi8/handmadecomputer/tree/master/RAMcity). 
The small red switch on the left enables you to select between reading or writing the data from the input to the RAM. When the switch is in writing mode, status of the switches (either on and off) is recorded on the RAM as four bits of information. 

 
  
#####Counter
The small yellow switch on the right controls the counter which counts from zero to nine, ten states where four bits of information can be recorded. When the switch is toggled, the number decreases from nine to zero. 
 
The blue button next to the Counter control is a load. If this switch is enabled, you can load the information stored in the RAM. This is possible by switching on and off the load switches behind the chip. The binary information from the switches gives you a random access to the information the R.A.M. When it's not on the load mode, the RAM can cycle through the ten steps. 

The Finite-state machine demonstrates how the instructions and information are stored in memory. However it doesn't explain how the computer calculates information, or to continue with our dumpling metaphor, how the chef actually cooks the dumplings. The mathematical and logical operations are made possible with the ALU, which stands for Arithmetic Logic Unit. 

![](https://farm6.staticflickr.com/5795/20876342206_4c0a7dcde4_b.jpg =600x)
 
The ALU is responsible for all mathematics and logical operations, like comparing two bits of information, multiplying, or subtracting. It performs all artithmetic calculations and logical decisions. Since computers only think and speak in binary numbers, ALU also only deals with the truth or falsity of operations.  

![](https://farm6.staticflickr.com/5626/20313162303_a0112be8ff_b.jpg =600x)

[Image source](https://commons.wikimedia.org/wiki/File:74181aluschematic.png) 

 

What's really fascinating about the ALU and the computers in general is that they are made for binary logic gates. ALU, which performs complex operations is still made of basic logic gates, as you as see on the diagram above. It looks like a busy street in the city. 

![](https://farm6.staticflickr.com/5696/20364771063_4c0aa7f838_b.jpg =600x)

When the chef grills dumplings on the pan, or packs up the cooked food, he's acting like the control unit. The control unit is in charge of coordination the operation of all the other components. It is the in charge of signalling the hardware devieces to to execute instructions. The ALU and the control unit together make up the CPU. 

[Video of ALU construction and demonstration](https://vimeo.com/136831074)


![](https://dl.dropboxusercontent.com/u/53638/infoflow.jpg)

ALU and Memory is only a part of what makes CPU. Many more machines are interconnected to make up a computer. Instruction register, memory address registers and other units make up the datapath.  The arrows connecting all of them are like highways connecting a city to another city. 

In the next chapter, we will look into the Random Access Memory more closely to see the parallel between computer architecture and urban space. 

###Extra 

- [1] [School for Poetic Computation](http://sfpc.io) is a an artist run school that I cofounded in 2013 to teach and learn code, hardware and theory.  
- [2] [Von Neumann architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture)
- [2] [Finite State Machine](https://github.com/tchoi8/handmadecomputer/tree/master/FSM) is actually a conceptual term for computational architecture.    
- Also [Turing](https://github.com/tchoi8/handmadecomputer/tree/master/Turing)'s Universal Machine is an important concept. 
 
[RAM CITY ⇒](https://github.com/tchoi8/handmadecomputer/blob/master/RAMcity/readme.md)
