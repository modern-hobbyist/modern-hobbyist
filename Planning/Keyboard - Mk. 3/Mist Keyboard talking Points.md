One thing to keep in mind when designing a custom keyboard is the keycaps you wanna use.  There are services you can use to order keycaps with custom text or graphics on them, but the only come in a limited set of layouts. So if you go too crazy adjusting keycap sizes, you'll have a hard time finding keycaps that fit. 

So for this design, I started with the ANSI 104 layout and adjusted it by moving keys around, rather than adding them entirely from scratch. 

However, I did go against my own advice in this scenario. I added 1.5u keys to the thumb clusters for what I intend to be my new space and command keys (since I'm a mac user). However, I didn't have any spare 1.5u keycaps in the set I bought, so they ended up being 1.25u keycaps, which didn't actually affect the overall functionality or looks too much.



Now, you have to try not to go too crazy during the layout designing phase, because you have to keep in mind the keycaps you want to use. There are services where you can order custom text or graphics on keycaps, but you're limited to the standard sets. 

I like to buy blank keycap so I can have a little more freedom in terms of where i put each one. 

This layout is pretty much your standard ANSI 104, but the big ticket items for me were the thumb clusters and arrow keys tucked beneath my right palm. With those in place, I was able to repurpose a lot of the keys along the bottom row and this sort of central column to fill in the extra space around the bottom.

And of course, I slapped on a full standard numpad, but I made sure to align it with the bottom row leaving this nice little space at the top, which I'll fill in later... 


At this point, I was pretty sure I had the keyboard layout how I wanted it, but before I move on, I always make sure to 3d print some test plates so I can actually get my hands on it and feel it.

I ended up doing several different versions with just some slight changes, they only take about an hour to print so they save me tons of time and money not having to reorder PCB's that only needed some slight tweaking.

Anyways, once was I certain I had the layout perfected, the real work begins.

- To actually make a keyboard, I need a PCB, and I like to design my PCB's in KiCAD. 
- KiCAD can have a bit of a steep learning curve, but there are some plugins that help to speed this process up quite a bit
- First is the Keyboard Plugin which allows you to take a layout from KLE and it will automatically place all your switches for you according to that layout.
- But before you can do that, you need to create a project and add all your switches. I have a set of template projects, that admittedly could probably use an update, but in any case they make it really easy for me to quickly spin up a new design.
- From there, I usually create a new sheet and start adding my switches, but for this project I wanted to do something a little different.
- In the interest of making this board as customizable as possible, I want it to support more than one type of switch. I know I want it to support standard MX switches which are compatible with standard Gateron switches as well, but I also want it to support Gateron KS-33 switches, which are their low profile switch. 
- To do that, I could either design two separate PCB's entirely, or I could create a new footprint that combines the MX hotswap socket with the KS-33 hotswap socket, and that's exactly what I did!
- Now, I know it looks a little funky but I promise it works because I'm making this video in the future where I've actually tested it. 
- One thing to note is that this doesn't allow you to switch between KS-33 and MX profile switches willy nilly, because you have to actually solder the hotswap sockets on, so you have to choose which one you want when you're building the board. 
- But the benefit, is that if I'm successful, and I'm able to sell this as an actual kit, I can support the MX profile crowd and the low profile crowd with a single PCB design, provided I tell the manufacturer which sockets to install. 

So with my new footprint made, I can go ahead and place all the switches and wire them up with their diodes. To make the layout part easier, I always make sure to renumber all the components to increment from left to right and top to bottom.

This board is gonna have per-key LEDs, so I also and added all the symbols for those. I like the SK6812-mini undermount LEDs cause that way all of the soldering is done on only the bottom side of the board.

I wish I had time to get into all the details that go into designing a keyboard PCB, but I got a lot of stuff to get through so in the interest of time, I'll just link all the resources I used to learn this stuff down in the description.

With all the switches and LEDs added to my schematic, I'm almost ready to run the KB Placer plugin, but first I always make sure to go back and add the component number as an annotation on the front-center legend for each key so that the plugin knows where I want each key to go.

With that done, I can download KLE JSON and run the Keyboard Placer plugin to see my PCB come to life.

The nice thing about this plugin is that I can tell it to place additional components beyond the switches and their corresponding diodes, which means I can have it place the LEDs and capacitors as well.

It might take a little tweaking to get them laid out exactly where I want them, so I usually uncheck the option to "Route with switches" until I'm done messing with it. Then I run it one final time and it'll connect the diodes and the switches for me.

At this point, I have all the switches, diodes, LEDs and capacitors in place, so I can get started adding some brains and other fun features to this PCB.

I chose the STM32G474RETx MCU which I know is just a bunch of numbers that you probably don't even care about, but I mention it because this really is a massively overpowered MCU for most keyboard applications, but I needed the extra pins and I wanted the extra flash memory for the 2.2" LCD.

Remember that little LCD shaped space I left at the top right of my keyboard, yeah well that's where it's going!

That also gives me a really convenient spot to stick the MCU and all of it's components. Speaking of the MCU components, normally you need a USB C input with ESD and reverse polarity protection and a fuse, and I initially added all those things to this build, but I decided to switch to something better.

One of the things I always struggle with is the USB placement. It's hard to get the port in the exact spot you want it while also having it protrude enough for a cable to connect to it through a case. That's why for this build, I opted to use a unified daughterboard instead.

The UDB not only allows me to place the USB port pretty much wherever I want in the case, but it also provides all the other protections I mentioned earlier for free! Well, not for free, but you get the idea.

I picked up one of these S Series UDB's which means all I have to do is slap a Molex Pico-EZMate connector onto my PCB and wire it up to the 5v's, Ground and the MCU data lines.

Now my PCB should be protected from most common electrical issues and I know they definitely did a better job of it than I would have, so WIN WIN.

So after placing the display, routing everything together, doing a little clean up and finalizing the board outline, I'm finally ready to order my PCB, and there's no better way to do it than with today's video sponsor PCBWay.

- PCBWay ad 

PCB Soldering thoughts
- I wish I had better footage of the actual soldering process, but not only am in just not that great of a cinematographer, but I also don't have a lense that can zoom in enough to show it off. So this is the best you're gonna get.





# Conclusion
- So I set out to design a keyboard that everybody loves, was I successful? You tell me...-