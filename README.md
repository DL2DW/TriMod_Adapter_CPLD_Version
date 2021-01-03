# TriMod Adapter CPLD Version

![](https://github.com/DL2DW/TriMod_Adapter_CPLD_Version/blob/main/Images/TriMod_Adapter_CPLD_Version.jpg)



By the middle of 2019, I had developed the TriMod adapter. An adapter that turns the Commodore floppy drive model 1451 into a model 2031LP.

The two drives differ actually only by the interface with which this is connected to the computer.

While the 1541 was primarily developed for the Commodore C64, this one has the "CBM bus" or sometimes called "IEC". 

The 2031 on the other hand has a GPIB or IEEE-488 interface and can thus be connected to the "big" CBM machines or the PET.

If you look at the schematics of the two drives, there is actually only one small difference, and this is to be found on slot UC3 of the VIA6522.

This is basically only that port A is not used on the 1541, and port B provides the lines for the CBM bus (port A was therefore used for later extensions, such as SpeedDOS).

With the 2031, port A is used for the data lines and port B for the control lines. Additionally the well known GPIB port drivers from Texas Instruments are used (SN75160 and 75161).

In simplified terms, these are the differences.

In the 80's, Andre Fachat had already taken up this idea, and presented a corresponding adapter in the magazine 64'er, which turns the 1541 into a 2031. For this, an adapter socket was simply plugged under the VIA 6522. 

Additionally, the Kernal ROM had to be exchanged accordingly.

But then only the IEEE-488 mode could be used.

I had then developed a switchable version that could switch lines using CD4066. So both modes were usable, although of course not at the same time.

I had already decided on the name "TriMod" at that time, because I also wanted to make the parallel cable for a floppy speeder switchable.

Since this would have been too much effort with the 4-way switches, and especially the board would have been much too big, I built a parallel version that uses a CPLD for this purpose.

In autumn 2019 I had finished another version of the TriMod adapter. This one could not only switch between IEC and GPIB, but also switched the parallel cable.

To my knowledge, this made my interface the first ever to be able to switch the parallel lines of port A for an eventual floppy speeder. Also, my adapter seems to have been the first **working** adapter at that time (End of 2019) that used a CPLD.

In the meantime [Jim Brain from RETRO Innovations](https://github.com/go4retro/Nu2031/) has finished a corresponding adapter or the code for it. However, like my first adapter, it can only switch between IEEE-488 and CBM bus. So far this adapter cannot handle a parallel floppy speeder.

Since I had built a replica of the 1541 motherboard in early 2019, this TriMod version was just to develop the appropriate code. This later found its use on my current NextGen1541 board, which already brings the GPIP and parallel port interface from home.

That was also the reason why I never published this adapter.

However, if there should be interest in it, there would be the possibility to develop and publish a small installable version.



# License

The contents of this repository are released under the following license:

- the "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License" (CC BY-NC-SA 4.0) full text of this license is included in the [LICENSE.CC-NC-BY-SA-4.0](https://github.com/DL2DW/TriMod_Adapter_CPLD_Version/blob/main/LICENSE.CC-NC-BY-SA) file and a copy can also be found at https://creativecommons.org/licenses/by-nc-sa/4.0/
