# CamillaDSP-Building-a-Config-5-Finishing-Touches
5. Fix up a few bumps and potholes in the SPL and add Bass &amp; Treble controls and have a look at CamillaDSP options to "liven up" the music to get away from the clinical dead sound of a flat SPL.

### Add Input channel EQ
When the crossover in practice does not perform like the crossover in theory we are often left with some bumps and potholes in the SPL that bridge two drivers and therefore are difficult to EQ on a driver by driver basis. The solution is to measure the Full System SPL, get REW to calculate the EQ required, then add the filters to the Input channel.

So, here is the SPL-
![alt text](<Images/REW V5.40 26 R 10_03_25 9_43 AM 11 74db no input EQ - SPL Phase.jpg>) 
REW V5.40 26 R 10_03_25 9_43 AM 11 74db no input EQ - SPL Phase.jpg

EQ settings - 
![alt text](<Images/EQ for measurement 7 R 10-033-25 9-43 AM.jpg>)
EQ for measurement 7 R 10-033-25 9-43 AM.jpg


These filters are saved and then imported into the Config file, here is a section of the Input in the pipeline.
![alt text](<Images/CamillaDSP GUI Pipeline tab showing Input filters before Mixer.jpg>)
CamillaDSP GUI Pipeline tab showing Input filters before Mixer.jpg

Here is a REW sweep with the input PEQs/Biquad filters applied
![alt text](<Images/REW V5.40 27 R 10_03_25 9_58 AM 12 73db Inp EQ.jpg>)

Impulse (Step Response), Group Delay (GD) and the Spectrogram are unchanged.

The Pipeline showing the Biquad group of EQ filters in the input
![alt text](<Images/CamillaDSP GUI Pipeline plot showing input EQ filters.jpg>)
CamillaDSP GUI Pipeline plot showing input EQ filters.jpg


### Add "Tone Control" filters. 
CamillaDSP has two special biquad filters, one called "Bass" and the other "Treble" that are user configured and can act as old fashioned tone controls or can be used to add a "house curve". They appear on the GUI under the "Shortcuts" tab as sliders and like the Volume control slider take effect immediately.

CamillaDSP suggests Bass : Lowshelf, Frequency=85Hz, Q=0.9 
and Treble : Highshelf, Frequency=6500Hz, Q-=0.7 .
![alt text](<Images/Pi Screen Shortcuts Tab.jpg>)


I like the Harman curve for loudspeakers, these filters are close -
Bass : Lowshelf, Gain=5db, Frequency=90Hz, Slope=12db/oct and 
Treble : Peaking, Gain=2db, Frequency=22,000Hz, Slope=3db.

I run my system with a 10.1" touch screen so can tickle the tone controls depending on the music. See https://github.com/wirrunna/CamillaDSP-an-implemantation

Here are REW measurements of some of the filters available:
![alt text](<Images/REW V5.40 FS Bass+6 Treble +2.jpg>)
REW V5.40 FS Bass+6 Treble +2.jpg

![alt text](<Images/REW V5.40 FS Tilt -10db.jpg>)
REW V5.40 FS Tilt -10db.jpg

and a Loudness control
![alt text](<Images/REW V5.40 FS CDSP level -37db, -44db and -50db Bass 6 Treble 2 Loudness Hi boost +2 Lo boost +6 Ref Level -35.jpg>)
REW V5.40 FS CDSP level -37db, -44db and -50db Bass 6 Treble 2 Loudness Hi boost +2 Lo boost +6 Ref Level -35.jpg

https://www.audiosciencereview.com/forum/index.php?threads/a-collection-of-speaker-target-responses-in-csv-txt-format.16401/
