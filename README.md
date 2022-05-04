# Pana4
Repository for STM32 based Panadapter Firmware
This project was intended to a an add-on for the Pic-A-Star HF transceiver.  Pic-A-Star is a high performance, 
homebrew transceiver developed by Peter Rhodes (G3XJP).  It was first published in Radcom, the magazine of the 
Radio society of Great Britain (RSGB) in the early 2000s.  Most of the functionality was performed digitally 
using digital signal processing (DSP).  The first IF (intermediate frequency) was at 10.7 MHz.  

The objective of this project was to sample the signal from the 10.7MHz IF, use a "Tayloe" mixer to 
convert the signal to the audio spectrum, with both the in-phase (I) and quadrature (Q) components.  
Use an analogue to digital converter (ADC) to allow the I and Q components to be processed in a 
suitable microcontroller, and display the bandscope on a graphical liquid crystal (lcd) display.  

The "front end" Tayloe mixer was a direct copy of the receive portion of the mcHF transceiver 
(http://www.m0nka.co.uk/?page_id=2).  The Si5351 local oscillator is clocked at four times the 
IF frequency, before being divided by four to produce the quadrature output signals needed to 
clock the Tayloe mixer.  The microcontroller was the STM32F407G-DISC1 Discovery development 
platform.  The display is a 2.8in TFT LCD module, model HY28B, driven via the Serial Peripheral 
Interface (SPI).  

The coding was done using the Eclipse Integrated Development Environment (IDE).  

Never got as far as attaching it to the Pic-A-Star transceiver, not sure why I stopped working on it, 
it just got pushed off the work-bench...  

If I was starting again, I'd probably still use the Tayloe front end, but use a Teeensy 
microcontroller and its audio shield.  

Jim Smith - G3ZQC
