# handmade computer

This posting is for Sam and Paul who I'm working with for a piece to be published at Avant.org soon.

#Overview 

- Multimedia introduction to Handmade computer piece on Avant.org.
- Readers scroll down to view the piece, few elements react to mouse click, mouse drag and etc. 
- Media contents include plain text, drawing (jpg, gif), video (quicktime file or vimeo link), photograph (jpg). 
- Viewing/reading time- 10 minutes or less, although they may connect to other resources with more material.     
- General feeling of the piece is playful and friendly and yet critical in core points. 

#Material 

Material that already exist online

- The project [documentation page](http://taeyoonchoi.com/handmade-computer/)
- Photo gallery [process](https://www.flickr.com/photos/80913365@N04/sets/72157642581138505)
- Mock up with images selections on [medium](https://medium.com/@tchoi8/29dec535074a) 
- Inspiration for layout, [Korean webtoons](http://webtoon.daum.net/webtoon/viewer/27963) 

Material which we will use for the Avant.org piece

- [Introduction](https://github.com/tchoi8/handmadecomputer/blob/master/Introduction.md)
- [Manifesto](https://github.com/tchoi8/handmadecomputer/blob/master/Manifesto.md)
- Some new writings and image captions 

# Interactive 

The piece will take inspiration from an interactive storytelling projects such as [this](http://www.nytimes.com/interactive/2014/09/19/travel/reif-larsen-norway.html). I haven't done a project like this before and do not have knowledge about how to do it most effectively. Therefore, I will be happy to hear your feedback and make it in the best way possible. While I can provide all material and storyboard, I will need help in programming interactive elements of the piece. 

###Vertical scroll 

Media objects appear and disappear in response to vertical scroll. The images appear in foreground and background, some of which are video 
Text bubble shows up, disappear (text bubble includes my handwriting) on top of the static image. This can be very helpful for dense images like this one)
![](https://farm4.staticflickr.com/3885/14442989638_19b14f5bc3_z.jpg)

In total, I think there will be about 7~10 images which react to the vertical scroll, and more images that are embedded between the text. 

###Binary logic demonstration
 
**Basic version**: An animation of binary logic and how it can be used to manipulate NAND gates and construct digital clock (oscillator), half adder and memory (flip-flop). The animaiton will go through various steps of logic, each part will be sequenced like a sprite animation. The animation will be based on hand drawings of the circuit. It may also involved having a static image on the background and having a small part of the drawing animate. If we don't have the time to make this with JS or anything that makes it native for the web, I can make an animated gifs, but it will be less awesome. 

**Full version**:


This maybe the piece for Rhizome.org main page. It's the visual explanation of the hardware 1 bit computer demonstration starts around 1 minute into [this video](https://vimeo.com/122206226).  

The demonstration is an interactive object which react to the users mouse click. The animation will be composed of four scenes, first three scenes demonstrate three elements of the computer and the final scene connects three components to make the primitive form of computer. 

Mouse Interaction: Viewer's mouse over the resistor sign and dragging to the left and right change the resistance value- and change the shape of the signal. Mouse drag to right - more resistance and slower frequency. 
![](https://farm1.staticflickr.com/268/18309860140_11f0769a0b.jpg)

For Memory, flip flop, the viewers may lock the data on the latch. This means that when they click S or R, the corresponding output will be turned on and off. If they lock the gate by clicking on the other input (R for S, S for R), and click on S or R, the data will remain stored until the gate is unlocked.
![](https://cdn.sparkfun.com/assets/learn_tutorials/2/1/6/34-sr-latch-nand.png)

And it will complete with Half adder. 
![](http://elm.eeng.dcu.ie/~molloyd/EE223Files/lab2_files/halfadderlogic.gif)
These images will be presented as a one complex schematic in the final scene. 
The viewers will be able to add two numbers and remember it by holding the bit on the latch, and delete it based on clock cycle. Thus we have an elementary state machine. 


###Embedded video 
 
Short clips of the video documentations of the making process and demonstraion will be embedded in the post. I can edit and make them available on vimeo/ youtube. However I  wonder if there will be a way of embedding video witout linking it to vimeo or youtube. Also, the video can be playing on full screen on the background. 


### Dev
JavaScript: I will be stoked if we can use [p5.js](http://p5js.org) to make the interactive parts, because the open source community around p5 is great, and I can see the right kind of readers coming in from there. Also the piece can be featured in p5 gallery. However, I understand the library is still limited and might not be the most efficient ways of doing things. 
