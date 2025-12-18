# **Hey this is My Portfolio/Blog thing.**

This is where I want to document all the projects I do. Especially in **Project Smart Bus.** Come back and see some other projects I have in mind\!

## **Project Smart Bus**

This is a project that I took on about 7 months ago. The point of this Project was to pack as many high tech projects into an off grid 40ft School Bus turned tiny house. It's for sure a labor of love and not as practical as I anticipated but alas here we are.  

This isn't a "Build a Skoolie Guide." I am **N O W H E R E N E A R** an authority on the subject. In fact if anyone tells you they are... well they're a ***liar.*** 

First I'll Document the "major hardware." Then I'll go into how they work together and some of the problems I've found. Last I'll tell you about some super fun projects I'd LIKE to implement as time comes.

### Currently Project Smart Bus has:

* a Lenovo ThinkCentre mini pc running [Proxmox](https://proxmox.com/en/)  
* A [Chester Tech Repair 5g Router](https://chestertechrepairs.com/products/5g-cheetah-v2-%F0%9F%90%86-dual-sim-wi-fi-6-industrial-lte-nr5g-wireless-modem-router-bundle-fixed-wireless-access-point-can-work-mobile)  
* A [Waveform 4x4 antenna](https://www.waveform.com/products/quadmini)  
* a Raspberry Pi 5 8gb  
* a Raspberry Pi 3b (honestly this is my kick around pi and rarely used)  
* a Cisco Small Business Switch  
* more smart products than I'd like to admit.

### Let's Start With The Obvious
Given enough money ***anyone*** can create a "smart bus" with off the shelf smart gadgets. Being the pretentious and slightly hypocritical man that I am I dont constitute this as a "Smart Bus." Hell I dont even count ***MY*** bus as a full fledged smart bus yet. Because of this I have defined "Smart Bus" as such: 

**Smart Bus** (*Noun*) : 
Any bus, camper, or Skoolie that utilizes technology to control most if not all aspects of its interior and exterior incuding engine and mechanical sensors.

***That Being said...***
### Smart Gadgets
Like other Nerdy Nerds I went down the rabbit hole. Coming out of that hole I ended up with some Smart Bulbs, a few Sensors, and a Smart Tea Kettle.

**Smart Bulbs**
Instead of telling you what bulbs to get I'll tell you this...
***PICK A BRAND AND STICK WITH IT***
As much as you can duct tape them all together in Home Assistant, I promise you it's WAAAAAAAY easier if you only have to set up one Integration/HACS/ADDON.

I choose IKEA. They're typically Zigbee and always super cheap, which is great because a bus build is FREAKING EXPENSIVE. If you get a kit, you get a hub. The Dirigera Hub is a Zigbee gateway. I've been able to hook all kinds of other Zigbee things to it but your mileage may vary. All in all, these are my go-to. Also, it gives me an excuse to play hide-and-seek in IKEA while eating meatballs. What's not to love?

Govee is kind of a pain in the nuts. The app is great and remote. Also, if your internet happens to be down, you can use Bluetooth. The Govee Home Assistant integrations are shoddy. Not in a bad way, but it's WAY more involved than the IKEA integration. You typically need to go into the app and request an API, then go back into Home Assistant. If that's okay with you, awesome. But I'm lazy.

I have yet to try the famous Hue lights and in all honesty, I don't plan on getting any anytime soon. Mainly because they're expensive.

I should probably mention at this point you'll want to get an MQTT Broker set up. Home Assistant has a pretty easy way to do this. I'll talk more about this in the "Services" section under Home Assistant.

You will spend a lot of time wondering if you need RGB lights. I'll make it easy for you... you probably don't, but don't let me stop you. Honestly, I have a touch of the 'tism and any light other than warm and soft isn't allowed in my dwellings—except my mini disco ball.
