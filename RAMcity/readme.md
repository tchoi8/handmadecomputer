 
![](https://farm8.staticflickr.com/7471/15750679268_d0c73f9a5f_o.jpg =600x)  </br>  </br>  </br>  </br>  </br>

Today, when we purchase a new computer one of the specifications we often hear about is the amount of RAM inside. We usually understand more RAM as allowing the computer to do more things at once. But it's different from hard disk space, which is where all the software and data lives.

What is RAM exactly then? RAM stands for random access memory. To help us understand how it works we can think of a parking lot with 8 parking spots. 

![](https://farm4.staticflickr.com/3872/14630594145_edc4ca6e67_o.jpg =600x)
 
The parking lot has a single 1-lane gate that acts as both entrance and exit for the cars. The gate is controlled by a binray clock that's either closed, in the zero state, or open in the one state. There are eight parking spaces because our RAM can store up to 8-bits of information. The input can accept  data, like an empty space accepts cars waiting to enter the parking lot.

However cars can't park in spaces which have already been filled and empty spaces must often be reserved. To prevent cars from attempting to park in a  space that has been filled or reserved, a big display tells incoming cars which spaces are in use.

Once the cars need to leave they can exit the parking lot, erasing the data that's been stored in their parking space. This is achieved by opening the gate and letting the car leave, thus setting the state of the parking space and the display to zero. Now that space is free again to be filled or reserved.

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

Do you remember the electronic display at fancy grocery stores which let you know which station to check out? It's when there are few lines of people waiting, and the display shows whichever station that's open, and assigns the person in the front of the line to that station and then move to the next line. It's not a perfect analogy because the real multiplexer only has one input, so all the lines would be a single line. However, the part about the displays showing where to go is quiet similar.
