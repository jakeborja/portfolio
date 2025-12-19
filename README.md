# **Hey this is My Portfolio/Blog thing.**

This is where I want to document all the projects I do. Especially in **Project Smart Bus.** Come back and see some other projects I have in mind\!
<details>
<summary> Project Smart Bus </summary>

This is an ongoing project that I took on about 7 months ago. The point of this Project was to pack as many high tech projects into an off grid 40ft School Bus turned tiny house. If you ask my partner it was so we had a place to live moving up the coast with our three kids, two dogs, and newly aquired hamster. Regardless it's a labor of love and not as practical as I anticipated but alas here we are.

I should probably get this out of the way now. My views on living in a skoolie have changed since starting. I personally can't wait to not live in this bus full time anymore. It's not as doable with kids. Although... Project Smart House Boat coming soon.

This isn't a "Build a Skoolie Guide." I am **N O W H E R E N E A R** an authority on the subject. In fact if anyone tells you they are... well they're a ***liar.*** 

This is more to help keep things in mind if **you** decide to do something objectivly reckless like convert a school bus. 

First I'll Document the "major hardware." Then I'll go into how they work together and some of the problems I've found. Thirdly I'll talk a bit about some services and software I'm running. Last I'll tell you about some super fun projects I'd LIKE to implement as time comes.

<details>
<summary>Hardware</summary>

* a Lenovo ThinkCentre mini pc running [Proxmox](https://proxmox.com/en/)  
* A [Chester Tech Repair 5g Router](https://chestertechrepairs.com/products/5g-cheetah-v2-%F0%9F%90%86-dual-sim-wi-fi-6-industrial-lte-nr5g-wireless-modem-router-bundle-fixed-wireless-access-point-can-work-mobile)  
* A [Waveform 4x4 antenna](https://www.waveform.com/products/quadmini)  
* a Raspberry Pi 5 8gb  
* a Raspberry Pi 3b (honestly this is my kick around pi and rarely used)  
* a Cisco Small Business Switch  
* more smart products than I'd like to admit.

### Let's Start With The Obvious
Given enough money ***anyone*** can create a "smart bus" with off the shelf smart gadgets. Being the pretentious and slightly hypocritical man that I am I don't constitute this as a "Smart Bus." Hell I dont even count ***MY*** bus as a full fledged smart bus yet. Because of this I have defined "Smart Bus" as such: 

**Smart Bus** (*Noun*) : 
Any bus, camper, or Skoolie that utilizes technology to control most if not all aspects of its interior and exterior incuding engine and mechanical sensors.

***That Being said...***
### Smart Gadgets
Like other Nerdy Nerds I went down the rabbit hole. Coming out of that hole I ended up with some Smart Bulbs, a few Sensors, and a Smart Tea Kettle.

<details>
<summary>Smart Bulbs and Lighs</summary>

I know what i just said but that doesnt mean you DONT get smart bulbs. They make things SOOOO much better during your build and if you plan this ahead of time you can avoid wiring so many light switches. Also the are enharently dimmable so thats a huge plus. Smart bulbs need constant power to work. its such a small amout that it doesnt even register on out Bluetti Power station.

Instead of telling you what bulbs to get I'll tell you this...
***PICK A BRAND AND STICK WITH IT***
As much as you can duct tape them all together in Home Assistant, I promise you it's WAAAAAAAY easier if you only have to set up one Integration/HACS/ADDON.

I choose IKEA. They're typically Zigbee and always super cheap, which is great because a bus build is FREAKING EXPENSIVE. If you get a kit, you get a hub. The Dirigera Hub is a Zigbee gateway. I've been able to hook all kinds of other Zigbee things to it but your mileage may vary. All in all, these are my go-to. Also, it gives me an excuse to play hide-and-seek in IKEA while eating meatballs. What's not to love?

Govee is kind of a pain in the nuts. The app is great and remote. Also, if your internet happens to be down, you can use Bluetooth. The Govee Home Assistant integrations are shoddy. Not in a bad way, but it's WAY more involved than the IKEA integration. You typically need to go into the app and request an API, then go back into Home Assistant. If that's okay with you, awesome. But I'm lazy and who wants to fight with a light bulb?

You'll probably want exterior lights and as much as I just said Govee isn't great with Home Assistant, they do have some great permanent exterior lights that I plan on using for the top of the sides of my bus.

I have yet to try the famous Hue lights and in all honesty, I don't plan on getting any anytime soon. Mainly because they're expensive and I already have light bulbs...

I should probably mention at this point you'll want to get an MQTT Broker set up. Home Assistant has a pretty easy way to do this. I'll talk more about this in the "Services" section under Home Assistant.

You will spend a lot of time wondering if you need RGB lights. I'll make it easy for you... you probably don't, but don't let me stop you. Honestly, I have a touch of the 'tism and any light other than warm and soft isn't allowed in my dwellings. Except my mini disco ball. That stays.
</details>
<details>
<summary>The Tea Kettle</summary>

Ok here is where it gets silly. I dont know why but in my early days of smart gadget obsession I wanted EVERYTHING to be smart. If you Google any product with "smart" at the end of it you'll find thousands of different products all with different apps. My rule of thumb is if the app look like crap it's probably not great but I've found the opposite to be just as frusterating. If an app is OVER pollished there's probably something else you need to pay for monthly and that doesn't sit well with my cheap ass. 

Govee actually has a pretty good app and they have some funky products. Such as Smart Tea kettles. I have this [gooseneck one.](https://www.amazon.com/Govee-Electric-Gooseneck-Temperature-Stainless/dp/B09TSKDKCL/ref=sr_1_1?adgrpid=184161636177&dib=eyJ2IjoiMSJ9.GZno-Ryd8wmPREFuo98jvAJG0x2OmNal1ML9zKuxGGgjeRP8RzXXyeOf2Ypfkour6iFh0feQ1f5-z4c5w9avJHTRktVDJLT-DSCesIRRY62ho1Dv-oHGBqZ32DLfeMh39oaqzYo0_KfqX6tjhJB7W1uOnwaY3_u0HPfffBv23-k7vM1_bRPPCWfy-YrqffYa37zRf7jUGGFTaSkXf0iKscE8FYUwRQ_zSW0SGNOO9nNIWRhbozVxEi4IwG8MVJJOAs81wlyh4qDa-1zdLJYY_xGxQTJOulNE_Rzs1TnBXMA.arf4grhL-hDcT4rxDKcB22J8FY74jblBFUolT1SupFs&dib_tag=se&hvadid=779522324841&hvdev=c&hvexpln=0&hvlocphy=9032382&hvnetw=g&hvocijid=7012697677609333789--&hvqmt=e&hvrand=7012697677609333789&hvtargid=kwd-2244502331656&hydadcr=20248_13318798_1285226&keywords=govee+gooseneck&mcid=0252854242543e8bb0bd43105ffee3c5&qid=1766047536&sr=8-1) Why does this need to be smart? It doesn't. Is it cool? well I can start my tea kettle from around the world and get an exact temperature for my coffee. Other than timers and a Stay Warm feature thats about it. If I spent any more than I would have spent on a regular electric tea kettle it wouldnt have been worth it. 

This is me saying not ***everything*** needs to be "smart." Infact sometimes it's more of headache if they are! I'm looking at you smart toaster in my Amazon shopping cart. 

</details>

</details>

<details> 
<summary>How It All Goes Together</summary>
</details>

<details> 
<summary>Software and Services</summary>
</details>
