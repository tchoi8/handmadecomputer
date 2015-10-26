Goal: "Hello World" in the Binary World with Electronics : D 

Concepts: 

- Basic electronics 
- Binary numbers and adder 
- Boolean logic and Universal gate 
- NAND gate Integrated Circuits chip 

#1. Breadboard 

Hello My name is a Breadboard!

We will use the breadboard to quickly prototype electronic circuits without soldering. Let's see how it works :) 

By the way, Breadboard is called Breadboard because the hackers of the olden days used to make circuits on wooden breadboards (using nails as connection points). It's an ideal nonconductive surface that can hold electrical parts in the right place. The modern breadboards are usually made with plastic, which is nonconductive and metal terminals which are conductive. The electrical current travels only in the conductive surfaces. 

**Terminal**: First, place the breadboard with the tiny alphabets facing up.  You should be able to read the alphabet from Left to Right. The letter row (ABCDE) are part of the terminal strips that are connected by metal plate underneath the plastic grids. On the other side of the notch (valley that divides left and right side of the breadboard) there are (FGHIJ) which are also connected. 

Each of these terminals are connected horizontally, but they are separated vertically. 
So the terminal ABCDE on the row 0 is separate from and the row 1.  

**Bus (Power rails)**: On the right and left end of the breadboard, there are two lines of Red and Blue. These buses are connected vertically from top of the breadboard to the bottom. They are conventionally used to supply Power ( + / Red) and Ground ( - / Blue)

#2. Battery

Hello My name is a battery! 
 
The Battery is our power source. The battery holder contains 3 AA batteries connected serially, which adds them up to make a 4.5 Volt. There are two wires coming out of the battery holder, one is Red (+ / Power) and Black or Blue (- / Ground).

Voltage is the electric potential difference between two points. 
Our battery holds close to 5V of difference in energy. 

When the circuit is completed with components, current travels between the circuit with a flow of electric charge. This is the energy that does the job for us, such as lighting up the LED or moving a motor. 

It's very important to **not** connect two of them directly, which is called 'shorting'. When the circuit is shorted, the battery will get hot very quickly and potentially destroy the circuit. Always have two wires on the correct spot (either Red or Blue bus). It can be also helpful to connect Battery using opposite columns on the Breadboard -- ex below (chose the heart option)

#3.Wires 

We can use the wires to connect one part of the breadboard to another part. Since wires are very conductive and we can use it to join one electronic component to another component, like connecting the dots with a line. The wires are covered in plastic sheathing, which makes them only conductive in the part that is stripped. There are few different kinds of wires, solid core wires are rigid inside and easy to shape (cut and bend) to connect parts on the breadboard. Standard wires are soft and they are good for connecting Input parts like a switch and Output parts like a motor. There are also Jumper wires which have pins on the either end, which is great for quickly connecting parts to test it works.  

#4.LED

Hello! I am an LED : )

LED is short for Light Emitting Diode! 
An LED is a diode that makes light when the current travels through it. The concept of diode is simply an electrical component that allows current to travel in one direction, but not the other. So, like a diode, LED has a polarity, which means it only works when the current travels from Anode to Cathode. We will explain these terms with an illustration. 


LED anatomy 

- Longer leg is ( + ) = connect to Red // Power ((anode))
- Shorter leg is ( - ) = connect to Blue // Ground ((cathode)) 
- Uncertain which leg is which? Some LEDs have equal length for both legs or reverse. You can tell by looking inside the LED. 
- Inside the bulb you'll see two tiny triangles:
 	- Triangle pointing upwards = ( + ) 
	-Triangle pointing downwards = ( - ) 
- The thin wire emits the light (light emitting part of LED) 
- In diagrams and schematics, you'll see LEDs represented like this: 


Putting a LED straight in between + and - on the breadboard will pass on too much current. Doing this might damage the LED if it's left on for too long. We need to use a *resistor* to make the LED happier.  

#5. Resistor

Hello! I am a resistor!  

Resistors come in different values, and they make it more difficult for the current to travel in the circuit. 
Unlike the LED, resistors do not have polarity. It means that they can be placed in any direction and it will work the same way.  Also, it can be placed before Anode or after Cathode on the circuit, it affects the LED in the same way. 

LEDs typically have 3.4 diode forward voltage and 6.8 mA forward current. 
- Link for more details
- Calculating resistor for an LED
We will use 100 Ohm or 200 ohm resistor for this circuit. 

Resistor is like a bumpy road, it makes it more difficult for the current to travel.


Now, we are going to control the LED with a switch. This switch will allow you to turn your LED switch off and on.  

