 
![](https://farm8.staticflickr.com/7471/15750679268_d0c73f9a5f_o.jpg =600x)  </br>  </br>  </br>  </br>  </br>

Today, when we purchase a new computer one of the specifications we often hear about is the amount of RAM inside. We usually understand more RAM as allowing the computer to do more things at once. But it's different from hard disk space, which is where all the software and data lives.

What is RAM exactly then? RAM stands for random access memory. To help us understand how it works we can think of a parking lot with 8 parking spots. 

![](https://farm4.staticflickr.com/3872/14630594145_edc4ca6e67_o.jpg =600x)
 
The parking lot has a single 1-lane gate that acts as both entrance and exit for the cars. The gate is controlled by a binray clock that's either closed, in the zero state, or open in the one state. There are eight parking spaces because our RAM can store up to 8-bits of information. The input can accept  data, like an empty space accepts cars waiting to enter the parking lot.

However cars can't park in spaces which have already been filled and empty spaces must often be reserved. To prevent cars from attempting to park in a  space that has been filled or reserved, a big display tells incoming cars which spaces are in use.

Once the cars need to leave they can exit the parking lot, erasing the data that's been stored in their parking space. This is achieved by opening the gate and letting the car dive through, thus setting the state of the parking space and the display to zero. Now that parking space is free again to be filled or reserved.

By combining the clock, mux, demux and flipflop we can construct a complete a 8-bit random access memory, where data can be written and read asynchronously. [we may need to clarify this asynchronous statement]

![](https://farm1.staticflickr.com/655/20889869441_19e63ce7cb_o.jpg)

The parking spaces are made of D-type flip-flops. D stands for data and delay which is a type of digital memory like the SR latch we made earlier. This component, however, has an additional input for the clock signal. This is a latch that only changes the flip-flop when the clock input sees the rising edge. Therefore, even when there's a change in the data input, if the clock signal is low, or zero, the flip-flop will not accept the new data. This delay feature also enables the flip-flop to hold data as long as the clock signal remains high, or the address input (which is routed by the DEMUX) has been changed to another flip-flop. [this paragraph gets very technical and it took me a little while to parse the logic. I'm not sure this entire description is necessary, we could probably cut this down and still give the reader the general idea, especially since you want to start moving into this RAM city philosophical portion soon.]
 
![](https://farm1.staticflickr.com/614/20695978869_4907925e5a_o.jpg) 
 
The top line is called the clock which is a persistent wave of high and low, ones and zeros that control the flip-flop. The second line is data, which is an input. At the rising edge of the clock signal A, data is also high which results in Q also being in the high state. At the end of the cycle A, data is Low, but Q remains the same because Q only changes state on the rising edge. This factor enables us to hold the data over time and have it erase at the end of the clock cycle.
 
The gate which controls the entrance and exit of the cars in the parking lot is much like the multiplexer and de-multiplexer, conveniently called MUX and DeMUX.

![](https://farm4.staticflickr.com/3883/14375838297_c42dab45a7_b.jpg =600x)

MUX has many data inputs in addition to several selector inputs. Depending on how the selector inputs (like the thumbs up or thumbs down in the drawing), the input data will be assigned to different places.

![](https://farm6.staticflickr.com/5532/14560631144_30ef4dddc6_b.jpg =600x)

Demux works in the inverse fashion. Demux is composed of an input, four binary switches and many outputs. The combination of thumbs up and thumbs down changes the logic within the demux and routes one input to a possible 16 outputs.

:( "Ok this is too confusing. What does MUX do again?"

![](https://farm6.staticflickr.com/5775/20706120532_578cac3552_b.jpg =600x)

Do you remember the electronic displays at fancy grocery stores which let you know which station is available for check out? It's when there are few lines of people waiting, and the display shows whichever station that's open, and assigns the person in the front of the line to that station and then move to the next line. It's not a perfect analogy because the real multiplexer only has one input, so all the lines would be a single line. However, the part about the displays showing where to go is quiet similar.

![](https://farm3.staticflickr.com/2933/14630595245_7ea41be283_o.jpg =600x)

Wiring the 8 Bit RAM

 ![](https://farm3.staticflickr.com/2918/14642585333_028c3324d5_b.jpg =600x)

On a breadboard, I used 2 D-type Flip-flop chips, one MUX and DEMUX and one 555 timer to generate signal. 

![](https://farm3.staticflickr.com/2900/14626353221_caae6df4e2_o.jpg =600x)

First thing to do is connect the DEMUX to three input swithces A, B and C. The DEMUX also needs to be connected to the clock signal and the data input needs to be connected to all the data inputs of D type flip flops. It's imporatant that the data line is connected to ALL of the inputs of the flip-flops. 
 
![](https://farm4.staticflickr.com/3923/14443190747_86c8f2d880_o.jpg =600x) 

The second step is to connect the DEMUX outputs to all of the clock inputs of the flip-Flops. Now we know that the DEMUX is really assigning the clock's signal to all of the D type flip-flops individually. 
 
![](https://farm4.staticflickr.com/3882/14629137692_c29f415a21_o.jpg =600x)

The third step is to connect the outputs of all individual flip-flops to the MUX. The ouputs are called Q on the flip-flops and it's connected to D0 from D7 on the MUX, 8 bits of information.

![](https://farm4.staticflickr.com/3885/14442989638_2a42bd8375_k.jpg =600x)

The fourth step is to create an oscillator with a 555 Chip. The 555 chip uses a capacitor and resistor similar to the Schimitt-Trigger oscillator we made earlier. We connect the output of the clock to a switch that alternates between a clock signal and READ mode. While on READ mode, the switch is connected to the ground, which means the DEMUX is in passive mode (there might be a more correct way to say this!) and this is how we know if the parking spaces are occupied or not.

And most importantly, we need to connect the output of the MUX into an LED. 

![](https://farm1.staticflickr.com/709/20695472168_71da556ea6_b.jpg =600x)

The [video demonstration](https://vimeo.com/113169467) of 8 bit RAM. 
 
![](https://farm3.staticflickr.com/2925/14444232477_45bef3c378_o.jpg =600x)

When you are wiring this many wires to make an electornics, you are bound to find time to think about a lot of things. I kept on thinking I'm building a tiny city. Each Flip-Flop is an apartment building that's either occupied or vacant. The DEMUX is like a giant terminal that all buses and cars travel through, the connections between logic gates are like tiny roads. Some of these roads are used more frequently like highways, others are local streets that see only occasional traffic.

Around the time I began building my computer, I found a a book of poems about cities by Donna Stonecipher. Here are a few passages, but the whole book continues like this:

**It was like dreaming that you are given the keys to a model city and instantly feeling the burden of ownership, the keys weighing down your coat pocket so severely you start dreaming of giving them back.**

*

**It was like dreaming that you are given the keys to a model city and then you get into your royal blue car and drive out to the outskirts of town to leave the keys on an unoccupied bench overlooking a lake.**

*

**It was like dreaming that you drive back home unburdened, enter your house with its key and sit down with a sigh on your bed, in the quiet and dark, until you notice that the keys to the model city are back in your pocket.**

*

**It was like waking suddenly from the dream, seeing your house key on its hook, and luxuriating in the freedom from keys to model cities — in the deep ease of the haphazard and the habitual, the half-assed.**

From Model City [7] by Donna Stonecipher

![](https://farm1.staticflickr.com/379/18607218102_f45e6d9b0c_o.jpg =600x)

I made a painting of the Random Access City on the studio wall. 

##Extra

- [1] D-Type Flip-Flops can be also made from NAND logic gates.  
![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/D-Type_Transparent_Latch.svg/300px-D-Type_Transparent_Latch.svg.png)

- [2] For detailed explanation of the Mux, refer to this [wiki article](https://en.wikipedia.org/wiki/Multiplexer).

[INTRODCTION ↻](https://github.com/tchoi8/handmadecomputer/blob/master/Entry/readme.md)
