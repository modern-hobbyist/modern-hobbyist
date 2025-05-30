## Layout
<img src="screenRecording-000167@2x 1.png" />
## Footprint
For this design, I decided I wanted to support more than one kind of switch:
- Gateron KS-33 (low profile Gateron switches v2)
- Cherry MX and Gateron Normal profile
After chatting with some folks on Discord, this is possible to support multiple types of switch with seemingly incompatible footprints by overlapping either the different switches/footprints or combining the two footprints into a single one like this:
<img src="./screenRecording-000166@2x.png" width="300px"/>
In this example, these are hotswap footprints that I've manually combined into a single footprint `KS-33_MX_HOTSWAP`.

Couple things to note about doing this:
- Will require a plate to keep the switch steady since you're overlapping several of the post holes. 
- Might get some DRC errors, need to manually override them.
- Manu might not be able to make them depending on how you overlap switches
- Some switch types are NOT compatible, the pads and holes might overlap too much.

## Gasket Mount
- Should have about 1mm of space between the PCB and the plate sides
- The gasket mount is basically a method of suspending the plate on gaskets or foam pads so that it has some bounce to it as the user is typing.
- The Megalodon macropad I have is gasket mounted so that could be a good resource