#6. Switch 

Hello! I am a switch! 

A switch connects the output pin (in the middle) to either one of the inputs (the outer pins in both ends). 
Inside of the plastic shell, there is a metal plate that physically slides one of the input to the output.   

Step by Step!

- We are going to leave the LED's Cathode and Resistor in where they are. 
- Now, move the Anode of LED out of the Power and put it on an empty Terminal on the breadboard near the Cathode. Also, don't feel bad about stretching the Anode out, like a tiny person spreading his legs to jump across a ditch. 
- Use a piece of wire to connect the Anode of LED to a breadboard terminal that's further away from ( where?) the LED, maybe 3~4 Terminals would be good. This wire will now be our Input Terminal.  
- Use the short wires to connect the Power (from Red + of the Breadboard bus) to the Input Terminal. And then connect another wire to the Ground to the terminal underneath the Input Terminal. 
- Place the switch vertically with the middle pin on the Input Terminal. The two other pins are now connected to the Power or Ground. 
- Slide the switch up and down. If everything is placed correctly, this circuit will turn on or off the LED. 

Now, we created a Digital switch! We have an Input (switch) and an Ouput (LED) which is always either On or Off, in other words either High or Low, 1 or 0.  

#7. Binary Logic 

Do you remember a math class in grade school or middle school when the teacher introduced series of Venn Diagram? 
It's basically circles that over lap with each other in different ways. 

- One of the first Venn Diagram to look for is a for when A and B are in common. It's when A and B are both True, the output is True. This is logically same as AND gate. Only the intersection of two circles are colored because it's only true when both are true. (this is repeat)  
- The next one is when either A or B is True, the output is True. This is logically same as OR gate. Both A and B circles are colored because if any of those are True, the output will be True. 
- The next one is an opposite of the first one, so when A and B are both False, the output is True. This creates a diagram where only the intersection is False, and everything else is True. This means when A is True and B is False, the output will remain Tr
ue. When A and B are both False, the output will be True. Only when A and B are both True, the output will be False. This is logically same as the NAND gate.  
- There are few more logic gates. One of them is NOR gate. As the name indicates, it's Not-OR Gate. It's the exact opposite of OR Gate. So, it needs both of the Inputs to be False, for the output to be True. For this diagram, only the parts outside of the circles are colored. 
- There are other gates like XOR, XNOR as well as NOT and Buffer which we skipped. However, it's important to note there are only finite amount of Boolean logic for two Inputs. And all of them can be created by manipulating NAND or NOR gates, which is known as the Universal Gates. 

#8. Chip

Hi! I'm a CD 4093 Chip (CMOS NAND Logic Gate) : D 
 
 
Inside of the chip, there are four Logic gates that operate NAND logic.

#9. Hello world with 1 Bit Computer!
Two exercises: ( sketch out schematic? with happy emotive LEDs etc?) 

- 1)  LED + 1 Switch 
- 2) LED + 2 switches 


###BATTERY: 

Let's get the current flowing :  )  Zzzzt -- Electric! 

- Connect *Battery's Red Power wire (+) * to ----> top socket of *Breadboard's Left Power Bus Strip (red/+)*
- Connect *Battery's Blue Ground wire (-) *  to ----> top socket of *Breadboard's Right Ground Bus Strip (blue/-)*
- Now - let's connect both "Bus Strips" to one another in order to distribute current 
- With a piece of wire, connect the *Left Bus Strip's Ground (-)* to *Right Bus Strip's Ground(-)* (crossing over A-E, trough/valley, and F-J)
- With another piece of wire - connect *Left Bus Strip''s Power(+)* to  *Right-Terminal's Power(+) *  


###SWITCHES:

We'll have 2 switches:  Switch A and Switch B


Pick a switch.  Any (Single pole double throw) switch. 
- This is now **Switch A** . : )  
- Place 'Switch A' on breadboard's *Right-Side* Terminal Strip 
- Make sure to place your switch vertically. Each of your switch's pins should be connected to a different terminal. 
	- So that the pins - two inputs and one output- are all on the different Terminals. 
Numbered from 123 for example 
	- Do not place horizontally. 
- Make sure to give yourself plenty of room to build out your circuit below. We suggest half way or higher.

- Connect Switch A to power and ground
- Now that Switch A has found a home, let's connect it to power (+) and ground (-).  
- Take a small piece of wire (cut and strip new piece if needed)
- Connect Switch A's top-right pin (the one furthest away from you) to power (red + column) 
- Take another small piece of wire (cut and strip new piece if needed)
- Connect Switch A's bottom/third pin to ground (blue - column) 
- Perfect! 

