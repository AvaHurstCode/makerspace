[Main](README.md) | [Access](access.md) | [Equipment List](equipment.md) | 
------------------------
[Makerspace website](https://codeuniversity.github.io/makerspace/) |
[Makerspace github repo](https://github.com/codeuniversity/makerspace/) | [Makerspace Slack channel](https://codeuniversity.slack.com/archives/C011CN2SMFY)

------------------------

# Prusa MK4s and Core One 3D printers

The MakerSpace currently has a Prusa MK4S and a Prusa CORE One Printer.

These are fast, modern, high-quality, reliable machines that deliver great performance but are also easy to use and set up for beginners, with a wealth of support and advice available.

Join one of our Introduction to 3D printing workshops to get started if 3D printing is new for you. You can find these listed in the [Introduction sessions in MakerSpace Google Docs](https://docs.google.com/spreadsheets/d/1lh0h8UYRIE3m7rFRqsqK_cCP7AEWUTUCyHSbxTzRfB4/edit?gid=0#gid=0)

You can find material on the Prusa Website about the MK4 and the Core One [Prusa MK4](https://help.prusa3d.com/tag/mk4)
[Prusa Core One](https://help.prusa3d.com/product/core-one)

Please download and read the Prusa introduction manual for safe and reliable printer operation 
 [Prusa MK4 Handbook](https://help.prusa3d.com/downloads/mk4/handbook)

The MK4 and Core One printers are very similar, sharing the same electronics, motors and printhead. Their speed and quality are comparable, though the CORE One has a temperature-controlled printing chamber that allows heat control when printing more complex engineering filemanets such as ABS and Nylon.

*adapted from Prusa forum induction*

The PRUSA MK4S and Core one are very nice printers, and you will find that they are reliable machines with great print quality. There are thousands of users who use this machine as a workhorse, and you can too.

That said, there is a learning curve and people make mistakes. If you are expecting this to be as easy as an inkjet or laser printer, it is not, but it can become that routine once you get over the learning curve.

This is a collection of things most discussed on this forum as a reference for someone having problems starting (initial section) or troubleshooting (second section). None of this is “mine” but rather a collection of the advice, solutions and problems that are frequently discussed on this forum. This should be a good place to start looking for your answers. I am in no way affiliated with PRUSA, just a user who climbed this learning curve with the help of many wonderful forum members.

These hints/steps are not to be used instead of thinking. Think about the problem/steps and make sure they make sense to you. This collection is provided in good faith, but you are responsible for your machine. Electricity and heat can hurt you or the machine. Make sure you are comfortable with the steps and your knowledge before jumping in.

Please watch the introduction video here 
[https://youtu.be/JqH41K2vq0g?feature=shared](https://youtu.be/JqH41K2vq0g?feature=shared)

![overview of Prusa 3d Printer](prusa3dprinter.png) 

## Troubleshooting

### General advice.
1. The first layer is ALL important. Get it right first. See steps listed above. This will prevent a lot of frustration.
2. Print something from the SD card that came with the printer. If it prints fine, and things you slice don’t, then you have a slicer issue. If they don’t, you have a hardware issue.
3. Determine if the issue is persistent or intermittent. Try to localise the conditions that cause it. This is the fastest way to get to an answer.
4. Start simple before getting advanced. This is true for material choice, model choice, and adding the MMU upgrade.

Print comes loose from the bed during printing, causing either spaghetti or a plastic tumour to grow on your extruder.
**Common causes:**
1. Poor Z Height setting (see above).
2. The print bed is not clean (see above).
3. The extruder cable knocked the print off the bed (see above).
4. The model has a small footprint on the bed. Add BRIM in your slicer if the model has a flat bottom, and/or a RAFT if it has a curved bottom.
5. A part of the print has “curled” up and caught on the nozzle or PINDA sensor. Look at supports in the slicer, increase bed temperature, use an enclosure to keep the part warmer and reduce drafts.

Extruder stops extruding filament. (Works for a while then stops)
**Common causes:**
1. Tension on the extruder springs is set wrong (see above).
2. The filament spool is not free to turn, creating intermittent friction or binding. (Or the filament is not wound well on the roll). Fix the filament holder. Consider alternate designs on Thingiverse.
3. The extruder “Hobb-Goblin” pulley is dirty, and debris is following the filament into the extruder.
4. The extruder “Hobb-Goblin” pulley is worn and is no longer grabbing the filament.
5. The extruder cooling fan (that cools the heat-break) is not keeping the heat-break below the filament melting temperature, so it is melting and causing a clog. If in an enclosure, open the door. Verify the fan is running.
6. Intermittent (or broken) connection in the cable bundle for the extruder stepper (not stepping), cooling fan (not cool enough) or thermistor (causing the printer to think the temperature is cooler than it is, causing it to increase temperature beyond the range of the filament). Intermittent comes and goes as the cable flexes at different Z values.
7. Bad temperature for the filament.
8. The set screw on the extruder “Hobb-Goblin” pulley has come loose, allowing the pulley to spin independently of the extruder stepper motor.
9. The set screw on the extruder thermistor is loose, creating a poor temperature reading of the heat block (see 6).
10. Poor quality of the filament diameter. Measure it with a calliper over a short span. Try a different spool.

Bad surface quality on the final prints.
**Common causes:**
1. Temperature swings. Do the two PID calibrations in the menu. (See above). (Some disagree.)
2. Loose belts (see above).
3. Linear axis (X and Y) bearings are binding or jerky (technical term). Check assembly, consider lubricant.
4. Wobbly Z axis or wobbly extruder casing.
5. Belts are rubbing on the pulley. This creates a periodic “bump” that takes the shape of vertical lines on the print.
6. Slicer settings. (A topic unto itself). Try different temperatures, retraction, cooling fan, etc.
7. Poor quality of the filament diameter. Measure it with a calliper over a short span. Try a different spool.

Print suddenly shifts in X or Y and keeps printing.
**Common causes:**
1. Loose belts. (see above).
2. The extruder cable hit the print. (see above).
3. Stepper motor not secured properly.
4. Curled print hits the nozzle or PINDA sensor.
5. Bad wiring to steppers, or steppers overheating (rare), or power issues (use a UPS).
6. Binding on the axis - bearings not clean/parallel, failing or not secured properly (zip tie) to the carriage.
7. Cat, kid, or ghost bumped the extruder while printing. Punish the offending party.

The heated bed struggles to keep up with hotter bed temperatures.
1. There is a potentiometer on the power supply. It comes set around 11.5V. People have reported success with increasing it to 12V to 12.5V. There is some controversy to this; read the forum for details.

## Software

There are 1000’s of free and paid tools out there for creating your models, slicing them, and so forth. This is really not the forum for that detailed a discussion, but here are some common ones so you can research them yourself. Prusa 

### OctoPrint
If you are on campus, you can print and monitor your print via OctoPrint.

[Octoprint Prusa MK4S](http://192.168.15.105)
[Octoprint Prusa Core One](http://192.168.10.156)

### Slicers 
* Convert .stl files (models) into .gcode commands for your printer. These can make a HUGE difference in your print quality. Most have 100s of settings and thus a learning curve, but the knowledge of the control is worth it. 
* Common ones are: [Slic3r (use Prusa one)](https://www.prusa3d.com/page/prusaslicer_424/), KISS, Cura, Simplify3D (S3D) [Guide to slic3r]( http://www.instructables.com/id/Guide-to-Slic3r/)
* There are many Prusa Slicer introduction videos - here is a reasonable one [YouTube: 
PrusaSlicer Beginner Tutorial: Learn the basics](https://www.youtube.com/watch?v=_kIqMPNQNSw)

### CAD
 * [OpenSCAD](https://openscad.org/) is open source, powerful, but complex - good if you have a programming background (even just a bit). [TinkerCAD](https://www.tinkercad.com/) is a super easy introduction to making 3d Models for printing. There is also software such as [SolidWorks](https://www.solidworks.com/) and also [SketchUp](https://www.sketchup.com/en)
* Autodesk Fusion360. Industrial level 3D modelling tool with free access for educational use [Fusion360 download](https://www.autodesk.com/products/fusion-360/choose-usage)
  * This intro to Fusion360 from formlabs is a good quick overview [formlabs: Fusion 360 Tutorial: Basics and Tips for 3D Printing](https://formlabs.com/eu/blog/fusion-360-tutorial-basics-and-tips-for-3d-printing/)
   
### Sculpting type modeling
* [Blender](https://www.blender.org/) and similar.

### Model and mesh Manipulation: 
* [Meshmixer](https://meshmixer.com/)
* [meshlab](https://www.meshlab.net)


 ![CODE logo](Word_AppliedSciences_Black-sml.png)
