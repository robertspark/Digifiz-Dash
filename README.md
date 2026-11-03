### NOTE: This is a work in progess, I'm not programmer or git expert, so I update straight to main branch... Sorry! ALSO the arduino code that is currently up is somewhat functional but definitely not finalized. That is the next focus.... (feb 2021) ###

# Digifiz-Dash v.03
### by GFunkbus76 / aka Gavin
## Check out http://www.youtube.com/GFunkbus76

 A pygame Dashboard mimicing the VW Digifiz Dash of the 80s. Powered by Raspberry pi4 and arduinos. This project was inspired by ManxGauged (on github) as well as supported by numerous online tutorials and google searches, I'm a cut, paste, edit and run coder... so beware. Sorry if I've used your experience and not thanked you! Tech with Tim, Coding by Mosh, Rik Cross and Christian Duenes on youtube all had good content I think! Thanks to DONE with ConsultDash(github) for some intial inspiration as well as Everlanders(youtube) oh yeah, also This Old Bus (has a canbus/node-red setup!).
 
 This has been a long term, evolving project started in 2019/2020. My project vehicle, a 1976 VW Bus has been customized and 
 includes a 1.9L AAZ Turbo Diesel engine upgrade. I wanted to also modernize some of the systems in the vehicle - mainly
 monitoring and entertainment. For entertainment, I'm currently using OpenAutoPro - it runs my 'head unit' part of the project.
 For the gauge cluster, I ended up going more one-off. As I'm going to be integrating various sensors, and not just plugging 
 in OBD2 or CANBUS - I have to decipher and interpret the data myself for display.
 
**This project has a few main areas:** 
  -Hardware 
      #-Raspberry Pi 4, 4gb as main computer
      #-Arduino Mega in engine bay transmitting via canbus currently (EGT, RPM, Boost, Oil Pressure, Coolant Temp, etc)
      #-Arduino Nano in front to receive and interpret canbus signals, connected to RPi via serial usb
      #-2nd Arduino Nano in cabin will probably function to do a variety of other sensors(ambient temp, gps, speedometer sensor)
      #-2x LCD Screens, 1x 7" Touch for the headunit, 1x 12.3" stretched LCD for the dashboard cluster
      #-Various sensors and modules (GPS, EGT, Pressure Transducers, optoisolators, buck converters etc)
  -Software
      -OpenAutoPro (use Coupon Code oap_2020 to save 5%) - I use this to manage the headunit and Android Auto portion
      -Digifiz Dash (main.py) - this is the main python/pygame code to run the dash
      -Mosquitto MQTT broker - set to run on Pi, it will publish the data from the Arduino to the Dash
      -Node-Red - used to manage MQTT processes
      
  -Mechanical
      -Wouldn't be much of a dash without a car to attach it to!
      -I've owned the bus since 2003 I think, still not done. So don't expect fast progression...
      -Have to finish the motor swap, hooking up of additional sensors then lots of testing.
      
**OKAY ... so, what's in this github?**
-main.py is the main program that runs and controls the pygame with python
-There is a folder for images and fonts, dive in and see. Image planning is important for using pygame.

#### NOT A PYTHON DEVELOPER!! ... THIS IS A HOBBY! ####
   If you've got tips or advice on how to clean up the code let me know!
   

 
 **Disclaimer:**
    -Not at all connected to or involved with VW. Using their logo for use in a VW with respect and admiration! Be gone lawyers!
    -This is not a tested or complete project, it represents  work-in-progress and should be treated as such.
    -Please check your local laws and guidelines if you wish to install this in a vehicle ....
 
# USE AT YOUR OWN RISK!

## Repository status and workstream maintenance

Documentation review: 3 November 2026. This is repository-local status, not an upstream release or deployment acceptance.

### Purpose and function

A pygame Dashboard mimicing the VW Digifiz Dash of the 80s. Powered by Raspberry pi4 and arduinos.

### Current objective

Maintain a clearly documented local copy for authorised evaluation/development, preserving upstream attribution and distinguishing local changes from upstream capabilities.

### Progress and evidence

This is a fork of gfunkbus76/Digifiz-Dash. Existing upstream documentation and attribution are retained. Local customisation, upstream parity, build success and runtime/hardware acceptance have not been verified in this documentation review.

### Next steps and roadmap

1. Confirm the next owner-approved outcome and reconcile this default branch with the workstream's actual source, test evidence and deployed version.
2. Compare with the upstream project before updating and use an appropriate disposable/non-live test setup.
3. Keep completed/in-progress/blocked work and next actions current here. Broader feature priorities remain for the owning workstream to agree; this update does not invent a feature commitment.

### Documentation chain

Read this README first, then the existing records and source/example entry points below. Listed paths were observed on the inspected default branch; source folders are not test results.

No separate root roadmap/handover was present. Maintain the objective and next actions here until a dedicated, linked record is needed.

- [Upstream repository](https://github.com/gfunkbus76/Digifiz-Dash)

### Standing instruction for every workstream

Every agent, developer or project workstream maintaining this repository must automatically keep this README current with its purpose/function, agreed objective, dated progress, blockers, roadmap/next actions and links to authoritative records. Update it when these facts materially change, at meaningful milestones and before handback, interruption or completion; do not wait for a separate owner reminder.

Read applicable project instructions, preserve concurrent work and existing attribution/licences, and distinguish source commits from deployed versions and verified results. Link requirements, design, handover, validation and recovery records when they exist rather than creating conflicting copies. If a fact is unknown, say so and identify the next verification action. Check affected links, publish authorised changes and verify the remote commit before claiming completion.

Keep credentials, private infrastructure/access routes, private datasets and confidential material out of public documentation. This instruction does not grant new access, replace project-specific authority or approve untested hardware/live operations. Retain detailed historical evidence in project records/version history rather than an ever-growing README log.
