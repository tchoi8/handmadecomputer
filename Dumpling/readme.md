[⇐ ZERO & ONE / BINARY](https://github.com/tchoi8/handmadecomputer/blob/master/Binary/readme.md)

![](https://c1.staticflickr.com/1/757/21579674474_0f54bf3373_b.jpg =600x)
 

Building the *1 Bit Computer* doesn't yet show us how your laptop or smartphone actually work. Instead, it demonstrates how binary numbers and boolean logic can be configured to create more complex components. On their own these components aren't capable of computing in anything particularly useful, but a computer is said to be [*turing complete*](https://en.wikipedia.org/wiki/Turing_completeness) if it includes *all* of them, at which point it has the extraordinary ability to carry out *any* possible computation.

So how do we get from adding 2 bits together to a system you might be more familiar with? Modern computers are very powerful and can compute millions or billions of bits of information in a fraction of a second, far more than our *1 Bit Computer*. You can still build one of these by assembling the proper hardware and installing the operating system. With some help from the [internet](https://pcpartpicker.com/), or an experienced friend, everyone can buy a CPU, graphics card, RAM and build their own computer. However, today it's rare for people to build their own devices because pre-assembled laptops, desktops, and mobile computers are now so readily accessible. 

There are still a few missing links between our 1-bit circuits and the parts you can buy off the shelf. We now know how to perform a binary computation and store the result, but as a user our interest is generally the context in which we perform that computation, the computer program. This is where the most important component of the computer comes in, the CPU (or Central Processing Unit).

The CPUs found in many of our devices today use what's called a *Von Neumann architecture*, named after the mathematician and polymath [John von Neumann](https://en.wikipedia.org/wiki/John_von_Neumann) credited with its invention[2]. A key scientific figure in the Manhattan Project, Von Neumann joined the US Army Ballistic Research Laboratory's program to develop the first electronic general purpose computation device, ENIAC (Electronic Numerical Integrator And Computer), whose initial program was a numerical simulation of the sustained hydrogen fusion reactions needed for second generation nuclear weapons. The ENIAC machine, however, was only programmable through manual switching, which could take weeks of preperation and debugging. This lead Von Neumann and his team to design a second machine, EDVAC (Electronic Discrete Variable Automatic Computer), the first device capable of using a stored-memory program, or what we now call *software*. Though computer technology has advanced dramatically since then, the conceptual framework of the modern CPU has remained largely unchanged since 1945.

![](https://c1.staticflickr.com/1/694/22177320676_f03d5251ce_b.jpg =600x)

[Image source](https://en.wikipedia.org/wiki/Von_Neumann_architecture#/media/File:Von_Neumann_Architecture.svg)

The Von Neumann architecture has two major components, the *arithmetic logic unit* (ALU) and a *control unit* which conducts information flow within the ALU. Depending on the program, the control unit may also communicate with the computer memory if given an instruction to do so, after which the result of an arithmetic operation can then be communicated through the output channel. Von Neumann's innovation with this architecture was to allow data and memory to be treated interchangeably, using the software to shape the operational conditions of each computation. This storage functionality, recalling information as an instruction, is what distinguishes the computer from electronic calculators and takes us from our 1-bit computer to a generalized, programmable computer. 


![](https://c1.staticflickr.com/1/608/22017554949_1f952e59a7_b.jpg =600x)

At the [School for Poetic Computation](http://sfpc.io/)[1], we like to have dumplings for lunch. C & C Prosperity Dumpling is right around the corner from our space in the Lower East Side. I walk in to the shop super hungry, ready for some sizzling dumplings.

![]( https://c2.staticflickr.com/6/5654/22189741202_4e893c6a29_b.jpg =300x)

After looking at the menu, I decide to get pork and chive. I ask the cashier at the counter for 5 boiled dumplings and give her $2. She writes down my order on a piece of paper, drops a few dumpings into the boiling pot, and puts the receipt on the counter next to all the previous orders.

![](https://farm1.staticflickr.com/710/20719118860_dc7ed0b3b2_b.jpg =300x)

The cashier alternates between taking orders from the people in line behind me and packing up orders as they're finished.

 
 
![](https://c1.staticflickr.com/1/704/22015717730_5f6b6f5e1f_b.jpg =600x)

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

![](https://c1.staticflickr.com/1/618/22191467572_b5cfdc230a_b.jpg =600x)

At the CPU Dumpling Shop, whenever a customer orders food their 1order is considered a single instruction set. The customer communicates this input the cashier (CU), who organizes the instructions and passes orders to the kitchen (ALU) about what dumplings to make as needed.

![](https://farm6.staticflickr.com/5773/20825301555_0ecf439c0a_b.jpg =600x)

 

While the employees all know how to perform a variety of tasks, the chef knows recipes for several types of dumplings and the cashier knows where to find extra takeout containers, they don't need to continually think about every step of each task. Instead, they concentrate on single procedure, or program, recalling the information required for other tasks only when they receive a new instruction. They remember where ingredients are stored and how to make different recipes by storing them in their long term memory whereas a single customer's order is only held in their working memory for a few minutes and then forgetten.

![](https://farm1.staticflickr.com/743/20774209011_a520def1b5_o.jpg =300x)

####Finite-state machine

This device is named "Finite-state machine"[2] because the entirety of its possible operation is limited to a finite number of configurations or memory states. I built it to better understand several of the CPU's important components.

![](https://farm6.staticflickr.com/5715/20893802212_7ed4646651_h.jpg =600x)

The four buttons in the front are the inputs which you can use to enter four bits of information. Pressing a button sets that input to 1 or *high* and the corresponding LED lights up immediately. The other four LEDs on the back are outputs, where machine-state information stored in the RAM (Random Access Memory) is displayed.  

The small red switch on the left enables you to select between two modes, reading mode to store a 4-bit input state to memory, and output mode to read the stored memory state. We'll go into the nature of RAM a bit more in the next chapter [RAM City](https://github.com/tchoi8/handmadecomputer/tree/master/RAMcity).

The counter counts up from from zero to nine: ten sequential memory blocks for recording a 4-bit state. Once recorded in reading mode, the binary information stored in memory can be accessed arbitrarily (randomly) via its address on the RAM chip.

The finite-state machine demonstrates how information is stored in memory but we still need one thing to complete the CPU, the computation. To continue with our dumpling metaphor, we know how to make dumplings but we don't have a kitchen. The logic function is made possible with the ALU or Arithmetic Logic Unit. 
 
 ![](https://farm6.staticflickr.com/5696/20364771063_4c0aa7f838_b.jpg =600x)
 
 [Video of ALU construction and demonstration](https://vimeo.com/136831074)
 
The ALU is responsible for all arithmetic operations such as addition and multiplication. However, since computers only think and speak with binary numbers, the ALU builds these arithmatic functions by computing the truth or falsity a particular state, comparing bits of information according to a particular boolean logic as we practiced in the previous section. This is the fascinating thing about computers: despite the many sophisticated ways we use them, the entirety of their function still reduces to the interplay of simple gate-logic.

![](https://farm6.staticflickr.com/5795/20876342206_4c0a7dcde4_b.jpg =600x)

Complex logic circuits look a lot like busy city streets. 

![](https://farm6.staticflickr.com/5626/20313162303_a0112be8ff_b.jpg =600x)

[Image source](https://commons.wikimedia.org/wiki/File:74181aluschematic.png)

The modern computer includes many other interconnected machines: instruction registers, memory address registers, cache systems and processes scheduler units, but the CPU described above captures the general the system logic. The datapaths between these machines are like highways connecting one city to another.

![](https://dl.dropboxusercontent.com/u/53638/infoflow.jpg)

###Extra 

- [1] [School for Poetic Computation](http://sfpc.io) is a an artist run school that I cofounded in 2013 to teach and learn code, hardware and theory.  
- [2] [Von Neumann architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture)
- [2] [Finite State Machine](https://github.com/tchoi8/handmadecomputer/tree/master/FSM) is actually a conceptual term for computational architecture.    
- Also [Turing](https://github.com/tchoi8/handmadecomputer/tree/master/Turing)'s Universal Machine is an important concept. 
 
[RAM CITY ⇒](https://github.com/tchoi8/handmadecomputer/blob/master/RAMcity/readme.md)