Let's Repeat for **Switch B**. Repeat steps from Switch A with a new switch - but on opposite (left) terminal strip. This is now our Switch B. Although it doesn't matter which number terminal you place the switch on the terminal strip, to make our happy face pictured above - let's mirror Switch A's position with our placement of Switch B

###CHIP PLACEMENT 

Let's add our Chip :D 
The chip should have CD 4093BE printed on the top. If it's different Chip, it will behave differently.


In most chips, there is a half circle indented on one of side. This is usually considered the top of the chip.  

- Place chip on the board 5 or so rows below Switch A & B
- Have it bridge the two terminals - straddling the breadboard's valley. 
- Connecting Chip to Power & Ground
- Wonderful! Let's connect our chip to power and ground. 
- Take a small piece of wire (cut and strip new piece if needed)
- Connect your chip's first/top-right pin to ground (red +) 
- take your small piece of wire and place it in one of the squares that's on the same row as your chip's top right pin. 
- Connect other end of wire to power (red + // right terminal)
- Take a small piece of wire (cut and strip new piece if needed)
- Connect your chip's bottom left pin to ground (blue - // left terminal) 

 
*It's important to have the correct orientation of the chip. If it's placed in wrong direction, we will be supplying Power to the Ground Pin and Grounding the Power Pin, which may damage the chip if it's left for a while.*  


###INPUT / OUTPUT PARTY!

Now it's time to connect Switches A & B to our Chip

- Take a piece of wire (cut and strip new piece if needed)
- Connect Switch A
- Place one wire end in same row as *Switch A's 2nd/middle pin*.  Reminder, Switch A is the Switch on right terminal.  
- Crossing over the trough/valley, place other wire end into the same row as your Chip's Top-left Pin. 
- Success! Now onward to connect Switch B 
- Take a piece of wire (cut and strip new piece if needed)
- Take one wire end - place in a socket the same terminal row as "Switch B's" 2nd-middle pin 
- Place other wire end in same row as Chip's left side, 2nd pin from the top
Huzzah!

LED PLACEMENT: 

- Now that our switches and chip are placed and powered, let's add our LED.
- Pick up your LED. Note which leg is ( + anode) or ( - cathode).   
- Remember that your LED legs are very flexible - meant for stretching across rows, etc. 
- Take your LED for a walk - Stretch LED's legs and place it on the left terminal strip below your current circuit. 
- Place Anode ( + ) leg first, closer to chip. Then, Cathode ( - ) leg, walking away from chip, crossing at least 2 terminals - see diagram? ) 
- Now that both LED legs are placed, let's connect it to our Chip. : )  

CONNECTING CHIP TO LED:

- Take a piece of wire (cut and strip new piece if needed)
- Place one wire end in the same row as your chip's 3rd pin, on the left terminal strip 
- Take other wire end and place it in the same row as your LED's Anode( +) // leg closet to chip 
- How does it look? 

Like this? 

- Perfect! Now on to our resistor!  

RESISTOR PLACEMENT: 

- Resistors are very important. They help control our current flow (point back to ch:5 Resistor) 
- Take your resistor - note it's ohm (consult ohm calculator if needed)
- Place one resistor leg in the same terminal row as your LED's cathode ( - ) 
- Place other resistor leg in your left ground (-) column // on the left bus strip 


CHECKING YOUR CONNECTION: 

- Awesome! Now that your circuit is complete, you can try out different switch connections.
- Take a second and play with Switch A and Switch B  
- Can you tell what kind of logic it is? 
- Not working how you thought it would? We can check it with a jumper cable : ) 


NAND Logic on the Breadboard!

- Now we connect the 3rd Pin to a LED
- Cut a piece of wire and connect the 3rd Pin with Anode of LED. 
- Connect the Cathode of LED to a resistor. 
- Resistor's connected to the Ground. 
- If unsure, connect the Anode of LED to Power (+) first to see if LED is working properly. 
- It's worth checking if the LED is positioned correctly, because LED has polarity. 
 
 

Outro! 

Now we successfully demonstrated NAND logic on the breadboard.
Here are the next challenges for you.

- Make an AND Gate from using 2 NAND gates on the I.C. 
- MAKE an OR Gate from using 3 NAND gates 
- Make an NOR Gate using 4 NAND Gates
- Make an XOR Gate using 4 NAND Gates

You can do all of this with just 1 NAND Chip. That's pretty awesome to manipulate a logic gate to make other kinds of logics. It's proving that NAND is a Universal Gate. And this is precisely the reason that computers can be built from electronics quiet efficiently. 
