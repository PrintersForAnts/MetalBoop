# MetalBoop

![MetalBoopRender](./imgs/MetalBoop_FinalRender_Both.png) 

**Note: MetalBoop has been released as beta RC1 - first beta version. There are also five beta testers that are currently receiving, assembling and testing kits for free and will shortly get more information from them regarding beta RC1 - so far, the results are great and comparison charts vs plastic Boop will be posted soon. MetalBoop is an open source project - CAD files are available for the public [here](./CAD).**

---

### Index
1. [Introduction](#1-introduction)
2. [Features](#2-features)
3. [Compatibility](#3-compatibility)
4. [BOM](#4-bom)
5. [Assembly](#5-assembly)
6. [FAQ](#6-faq)
7. [Beta issues/changelog](#7-beta-issueschangelog)
8. [Contact](#8-contact)
9. [Credits](#9-credits)

---


## 1. Introduction

  A smaller metal version of plastic [Boop](https://github.com/PrintersForAnts/Boop).

  MetalBoop shares many of the same features as [Boop](https://github.com/PrintersForAnts/Boop) and [Tap](https://github.com/VoronDesign/Voron-Tap/) such as:
  * Microstep level accuracy.
  * Durability due to optical switch.
  * Simplicity - no dock and undock macros to fiddle with.
  * Zero probe distance.
  * Max chamber temperature: 100 C (when using OPB666N).

> [!NOTE]
> Input shaper improvement charts from beta testers are available [here](./results).


## 2. Features
- Higher rigidity due to use of metals instead of plastic.
- Plastic Boop reduces Y travel by ~ 14mm, MetalBoop by **only** 8mm.
- Using a wide MGW7 rail instead of MGN9 - rigidity is on par with MGN12C while taking 1mm less space in Y direction.
- Placement of a singular high temprature magnet eliminates the need to assemble and configure lateral magnets on both sides.
- Special optional front plate has two extra bottom mounting holes for better attachment of DragonBurner v8 toolhead.
- Tested with DragonBurner v8 to ensure as much space as possible for hotend wiring.
- Modified version of Vitaliis CNC Tap belt attachments.
- MetalBoop is shorter 10mm vertically - build plate crash is impossible.
- Simplified assembly using printed mounting jigs for MGW7 rail and magnet.

> [!WARNING]
> Unfortunately, MetalBoop does not bring only improvements. Due to increased rigidity between parts (magnet coupling), there is substantially more force needed to decouple Front plate. This means that nozzle presses against bed with much higher force and consequently can damage certain weak printpad surfaces. When deciding whether to use MetalBoop, you should consider this important fact.


## 3. Compatibility

Same as plastic [Boop](https://github.com/PrintersForAnts/Boop). Any Voron0 type toolhead compatible with front plate (eg. Mini StealthBurner). 100% compatible with [Dragon Burner v8 - DBv8](https://github.com/chirpy2605/voron/tree/main/V0/Dragon_Burner). All Hotends* and all Extruders are supported.

_* As reported by one beta tester, if using Dragon hotend then silicone sock needs to be cut a bit for everything to fit together properly ([bug report](https://github.com/PrintersForAnts/MetalBoop/issues/1)). We have plans to fix this issue with next beta release._


## 4. BOM

| Part | Quantity | Links | Note
|---|---|---|---|
| CNC parts (2-part version) | 1 | [Open source CNC](./CAD/CNC) or [PCBWay](https://www.pcbway.com/project/shareproject/MetalBoop_2p_beta_RC1_de9ac2f4.html) | Order this if **you are NOT** using Dragon Burner V8 but any other Voron0 compatible toolhead such as Mini StealthBurner. You need to order two parts - Base plate and Front plate!
| CNC parts (2-part version for DBv8) | 1 | [Open source CNC](./CAD/CNC) or [PCBWay](https://www.pcbway.com/project/shareproject/Metal_Boop_DBv8_2p_beta_RC1_88e154ac.html) | Order this if **you are** using Dragon Burner V8. You need to order two parts - Base plate and Front plate!
| Linear rail MGW7C/STW7C 40mm | 1 | [Aliexpress](https://www.aliexpress.com/item/1005001499370117.html) | Z2 (medium) preload, 5mm edge-to-hole
| Magnet B842SH  | 1 | (NA) [Kj Magnetics](https://www.kjmagnetics.com/proddetail.asp?prod=B842SH) <br>(EU) [Replimat](https://www.replimat.eu/metalboop-magnet-b842sh/rt10176) | To secure magnet, RTV Silicone is needed. Make sure you have it or get high quality one.
| M3 10mm spacer  | 2 | [Aliexpress](https://www.aliexpress.com/item/1005003018651855.html) | Only needed if using 3-part version of MetalBoop
| M3 10mm standoff  | 2 | [Aliexpress](https://www.aliexpress.com/item/1005005462128073.html) | Only needed if using 2-part version of MetalBoop (can also use plastic standoffs)
| 2x Makerbeam T-slot nut - (drilled out to 3mm) | 2 | [Aliexpress](https://www.aliexpress.com/item/1005004891815148.html) | Optional - only used to additionally secure belts
| BHCS/SHCS M3x5 | 2 |  | Optional - only used to additionally secure belts
| BHCS/SHCS M3x22 | 2 |  | Only needed if using 3-part version of MetalBoop
| BHCS M3x6 | 2 |  | Only needed if using 2-part version of MetalBoop
| FHCS M3x5 | 8 |  | Make sure these are 5mm; 6mm version is too long!
| SHCS M3x4 | 1 |  | Used to mount top part of MGW7 rail
| SHCS M3x5 | 1/3/5 |  | Used to mount bottom part of MGW7 rail; get extra 2pcs if not using sensorless homing; get extra 2pcs if using DragonBurner V8
| Slim version of OptoTAP PCB (5V only) | 1 | (EU) [Replimat](https://www.replimat.eu/optotap-v1.3-opb666n/rt10181)<br> (EU) [Lab4450](https://lab4450.com/product/voron-tap-probe/) (select OptoTap v1.3 5v with Omron SX-EE398)<br>(NA) [Fabreeko](https://www.fabreeko.com/products/voron-tap-pcb?_pos=1&amp;amp;amp;amp;amp;amp;_psq=Tap&amp;amp;amp;amp;amp;amp;_ss=e&amp;amp;amp;amp;amp;amp;_v=1.0&amp;amp;amp;amp;amp;amp;variant=44462578368767) (select Voron TAP 5v) | Although either PCB type can be mounted, the larger version of the OptoTap PCB may interfere with either the extruder or extruder stepper.

> [!IMPORTANT]
> Current latest available version is beta RC1 which is not rigorously tested by many users yet. Purchase, assemble and use at your own risk!


## 5. Assembly

> [!NOTE]
> Please, [contact us](#8-contact) if assembly manuals are unclear, so we can improve them. Thank you!

> [!TIP]
> You can always check out [CAD design file](./CAD) to see how parts fit together.

![MetalBoopNames](./imgs/assembly/part_names.jpeg)   


#### A) Magnet

Start by assembling magnet because after this task you will have to wait 24 hours for RTV to cure. [Recommended to use printed jig to help with correct assembly.](https://github.com/PrintersForAnts/MetalBoop/tree/main/STL/jigs#assembly-of-magnet)


#### B) Belts

Next attach base plate to X rail cart together with belts as shown in the picture provided by Vitalii (**Vitalii's belt mount**). Make sure that both belts are of equal lengths!

![MetalBoopBelts](./imgs/assembly/belts.jpeg) 

Note that MetalBoop has additional M3 holes for securing belt the same way as plastic Boop. According to our tests, when Base plate is made out of Alu7075 or better, it is enough to secure belts using only Vitalii's belt mount. If you are not sure, you may additionally secure belts using Makerbeam T-slot nuts, but make sure you drill them out with 3mm drill bit before as holes in T-slot nuts must be without threads!

Base plate is secured to X rail cart using **4x FHCS M3x5mm**. You have to do this step before mounting MGW7 rail, otherwise you won't be able to reach these four screws.


#### C) MGW7 rail

Slide MGW7C cart off the linear rail onto plastic jig that was supplied with the rail and save it. You do not have to clean/grease this rail.
[Detailed instructions regarding assembly of MGW7 are here.](https://github.com/PrintersForAnts/MetalBoop/tree/main/STL/jigs#assembly-of-mgw7-rail)


#### D) Sensor

How to mount optotap sensor PCB depends whether you have 2-part or 3-part MetalBoop. 

> [!IMPORTANT]
> If using OPB666N sensor, you may have to extend standoffs/spacers by 0.5mm - 1.0mm because OPB666N is a bit larger and would not fit otherwise. You can do this by adding shims/washers in between standoffs/spacers and OptoTap PCB.

#### 2-part MetalBoop

![MetalBoopSensor2Part](./imgs/assembly/sensor_2part.png) 

#### 3-part MetalBoop

![MetalBoopSensor3Part](./imgs/assembly/sensor_3part.png)


#### E) Finish

Slide MGW7C cart back onto MGW7 rail from below and make sure that the cart doesn't slide off before you complete next step. Carefully bring assembled Front plate near assembled Base plate. When Front plate is very close to the Base plate, magnet's force will position Front plate. Adjust position of MGW7C cart so that 4 mounting holes on cart align with 4 holes on Front plate. Use **4x FHCS M3x5mm** screws to attach Front plate to the cart. 

It is recommended to test MetalBoop before you continue with mounting toolhead. If boop'ing doesn't work correctly, then the issue is most likely in vertical position of sensor. You can adjust that by moving MGW7 rail slightly down and retightening its mounting screws ([make sure to use jigs - clamps](https://github.com/PrintersForAnts/MetalBoop/tree/main/STL/jigs#assembly-of-mgw7-rail)).


#### F) Misc

[If you are not using sensorless homing but rather endstop switches, please check out this page.](https://github.com/PrintersForAnts/MetalBoop/tree/main/STL#xy-homing-using-endstops)


## 6. FAQ

1. <ins>When is it going to be available?</ins>
  * MetalBoop has entered public beta RC1 phase. Note that this is public beta and there may be some small issues here and there. We are doing our best to list all found issues [here](#7-beta-issueschangelog). If you find any issue, error with CAD design or error in GitHub page, please [contact us and report it](#8-contact).
        
2. <ins>What else besides the BOM do I need?</ins>
  * Unfortunately, from the start, we expect that for the first few weeks or months, you will also have to get parts manufactured on your own. CNC design files are available [here](./CAD/CNC). There are online services such as [JLCPCB](https://jlcpcb.com/) or [PCBWAY](https://www.pcbway.com/) which can make the parts. After some time, we hope vendors will pick up the design and make kits with already manufactured metal parts so you won’t have to do anything but purchase a kit and assemble it.

3. <ins>What is the difference between 2-part and 3-part MetalBoop?</ins>
  * Boop usually consists of 3 main metal parts; those are:
    * Base plate (screws into X rail cart and to which belts are attached),
    * Front plate (screws into Boop's vertical MGW7 rail and toolhead) and
    * Top plate (screws into Front plate and where optical sensor PCB attaches to).
      
    ![MetalBoopNames](./imgs/assembly/part_names.jpeg)
    
This configuration is called 3-part MetalBoop and is cheaper for CNC production. 2-part MetalBoop is optimisation to further increase rigidity by merging Front and Top plates together. But while more efficient and also easier to assemble, it can be 5-20 $ more expensive to produce. Both versions are available and the choice which one to get and assemble is yours.

![MetalBoopDifference](./imgs/2part-3part-diff.png)   

4. <ins>How much downforce is there?</ins>
  * While for Voron Tap is being said that it needs 600g of force to uncouple, we measured MetalBoop needs around 1500g! This means that it is way more rigidly coupled than Tap, which should improve your input shaper charts and allows you to print with higher accelerations while maintaining same level of print quality. Note that more downforce is not always better - higher force can damage your printpad, so be aware of that when choosing MetalBoop. We recommend using textured PEI plate, invar plate or any other plate that has strong surface.

5. <ins>Is it mandatory to use T-nuts and M3 screws to attach belts?</ins>
  * While for plastic Boop, simply hooking belts between rail and plastic part turned out not to be enough, when using aluminum parts, this is not the case. Using additional T-nuts and screws is therefore completely optional thus redundant. 
        
6. <ins>I would like to sell manufactured metal parts and/or kits. Can I do that free of charge or do I have to ask your permission or pay for license, royalties, etc?</ins>
  * MetalBoop is completely open source, released under GPLv3 license. You can freely use designs for your commercial purposes free of charge.

7. <ins>I am stuck with assembly/I do not understand assembly process. What should I do?</ins>
  * Get in [contact with us](#8-contact) and ask for help. While also providing help to you, we will do our best to also update currently developed manuals on Github under [Assembly topic](#5-assembly).


## 7. Beta issues/changelog
> [!NOTE]
> Marked issues will be fixed in following version.
- [x] https://github.com/PrintersForAnts/MetalBoop/issues/1 Dragon hotend: small part of silicone sock needs to be cut for MetalBoop to fully fit.


## 8. Contact
You can get in contact with us by:
- Submitting [GitHub issue](https://github.com/PrintersForAnts/MetalBoop/issues) or
- [Discord #CNC_boop channel](https://discord.com/channels/825469421346226226/1222971771444006996).


## 9. Credits
- [Kizime123](https://github.com/Kizime123) for CAD design and
- [djeZo888](https://github.com/djeZo888) for sponsoring, GitHub page and initial testings.

Credits also go to:
- [Voron TAP](https://github.com/VoronDesign/Voron-Tap/) designers,
- [Boop](https://github.com/PrintersForAnts/Boop) designers,
- [AndyABG](https://github.com/AndyABG),
- [Vitalii](https://github.com/Vitalii3D-xyz),
- Solders.
