# 1. Introduction

![](https://c2.staticflickr.com/6/5764/22013480432_3f3cf9ea77_b.jpg=600x)
![](https://c1.staticflickr.com/1/589/21402894434_3125c39431_b.jpg=600x)

![](https://dl.dropboxusercontent.com/u/53638/phone.jpg)

[1]

![](https://dl.dropboxusercontent.com/u/53638/present.jpg)

[2]


![](https://c1.staticflickr.com/1/613/22013727102_f7278f02c1_b.jpg)

 ![](https://c2.staticflickr.com/6/5621/21838167168_029bf6e244_b.jpg =600x)
![](https://farm6.staticflickr.com/5714/20769983945_476766792e_b.jpg =600x)
![](https://dl.dropboxusercontent.com/u/53638/intricate.jpg)

 
## Reference

[1] There are many ways of defining a computer other than the desktop, laptop, or smartphone. The "computer," on a fundamental level is a tool that can do mathematical operations like add and multiply, remember information and follow instructions. 

The first computers were human. In fact, we get the term "computer" from the outmoded practice of human computation, peoples whose profession was the performance of arithmetic for scientific, logistical, or military production.

[2] There is a silicon valley mythology that centers around protagonists like Jobs, Wozniak, the legend of innovation. But what's left out of this glossy narrative are parallel stories about militarization, state power, and mass production, which not only financed, but provided the right political conditions for the computer's invention.

Before computers became personal, they were used as tools for scientific research and engineering, as technologies to scale growing electronic communication systems and as machines for war.

Manuel DeLanda in *War in the Age of Intelligent Machines* chronicles the development of computational technology and theory from the perspective of military operations.

# 2. Interface

![](https://c2.staticflickr.com/6/5697/22228829805_1ef410a9de_b.jpg)
![](https://dl.dropboxusercontent.com/u/53638/tablet.jpg)
![](https://c1.staticflickr.com/1/761/22041074988_75fa31b7f0_b.jpg)
![](https://c1.staticflickr.com/1/567/22042008679_df0a1c965f_b.jpg)
![](https://dl.dropboxusercontent.com/u/53638/laptop.jpg)
![](https://c1.staticflickr.com/1/724/22042007159_e7a733dd75_b.jpg)
![](https://c2.staticflickr.com/6/5812/21607865113_2a1f05d3cf_b.jpg)

```black box image here?```

But setting aside the computing industry's privatization of technical knowledge for a moment, the complexities of the modern computer can be broadly understood as the product of only a few basic operations repeated and abstracted.

![](https://dl.dropboxusercontent.com/u/53638/abstraction.jpg)

Both art and computation are often made opaque because access is equated with power. But just like the painting, stepping inside the computer may be easier than you think.

```open computer image here?```

Opening the computer we find lots of small electronic components and a circuit board that connects them together. This is an image of a microchip from 1963 at 100x magnification.

![](https://farm6.staticflickr.com/5652/20858537691_ebe368b805_o.jpg =400x)

```resistor-transistor flip-flop logic [1]```

Micrograph photos reveal the unique visual patterns of the computer's interior circuitry. Designed to maximize electronic performance at infinitesimal scale, they can also be quite geometrically appealing.

But when I look at images like these I see artworks.

![](https://farm4.staticflickr.com/3845/18745549829_6d22d7e788_z.jpg =400x)

Artworks like this painting by [Peter Halley](http://www.peterhalley.com/) titled *Instant City*[2]. Halley's works not only remind me of microchip designs but many other computer design patterns. In fact the term "design pattern" was introduced to computer scientists by an architect and design theorist Christopher Alexander. We'll touch on one design pattern in particular, the von Neumann architecture, in more detail when we get to the [CPU Dumpling Shop](https://github.com/tchoi8/handmadecomputer/tree/master/Dumpling) chapter coming up.

I often find surprising connections between art and computation. Conceptual artists, for instance, were interested in more than just the formal qualities of the painting, such as color and shape. They were also attentive to the systems in which their work was created. Their working process emphasized making *programs*, sets of instructions that, when executed, resulted in both a performative action and production of the artwork.
 
![](https://farm6.staticflickr.com/5823/20813920292_f172897655_b.jpg =600x)

Paintings and books all make use of repetition. Layering shapes or wires or pages, the composition and logic of which allow them to function as a whole.
 
This phrase "Each one comes to be a whole one to me" is from *The Making of Americans* by Gertrude Stein. I opened a random page in the book and picked this line, so it could just have been any other phrase. In this book, a story is told and retold in many ways. The result is a fragmented narrative with multiple perspectives. 

![](https://farm1.staticflickr.com/679/20823369765_30e3a61dd6_b.jpg =600x)

Making a computer and building electronic circuits feels like building a tiny city. The circuit board is a little urban architecture and its inhabitants a busy traffic of electronic signals. Just like cities, memories are made and remembered in the buildings and roads connecting them.

![](https://farm4.staticflickr.com/3940/15752018125_41037ef0c6_b.jpg =600x)
 
We are now going to make a window into this city and peer into the world of zero and one.

![](https://farm8.staticflickr.com/7541/15566849007_edcf431bec_b.jpg =600x)

We will build a 1-bit computer in the future chapter with electronics. 

##References 
- [1] Stan Augarten, State of the Art, http://smithsonianchips.si.edu/augarten/index.htm 
- [2] Peter Halley, Instant City, 1996, Acrylic, Day-Glo acrylic, Metallic acrylic &
Roll-a-Tex on canvas 58 x 93 inches

#3. Zero and One

##What is a Computer?

"Now let's make a computer! Wait, what is a computer?

Well, that's a little difficult to explain, even for experts, but let's start by giving an ostensible definition, specifying a system which can "compute" something.

Ok... but what does it mean to be "computed"?

Oddly enough, the widely accepted meaning of a [computable talk](https://en.wikipedia.org/wiki/Computable_function) is the intuitive one: an operation which is capable of being reliably carried out by a machine according to a specific sequence of instructions or algorithm. If that seems circular, it's because the fundemental limits of computation are still largely unknown (and potentially unknowable), therefore any axiomatic description of universal computation remains hypothetical.

But we see algorithms all around us, repeated patterns of action and process. Surely we can describe some of these mechanisms?

Alan Turing's work prior to WWII was focused on this very question. Turing developed a framework which he called automatic machines, known today as *turing machines*, to encode mechanistic processes as general symbolic expressions.

Turing along with Alonzo Church, the creator of λ-calculus, concurrently [postulated](https://en.wikipedia.org/wiki/Church%E2%80%93Turing_thesis) that the set of all automatic machines had equivalent functional capabilities. In affect, that the operation of any computing mechanism could be replicated by a turing machine, thus formalizing the notion of *turing completeness* and offering von Neumann an opening to build his stored-program computer.

The Turing Machine which fed an arbitrary length of ticker tape with a series of discrete symbols through a reading window, looked up the symbol in the reading frame, and replaced it with the resulting symbol, isn't suitable for practical computation.

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
   
 
##4. Binary logic 

``` Break from the technical details, change tones slightly. Brief mention of Claude Shannon's paper on switching circuits and George Boole' logic. Explain Binary with Thumbs up & down and Venn Diagram. Also introduce Integrated Circuit and the idea of abstraction here.``` 

Before we get into the details of *1 Bit Computer*, let's return to the idea of zero and one, binary numbers, and their boolean logic.

NAND is short for *not* AND logic. Here A and B are inputs, either of which can be zero or one, and Y is the logical output. In the venn diagram above, depicting possible input state configurations, every shape is colored except the intersecting region. This means the result is true in every case *except* when both inputs are true.  
 ![](https://c1.staticflickr.com/1/613/21839648508_2346bd533a_o.jpg =600x)

It's exhauting to go through these logic stuff, but believe me, it's like climbing a mountain. You will get a great view in the end!

![](https://dl.dropboxusercontent.com/u/53638/mountain.jpg)
 
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

##1-bit computer

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

##Summary

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

![](https://c2.staticflickr.com/6/5760/22350581051_2b5ec9f2a1_b.jpg)
![](https://c2.staticflickr.com/6/5621/22153093839_b292654f96_b.jpg)

#4. Dumpling Shop

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

- the drawing will need to clarify that the cashier is also cooking. or just delivering orders 

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

 - this drawing will need edit, CU and ALU will swap. CU gives orders to the kitchen and translates 
 - ALU is the kitchen tool that actually do the cooking, arithmetics and logical operations. 
 

While the employees all know how to perform a variety of tasks, the chef knows recipes for several types of dumplings and the cashier knows where to find extra takeout containers, they don't need to continually think about every step of each task. Instead, they concentrate on single procedure, or program, recalling the information required for other tasks only when they receive a new instruction. They remember where ingredients are stored and how to make different recipes by storing them in their long term memory whereas a single customer's order is only held in their working memory for a few minutes and then forgetten.

![](https://farm1.staticflickr.com/743/20774209011_a520def1b5_o.jpg =300x)

YOYO

- Honest recount here. of "There are the correct ways of building CPU from electronics. I looked at them and I got interested in some elements of it. focusing on RAM and Counter and ALU. This is as far as I got."
- not call this machine FSM, but use parts of it to explain how CPU's work in electronical level. 

How does the CPU actually operate? We can begin to explore the CPU by making a compute that's good at remembering and executing simple instructions. 

This device is named "Finite-state machine"[2] because the entirety of its possible operation is limited to a finite number of configurations or memory states. I built it to better understand several of the CPU's important components.

![](https://farm6.staticflickr.com/5715/20893802212_7ed4646651_h.jpg =600x)

The four buttons in the front are the inputs which you can use to enter four bits of information. Pressing a button sets that input to 1 or *high* and the corresponding LED lights up immediately. The other four LEDs on the back are outputs, where machine-state information stored in the RAM (Random Access Memory) is displayed.  

The small red switch on the left (with a sticker labled Read/Write RAM) enables you to select between two modes, reading mode to store a 4-bit input state to memory, and output mode to read the stored memory state. We'll go into the nature of RAM a bit more in the next chapter [RAM City](https://github.com/tchoi8/handmadecomputer/tree/master/RAMcity).

The counter tots up from from zero to nine: ten sequential memory blocks for recording a 4-bit state. Once recorded in reading mode, the binary information stored in memory can be accessed arbitrarily (randomly) via its address on the RAM chip.

The finite-state machine demonstrates how information is stored in memory but we still need one thing to complete the CPU, the computation. To continue with our dumpling metaphor, we know how to make dumplings but we don't have a kitchen. The logic function is made possible with the ALU or Arithmetic Logic Unit. 
 
 ![](https://farm6.staticflickr.com/5696/20364771063_4c0aa7f838_b.jpg =600x)
 
 [Video of ALU construction and demonstration](https://vimeo.com/136831074)
 
The ALU is responsible for all arithmetic operations such as addition and multiplication. However, since computers only think and speak with binary numbers, the ALU builds these arithmatic functions by computing the truth or falsity a particular state, comparing bits of information according to a particular boolean logic as we practiced in the previous section. This is the fascinating thing about computers: despite the many sophisticated ways we use them, the entirety of their function still reduces to the interplay of simple gate-logic.

![](https://farm6.staticflickr.com/5795/20876342206_4c0a7dcde4_b.jpg =600x)

Complex logic circuits look a lot like busy city streets. 

![](https://farm6.staticflickr.com/5626/20313162303_a0112be8ff_b.jpg =600x)

- draw this by hand

[Image source](https://commons.wikimedia.org/wiki/File:74181aluschematic.png)

The modern computer includes many other interconnected machines: instruction registers, memory address registers, cache systems and processes scheduler units, but the CPU described above captures the general the system logic. The datapaths between these machines are like highways connecting one city to another.

![](https://dl.dropboxusercontent.com/u/53638/infoflow.jpg)

###Extra 

- [1] [School for Poetic Computation](http://sfpc.io) is a an artist run school that I cofounded in 2013 to teach and learn code, hardware and theory.  
- [2] [Von Neumann architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture)
- [2] [Finite State Machine](https://github.com/tchoi8/handmadecomputer/tree/master/FSM) is actually a conceptual term for computational architecture.    
- Also [Turing](https://github.com/tchoi8/handmadecomputer/tree/master/Turing)'s Universal Machine is an important concept. 

#5. RAM City

- Transition to City metaphors by an introductory drawing
- Zooming out from the dumpling shop, the whole city, the whole computer 
- driving in from the desert, the city comes closer and closer ( maybe reference the Poetry here, or choose Calvino's episode?)
- try to park
- there's a small logical blindspot with the parking lot metaphor 
- simplify mux/ demux
- focus on the question "What is similar about cities and computers"
- Here, we return to what kind of computer do we want to build? what kind of city do we want to live in?
- Occupy, open space and etc 
- Last drawing - square wave, and wave forms 

What is RAM exactly? RAM stands for Random Access Memory. To help us understand how RAM works let's imagine a parking lot with 8 spaces representing 8-bits of information.

![](https://farm4.staticflickr.com/3872/14630594145_edc4ca6e67_o.jpg =600x)
 
Our lot has a single gated lane for cars, acting both as entrance and exit. The gate can either be closed or open to let a car pass. To ensure only one car travels through at a time, we have a timing system consisting of a clock – same as we used in the finite-state machine – and a queue for cars coming and going. When accepting a new car we want to need to tell them where to park, which we do with a big numbered display. If we want to read the saved data we can simply look at the state of the parking spaces. 

The RAM we can construct on a circuit board is quite similar, here I made 8-bit random access memory by combining the clock, mux, demux and flip-flop. There, data can be written and read asynchronously, which means the data can be kept independent of the clock cycle.

![](https://farm1.staticflickr.com/655/20889869441_19e63ce7cb_o.jpg)

The parking spaces are made of D-type flip-flops which is a type of digital memory like the SR latch we made earlier. This component, however, has an additional input for the clock signal. This is a latch that only changes the flip-flop when the clock input sees the rising edge. Therefore, if the clock signal is low, or zero, the flip-flop will not accept the new data. This delay feature also enables the flip-flop to hold data as long as the clock signal remains high. So we can store it in memory and call it up as long as the circuit is connected to the power. 
 
![](https://farm1.staticflickr.com/614/20695978869_4907925e5a_o.jpg) 
 
CLK on the top line stands for the clock which is a persistent wave of Ones and Zeros that control the flip-flops. The second line is DATA, which is an input. Q is the Data that's stored in the memory during the clock cycle.  
 
![](https://farm4.staticflickr.com/3883/14375838297_c42dab45a7_b.jpg =600x)

MUX has many data inputs in addition to several selector inputs. Depending on how the selector inputs (like the thumbs up or thumbs down in the drawing), the output will be assigned to different inputs.

![](https://farm6.staticflickr.com/5532/14560631144_30ef4dddc6_b.jpg =600x)

Demux works in the inverse fashion. Demux is composed of an input, binary switches and many outputs. The combination of thumbs up and thumbs down changes the logic within the demux and routes one input to a possible 16 outputs.
 
![](https://farm3.staticflickr.com/2933/14630595245_7ea41be283_o.jpg =600x)

The principle operation of RAM is made possible with the mux and demux, which is the gate that controls the cars coming in and out of the parking lot spaces (flip-flops). 
 
![](https://farm3.staticflickr.com/2918/14642585333_028c3324d5_b.jpg =600x)

On a breadboard, I used 4 D-type flip-flop logic gates, one MUX and DEMUX and one 555 timer to generate signal. The LEDs indicate output status of each flip-flop as well as the RAM's output. 
 
![](https://farm4.staticflickr.com/3885/14442989638_2a42bd8375_k.jpg =600x)

When you are wiring this many wires to make an electornics, you are bound to find time to think about a lot of things. I kept on thinking I'm building a tiny city. Each Flip-Flop is an apartment building that's either occupied or vacant. The DEMUX is like a giant terminal that all buses and cars travel through, the connections between logic gates are like tiny roads. Some of these roads are used more frequently like highways, others are local streets that see only occasional traffic. 

![](https://farm1.staticflickr.com/709/20695472168_71da556ea6_b.jpg =600x)

The [video demonstration](https://vimeo.com/113169467) of 8 bit RAM. 

Around the time I began building my computer, I found a a book of poems about cities by Donna Stonecipher. Here are a few passages, but the whole book continues like this: 

```
It was like dreaming that you are given the keys to a model city and instantly feeling the burden of ownership, the keys weighing down your coat pocket so severely you start dreaming of giving them back.

*

It was like dreaming that you are given the keys to a model city and then you get into your royal blue car and drive out to the outskirts of town to leave the keys on an unoccupied bench overlooking a lake.

*

It was like dreaming that you drive back home unburdened, enter your house with its key and sit down with a sigh on your bed, in the quiet and dark, until you notice that the keys to the model city are back in your pocket.

*

It was like waking suddenly from the dream, seeing your house key on its hook, and luxuriating in the freedom from keys to model cities — in the deep ease of the haphazard and the habitual, the half-assed.
```

From Model City [7] by Donna Stonecipher [4] 

![](https://farm8.staticflickr.com/7471/15750679268_d0c73f9a5f_o.jpg =600x)

Much like how the cities in Stonecipher's poem builds itself and then vanishes, the computers remembers data into its memory and then deletes it constantly. That's the nature of RAM city where the buildings are occupied and then deserted over night, all governed by the clock and data that signals everyone's movement.  

##Reference 

- [1] D-Type Flip-Flops can be also made from NAND logic gates.   
- [2] For detailed explanation of the Mux, refer to this [wiki article](https://en.wikipedia.org/wiki/Multiplexer).
- [3] How to make 8-Bit RAM circuit. Step by Step instruction.  ```[will linnk to a tutorial and leave most of the technical details there]``` 
- [4] From Model City [7] by Donna Stonecipher
 
##End note
 
![](https://farm1.staticflickr.com/710/20421656493_a9f3d6a5c9_b.jpg =600x)

Hand making circuits is an act of love, love for the ideas that the computer has come to embody. It is a practice devoted to the history and craft of computation, one that's taught me a great respect for the material and form. There is an elegance in the abstraction and repetition of computational logic that I can only describe as 'beautiful.'

![](https://farm1.staticflickr.com/777/21016448716_dda5517174_b.jpg =600x)

Overlooking the importance of our relationship to the computers and choosing consumption over construction is the path of least resistance. Recent events highlight the effect of our ambivalence, drone technology which often takes away human agency in warfare, government and private agencies infringing on our privacy in the name of security, corporate information technology monopolies jeopardize political and ethical neutrality. When our lives are so profoundly affected by algorithms and programs, what are acts of resistance or dissent that preserve our morality, our humanity?

Nam June Paik wrote “… Karma is samsara. Relationship is metempsychosis. We are in open circuits" [1] I wonder what he meant by "We are in open circuits"? Did he mean a circuit of information? I think we try to close these circuits by striving to master the technologies of our time. But maybe we can also become part of the circuit. Imprint ourselves into the spaces we occupy and dispurse our memories across the people we touch. We are open circuits, we are open city.

![](https://farm1.staticflickr.com/744/21033033342_99373b5f53_b.jpg =600x)

**Reference**

- [1] Manifestos, Great Bear Pamphlets, Something Else Press, 1966).
