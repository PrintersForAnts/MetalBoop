# MetalBoop

![MetalBoopRender](./imgs/MetalBoop_FinalRender_Both.png) 

**Note: Unfortunately, we did some further improvements in design to reduce CNC costs, therefore MetalBoop is going to be officially launched in _early July 2024_ as we have to perform one more internal testing iteration. It is an open source project - CAD files will be available for the public. This site is under construction - new content is added daily. BOM is already available as you may need to get certain items ahead such as MGW7C rail.**


## 1. Introduction

  A smaller metal version of plastic [Boop](https://github.com/PrintersForAnts/Boop).

  MetalBoop shares many of the same features as Boop and [Tap](https://github.com/VoronDesign/Voron-Tap/), such as:
  * Microstep level accuracy
  * Durability due to optical switch
  * Simplicity - no dock and undock macros to fiddle with
  * Zero probe distance
  * Max chamber temperature: 100 C (when using OPB666N)


## 2. Features
- Higher rigidity due to use of metals instead of plastic.
- Printed boop reduces Y travel by ~ 14mm, Metalboop by **only** 8mm.
- Using a wide MGW7 rail instead of MGN9 - rigidity is on par with MGN12C while taking 1mm less space in Y direction.
- Placement of a singular high temprature magnet eliminates the need to assemble and configure lateral magnets on both sides.
- Special optional front plate has two extra bottom mounting holes for better attachment of DragonBurner v8 toolhead.
- Tested with DragonBurner v8 to ensure as much space as possible for hotend wiring.
- Modified version of Vitaliis CNC tap belt attachments.
- MetalBoop is shorter 10mm vertically - so no need to worry about build plate crashes.
- Simplified assembly using printed mounting jigs for MGW7 rail and magnet.

  
## 3. Compatibility

Same as plastic [Boop](https://github.com/PrintersForAnts/Boop). Any Voron0 type toolhead compatible with front plate (eg. Mini StealthBurner). 100% compatible with Dragon Burner v8.


## 4. BOM

| Part | Quantity | Links | Note
|---|---|---|---|
| Rail MGW7C/STW7C 40mm | 1 | [Aliexpress](https://www.aliexpress.com/item/1005001499370117.html) | Z2 preload 5mm edge-to-hole
| Magnet B842SH  | 1 | (NA) [Kj Magnetics](https://www.kjmagnetics.com/proddetail.asp?prod=B842SH) <br>(EU) [Replimat](https://www.replimat.eu/metalboop-magnet-b842sh/rt10176) | To secure magnet, RTV Silicone is needed. Make sure you have it or get high quality one.
| M3 10mm spacer  | 2 | [Aliexpress](https://www.aliexpress.com/item/1005003018651855.html) | Only needed if using 3-part version of MetalBoop
| M3 10mm standoff  | 2 | [Aliexpress](https://www.aliexpress.com/item/1005005462128073.html) | Only needed if using 2-part version of MetalBoop (can also use plastic standoffs)
| 2x Makerbeam T-slot - (drilled out to 3mm) | 2 | [Aliexpress](https://www.aliexpress.com/item/1005004891815148.html) | Optional - only used to additionally secure belts
| BHCS/SHCS M3x5 | 2 |  | Optional - only used to additionally secure belts
| BHCS/SHCS M3x22 | 2 |  | Only needed if using 3-part version of MetalBoop
| BHCS M3x6 | 2 |  | Only needed if using 2-part version of MetalBoop
| FHCS M3x5 | 8 |  | Make sure these are 5mm; 6mm version is too long!
| SHCS M3x4 | 1 |  | Used to mount top part of MGW7 rail
| SHCS M3x5 | 1 |  | Used to mount bottom part of MGW7 rail
| Slim version of OptoTAP PCB (5V only) | 1 | (EU) [Lab4450](https://lab4450.com/product/voron-tap-probe/) (select OptoTap v1.3 5v with Omron SX-EE398)  <br>(NA) [Fabreeko](https://www.fabreeko.com/products/voron-tap-pcb?_pos=1&amp;amp;amp;amp;amp;amp;_psq=Tap&amp;amp;amp;amp;amp;amp;_ss=e&amp;amp;amp;amp;amp;amp;_v=1.0&amp;amp;amp;amp;amp;amp;variant=44462578368767) (select Voron TAP 5v) | Although either PCB type can be mounted, the larger version of the Tap PCB may interfere with either the extruder or extruder stepper.


## 5. Assembly

As assembly manuals are not complete yet, we are providing instructions on the go as needed.

[Here are some short descriptions regarding use of printed jigs to help with correct assembly.](https://github.com/PrintersForAnts/MetalBoop/tree/main/STL/jigs)

## 6. FAQ

1. When is it going to be available?
  * As soon as we finish internal testing. If everything goes by the plan we have and there are no major issues, **you can expect it to be available in around early July 2024**.
        
2. What else besides the BOM do I need?
  * Unfortunately, from the start, we expect that for the first few weeks or months, you will also have to get parts manufactured on your own. There are online services such as [JLCPCB](https://jlcpcb.com/) or [PCBWAY](https://www.pcbway.com/) which can make the parts. After some time, we hope vendors will pick up the design and make kits with already manufactured metal parts so you won’t have to do anything but buy a kit and assemble it.

3. What is the difference between 2-part and 3-part MetalBoop?
  * Boop usually consists of 3 main metal parts; those are:
    * base plate (screws into X rail cart and to which belts are attached),
    * front plate (screws into Boop's vertical MGW7 rail and toolhead) and
    * top plate (screws into front plate and where optical sensor PCB attaches to).
  This configuration is called 3-part MetalBoop and is cheaper for CNC production. 2-part MetalBoop is optimisation to further increase rigidity by merging front and top plates together. But while more efficient and also easier to assemble, it can be 5-20 $ more expensive to produce. Both versions are available and the choice which one to get and assemble is yours.
![MetalBoopDifference](./imgs/2part-3part-diff.png)   

4. How much downforce is there?
  * While for Voron Tap is being said that it needs 600g of force to uncouple, we measured MetalBoop needs around 1500g! This means that it is way more rigidly coupled than Tap, which should improve your input shaper charts and allows you to print with higher accelerations while maintaining same level of print quality.

5. Is it mandatory to use T-nuts and M3 screws to attach belts?
  * While for plastic Boop, simply hooking belts between rail and plastic part turned out not to be enough, when using aluminum parts, this is not the case. Using additional T-nuts and screws is therefore completely optional thus redundant. 
        
6. I would like to sell manufactured metal parts. Can I do that free of charge or do I have to ask your permission or pay for license, royalties, etc?
  * MetalBoop is completely open source, released under MIT license. You can freely use designs for your commercial purposes free of charge.


## 7. Credits
- [Kizime123](https://github.com/Kizime123) for CAD design
- [djeZo888](https://github.com/djeZo888) for sponsoring and initial testings
- [LillianaMirrors](https://github.com/LillianaMirrors) for the manual / github page

Credits also go to:
- [Voron TAP](https://github.com/VoronDesign/Voron-Tap/) designers
- [Boop](https://github.com/PrintersForAnts/Boop) designers
- [AndyABG](https://github.com/AndyABG)
- Solders
- [Vitalii](https://github.com/Vitalii3D-xyz)
