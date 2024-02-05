---
draft: false
title: Hacking together a Zigbee bed sensor with no soldering
subtitle: A quick and easy way of creating a new sensor # Optional
date: 2024-02-01
description: >-
  A small list of my favorite games that I played this year, but not necessarily new games.
tags:
  - home assistant
  - home automation
---
For a long time I wanted to have a presence sensor that could see if I was laying on my bed.
But never quite found what I needed, until now. I'll show you how I managed to make an usable bed (and chair!)
sensor for cheap with easy to get parts and no soldering.
<!--more-->

{{<admonition title="Information" bg-color="#00ee88">}}
This article contains links to produtcs on Amazon and other sites, but none of them are part of an affiliate or similar and I do not get any money if you choose to purchase any of the products. 
{{</admonition>}}

## The What
I wanted to sense whether or not I was lying on my bed for some automation ideas that I had on mind, but my search for ready to go solutions turned out futile (except for [super expensive devices](https://www.sleepnumber.com/)). But in my quest for the right device I found out about other people making their own bed sensor out of parts! Here are the videos that inspired me: [link1](link) and [link2](link2).  
 
Basically, all you need to do is to get a sensor that can feel when something is pushing on it and outputs a true or false signal, and something to connect it to your home automation system.  
This could be done in one of many ways, for the sensor you can get something like this [car seat sensor](link), or this [mat sensor](link). And as for the device, you can use something like.  
 
I will show you how how I made mine and a few alternatives that you can try, and I will also show you how to integrate with with you existing Home Assistant.  

## Materials

- Mat sensor or seat sensor
- Aqara Zigbee door sensor
- Wire cutters
- Wire strippers
- Electrical tape (optional)
- Soldering Iron and lead (optional)

### - Mat or seat sensor

There are two main options here, you can either get a [car seat safety sensor](https://www.amazon.com/gp/product/B09WDCWX8K/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1), or a [pressure mat alarm](https://www.amazon.com/gp/product/B00GUNX7WY/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1). There may be other options out there, but the important part is that they must have only two wires coming oout of them, and that the sensor closes/opens the circuit depending on whether pressure is applied on them or not. My recommendation for a bed sensor is the pressure mat, while the car seat sensor is more suited for chairs.

### - Zigbee door sensor

Door sensors are usually just simple on/off reed switches that come with a magnet, so they are a perfect pair to an open/close sensor like our mat. In my case I will use [Aqara door sensors](https://www.amazon.com/s?k=aqara+door+sensor&crid=13UU5JI6Y5976&sprefix=aqara+door+senso%2Caps%2C123&ref=nb_sb_noss_2) ones, they are easy to get and also have a nice enough quality. But you can choose any other brand that you preffer. 
[Water leak sensors](https://www.amazon.com/Aqara-Water-Leak-Sensor-Kit/dp/B09WQPJBTQ/ref=sr_1_5?crid=1C3GQ7KP397QR&qid=1707037192&sprefix=aqara%20water,aps,146) also seem to be a great option, but I haven't personally used them.
You can also use Z-Wave sensors if you want.

## How-to make the sensor

### Open your sensor and identify the reed switch

You will be able to open most sensors just by prying with a thin tool like a guitar pick or a flat scredriver.
Some of them might have screws, but these are more rare.  
Be sure to open only the part that is bigger (it probably has a small light and button too), the small part is just a magnet.  

[photos]  

Once it is open you need to identify the reed switch and its two sides. If you are using the Aqara this is very wasy to do, the switch is big and its poles (or sides) are easily accesible.  

[photos]  

Other sensors are different and harder to work with. I've tried with [this](https://www.amazon.com/gp/product/B09W8F3ZV1/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1) Tuya sensor, and it uses a different style of reed switch which is smaller and much harder to work with. Unfortunately I don't have a picture of it.

### Prepare your pressure mat

You need the pair of bare wires that are comming out of your pressure mat. Its possible that they already come like that, but they usually come with a plug already on them. You simply need to cut that off and strip off about 2cm of the insulation.  

[photos]  

### Connect the stuff
