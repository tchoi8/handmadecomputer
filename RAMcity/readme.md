[⇐ DUMPLING SHOP](https://github.com/tchoi8/handmadecomputer/blob/master/Dumpling/readme.md)


What is RAM exactly? RAM stands for Random Access Memory. To help us understand how RAM works let's imagine a parking lot with 8 spaces representing 8-bits of information.

![](https://farm4.staticflickr.com/3872/14630594145_edc4ca6e67_o.jpg =600x)
 
Our lot has a single gated lane for cars, acting both as entrance and exit. The gate can either be closed or open to let a car pass. To ensure only one car travels through at a time, we have a timing system consisting of a clock – same as we used in the finite-state machine – and a queue for cars coming and going. When accepting a new car we want to need to tell them where to park, which we do with a big numbered display. If we want to read the saved data we can simply look at the state of the parking spaces. 

The RAM we can construct on a circuit board is quite similar, here I made 8-bit random access memory by combining the clock, mux, demux and flip-flop. There, data can be written and read asynchronously, which means the data can be kept independent of the clock cycle.

![](https://farm1.staticflickr.com/655/20889869441_19e63ce7cb_o.jpg)

The parking spaces are made of D-type flip-flops which is a type of digital memory like the SR latch we made earlier. This component, however, has an additional input for the clock signal. This is a latch that only changes the flip-flop when the clock input sees the rising edge. Therefore, if the clock signal is low, or zero, the flip-flop will not accept the new data. This delay feature also enables the flip-flop to hold data as long as the clock signal remains high. So we can store it in memory and call it up as long as the circuit is connected to the power.   ```[yep. gave a try in minimizing the tech]``` 
 
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


**Reference** 

- [1] D-Type Flip-Flops can be also made from NAND logic gates.   
- [2] For detailed explanation of the Mux, refer to this [wiki article](https://en.wikipedia.org/wiki/Multiplexer).
- [3] How to make 8-Bit RAM circuit. Step by Step instruction.  ```[will linnk to a tutorial and leave most of the technical details there]``` 
- [4] From Model City [7] by Donna Stonecipher
 
 
#End note
 
![](https://farm1.staticflickr.com/710/20421656493_a9f3d6a5c9_b.jpg =600x)


Hand making circuits is an act of love, love for the ideas that the computer has come to embody. It is a practice devoted to the history and craft of computation, one that's taught me a great respect for the material and form. There is an elegance in the abstraction and repetition of computational logic that I can only describe as 'beautiful.'

![](https://farm1.staticflickr.com/777/21016448716_dda5517174_b.jpg =600x)

Nam June Paik wrote “… Karma is samsara. Relationship is metempsychosis. We are in open circuits" [1] I wonder what he meant by "We are in open circuits"? Did he mean a circuit of information? I think we try to close these circuits by striving to master the technologies of our time. But maybe we can also become part of the circuit. Imprint ourselves into the spaces we occupy and dispurse our memories across the people we touch. We are open circuits, we are open city.

![](https://farm1.staticflickr.com/744/21033033342_99373b5f53_b.jpg =600x)

**Reference**

- [1] Manifestos, Great Bear Pamphlets, Something Else Press, 1966).  

 

[INTRODCTION ↻](https://github.com/tchoi8/handmadecomputer/blob/master/Entry/readme.md)
