 
![](https://farm8.staticflickr.com/7471/15750679268_d0c73f9a5f_o.jpg =600x)  </br>  </br>  </br>  </br>  </br>

When we are getting a new computer, quiet often we hear about how much RAM is inside of the computer. You can't really fit a lamb inside of a computer, so it must be something different. We usually understand having more RAM means the computer can do more things at the same time. RAM is memory but it's different from Hard disk space in the computer, which is where all the software and data lives. Then, what is RAM exactly? 
It stands for Random Access Memory. We can think of a parking lot with 8 parking spots. 

![](https://farm4.staticflickr.com/3872/14630594145_edc4ca6e67_o.jpg =600x)
 
The Parking lot has one gate that's both entrance and exit for the cars. The gate is controlled by a binray clock that's either closed, on Zero state, or open on One state. There are eight parking spaces because our RAM can store up to 8-bits of Information. The Input can take in  Data, like a car waiting to come in to the parking lot. However the car can not go to a parking space which already has a car on it. To prevent this, the giant display on the back displays if a parking space is occupied or vacant. The cars can get out of the parking lot, which is like erasing the data that's been stored in the specific parking space. It's achieved when the gate is open, Zero (which means no car) is signalled into the Input. The circuit assigns the value of Zero to the Parking space. Now new car can come in to that space. Also the path between the parking space and the gate is really narrow and only one car can come in and out at a time. The combination of clock, mux, demux and flipflops complete a 9-bit Random Access memory, where Data can be written and read asynchronously. 
 </br>
![](https://farm1.staticflickr.com/655/20889869441_19e63ce7cb_o.jpg)

The Parking spaces are made of D-Type flip flops. D stands for Data and Delay and it's a type of digital memory like the SR latch we made earlier. However it has additional input for clock signal. This is a latch that only change the Flip-Flop when the Clock input is on the rising edge. Therefore, even when there's a change in the Data input, if the clock signal is Low, or Zero, the Flip-Flop will not accept the new data. This delay feature also enables the Flip-Flop to hold data as long as the clock signal remains High or the address input (which is routed by the DEMUX) has been changed to another Flip-Flop. 
 
  </br>
 ![](https://farm1.staticflickr.com/614/20695978869_4907925e5a_o.jpg) 
  
 
 The top line is called "Clock" which is a constant wave of High and Low, One and Zeros that control the Flip-Flop. The second line is Data, which is an Input. At the rising edge of the Clock signal A, Data is also High which results in Q being also High. At the end of the cycle A, Data is Low, but Q remains the same because Q only changes state on the rising edge. This factor enables us to hold the data over time and have it erase at the end of the clock cycle. 
 
The gate which controls the entrance and exit of the cars in the parking lok is a lot like the Multiplexer and De-multiplexer, which is conveniently called MUX and DeMUX. 
![](https://farm4.staticflickr.com/3883/14375838297_c42dab45a7_b.jpg =600x)

MUX has many inputs and the selector inputs. Depending on how the selector inputs (like the Thumbs Up or Down in the drawing), the input Data is assigned to different plaaces. 

![](https://farm6.staticflickr.com/5532/14560631144_30ef4dddc6_b.jpg =600x)

Demux works exactly the opposite of Mux. It's made of an input, four binary switches and many outputs. The combination of Thumbs up and down change the logic within the demux and route that one input to 16 outputs. 

 
:(  "Ok this is too confusing. What is MUX do again?" 

</br>
![](https://farm6.staticflickr.com/5775/20706120532_578cac3552_b.jpg =600x)

Do you remember a smart things at a fancy grocery store or airport where the display lets you know which station you should go? It's when there are few lines of people waiting, and the display shows whichever station that's open, and assigns the person in the front of the line to that station and then move to the next line. It's not a perfect analogy because the real multiplexer only has one input, so all the lines would be a single line. However, the part about the displays showing where to go is quiet similar.  
 
 
![](https://farm3.staticflickr.com/2933/14630595245_7ea41be283_o.jpg =600x)
  

Wiring the 8 Bit RAM
  
 ![](https://farm3.staticflickr.com/2918/14642585333_028c3324d5_b.jpg =600x)

On a breadboard, I used 2 D-type Flip-flop chips, one MUX and DEMUX and one 555 Timer to generate signal. 

![](https://farm3.staticflickr.com/2900/14626353221_caae6df4e2_o.jpg =600x)

 First thing to do is connect DEMUX with three input swithces A, B and C. Also it needs to be connected to the Clock signal. Data input needs to be connected to all the Data inputs of D type flip flops. It's imporatant that the Data line is connected to all of the inputs of the Flip-Flops. 
 
![](https://farm4.staticflickr.com/3923/14443190747_86c8f2d880_o.jpg =600x) 

Second step is to connect DEMUX outputs to all of the clock inputs of the Flip-Flops. Now we know that the DEMUX is really assigning the clock's signal to all of the D Type Flip-Flops individually. 
 
![](https://farm4.staticflickr.com/3882/14629137692_c29f415a21_o.jpg =600x)

The third step is to connect the Outputs of all individual Flip-Flops to the MUX. The Ouputs are called Q on the Flip Flops and it's connected to from D0to D7 in the MUX, 8 bits of information.

![](https://farm4.staticflickr.com/3885/14442989638_2a42bd8375_k.jpg =600x)

The fourth step is to create an oscillator with 555 Chip. It's using capacitor and resistor similar to the Schimitt-Trigger oscillator we made earlier. We connect the output of the clock to a switch that alternate between Clock signal and READ mode. On Read mode, the switch is connected to the ground, which means the DEMUX is in passive mode (there might be a more correct way to say this!) and this is how we know if the parking spaces are occupied or not. 

And most importantly, we need to connect the output of the MUX into an LED. 

![](https://farm1.staticflickr.com/709/20695472168_71da556ea6_b.jpg =600x)

The [video demonstration](https://vimeo.com/113169467) of 8 bit RAM. 
 
![](https://farm3.staticflickr.com/2925/14444232477_45bef3c378_o.jpg =600x)

When you are wiring this many wires to make an electornics, you are bound to find time to think about a lot of things. I kept on thinking I'm building a tiny city. Each Flip-Flop is an apartment building that's either occupied or vacant. DEMUX is like a giant terminal that all bus and cars go through, and all the connection between logic gates are like Highways. There are some roads that are used more frequently than others, some for high speed and others which are like more local roads. 

Around that time, I found a a book of poems about cities by Donna Stonecipher. The whole book continues like this. 

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

</br></br></br></br></br></br></br></br></br></br></br>
##Extra

 


- [1] D-Type Flip-Flops can be also made from NAND logic gates.  
![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/D-Type_Transparent_Latch.svg/300px-D-Type_Transparent_Latch.svg.png)

- [2] For detailed explanation of the Mux, refer to this [wiki article](https://en.wikipedia.org/wiki/Multiplexer). 