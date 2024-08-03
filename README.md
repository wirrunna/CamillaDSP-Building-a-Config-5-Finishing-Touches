# CamillaDSP-Building-a-Config-5-Finishing-Touches
5. Fix up a few bumps and potholes in the SPL and add Bass &amp; Treble controls

### Add Input channel EQ
When the crossover in practice does not perform like the crossover in theory we are often left with some bumps and potholes in the SPL that bridge two drivers and therefore are difficult to EQ on a driver by driver basis. The solution is to measure the Full System SPL, get REW to calculate the EQ required, then add the filters to the Input channel.

So, here is the SPL-
![alt text](<Images/Jun 23 2 T44_A67 new pf - no input peqs.jpg>)
 

EQ settings - 
![alt text](<Images/EQ Jun 23 4 T44A 77db TL76.3 20-20k 1db.jpg>)




These filters are saved and then imported into the Config file, here is a section of the Input in the pipeline.
![alt text](<Images/CamillaDSP GUI, Pipeline tab showing input filters.jpg>)


Here is a REW sweep with the input PEQs/Biquad filters applied
![alt text](<Images/Jun 23 5 T45_A67 FS 77db new pf input peqs.jpg>)



The Pipeline showing the Biquad group of EQ filters in the input
![alt text](<Images/CamillaDSP GUI Pipeline plot collapsed.jpg>)

### Add "Tone Control" filters. 
CamillaDSP has two special biquad filters, one called "Bass" and the other "Treble" that are user configured and can act as old fashioned tone controls or can be used to add a "house curve". They appear on the GUI under the "Shortcuts" tab and must be applied and saved for them to take effect. 

CamillaDSP suggests Bass : Lowshelf, Frequency=85Hz, Q=0.9 
and Treble : Highshelf, Frequency=6500Hz, Q-=0.7 .
![alt text](<Images/CamillaDSP GUI Shortcuts.jpg>)


I like the Harman curve for loudspeakers and so set 
Bass : Lowshelf, Gain=5db, Frequency=90Hz, Slope=12db/oct and 
Treble : Peaking, Gain=2db, Frequency=22,000Hz, Slope=3db.

Add a jpg of All SPL - flat response, Bass +6 Hi -3 

https://www.audiosciencereview.com/forum/index.php?threads/a-collection-of-speaker-target-responses-in-csv-txt-format.16401/
