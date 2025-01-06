# flysky sm100
my notes and software for the flysky sm100 usb adapter. these are the settings and actions I used to successfully configure my FrSky Taranis x9d as a game controller in Windows 10 to fly aircraft in the following simulators:
<li>RealFlight 9.5</li>
<li>Tryp FPV</li>
<li>MissionPlanner (RC Control over telemetry radio)</li>

# purchase
Flysky sm100 usb simulator adapter is a device commonly found on ebay, which allows drone pilots and rc pilots to connect their radio transmitters to a computer. One end connects to the usb port of a windows pc, the other end is a mono audio signal cable 3.5mm plug which plugs into the trainer port on the rc transmitter. on the X9D, looking at the back it is the port on the left labeled DSC. The other port is for headphones and will have the headphones logo pictured above it, and will not work for these purposes. 

<img src="https://github.com/joshbasquez/flysky_sm100/blob/main/images/usbppm.png" width="200">

ebay sellers:
https://www.ebay.com/itm/195546780052

# Connect to Windows
Device driver is typically installed automatically by windows after plugging in to USB port. 

One ebay seller of these adapters recommended the following url for manually downloading the required drivers (external link):
https://www.majorgeeks.com/files/details/fms.html

Once drivers are installed, click the start button and type "USB Game Controllers". Look for device called PPM. Click to highlight, and click on Properties.

<img src="https://github.com/joshbasquez/flysky_sm100/blob/main/images/win10_usb_controllers.png" width="250">

<b>Leave this device window open</b>, plug the mono plug into the rc transmitter, and proceed to the next section to configure the transmitter.

# configure Transmitter
Be advised that I was only able to achieve 7 channels output on my x9d, although I believe with some work I could get an 8th channel working. However, the 7th channel takes some calibration work and it is much simpler to configure only 6 channels if possible. TODO: add notes for Ch7/8.

For this step be sure to turn on the transmitter if it is not already on, and have the adapter cable plugged into the 3.5mm trainer port labeled DSC. The adapter typically comes with additional adapters that look like a large and a small ps/2 plug, intended I believe for older transmitters such as Futaba or 

First, in the x9d, create a new model or copy a basic plane model to an open slot. On Page 2 (model setup), set a name and scroll down to RF settings.
Internal RF: Mode OFF. 
External RF: Mode OFF. 
Trainer Port: Mode Slave. Channel Range: CH1-6. PPM Frame: 22.5ms, 300u -.

Move to Page 5 Inputs, and setup the main 4 channels for Ail, Ele, Thr, and Rud 100. 

For the Aux switches, on x9d I use Page 11 (Special Functions) to configure 3 position switches for CH 5 and Ch 6. 

for example, for CH 5 I have configured:
SF1 SC^ OverrideCH5 100  enabled.
SF2 SC- OverrideCH5 0    enabled. 
SF3 SCv OverrideCH5 -100 enabled. 

which gives me a high, medium and low value for that channel. Repeat previous steps to configure for Channel 6 (I used Switch SA). 

# Confirm controller input
Look back at the windows usb controller window, moving the sticks around and toggle the switches configured for channel 5 and 6, to confirm movement is seen on the controller screen. 

<img src="https://github.com/joshbasquez/flysky_sm100/blob/main/images/usb-ppm-properties.png" width="200">

If the sliders and other axes show movement corresponding to the transmitter movements and switches, contratulations you are all set. 

Proceed to the game to map the controller inputs to the game's aircraft controls. 
