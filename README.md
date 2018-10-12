# Project LittleBirds

## Why we chose the silent daemon ?

The forest fires are usually seasonal and various regions have different normal and peak fire seasons. Over 90 per cent of forest fires are man-made, the following report shows the statistics on how much of a damage forest fire can cost.

Inventories conducted by the Forest Survey of India show that on average
 India saw 46% increase in past 16 years and **125% rise in just past 2 years**.
 
 >**55% of forest area in India is affected by fire**
 
A study made by the Forest Survey of India reveals that
* 51% of the forest area in Assam and Gujarat, 
* 93% in Arunachal Pradesh,
*  67% in Bihar, 
* 69% in Himachal Pradesh,
*  46% in Jammu & Kashmir,
*  45% in Karnataka, 
* 76% in Madhya Pradesh,
*  94% in Meghalaya and Orissa,
*  87% in Nagaland,
*  58% in Uttar Pradesh and 
* 33% in West Bengal

have a risk of being subjected to repeated annual fires

India loses around **Rs 550 crore every year** owing to damages caused by forest fires. 
	

## Idea :
One of the major concerns of India is management of Terrestrial Ecosystem. Wildfires are one of those disasters that pose a threat to Terrestrial Ecosystem and often goes unnoticed until far spread. Wildfire (commonly referred to as forest fire) is a Disaster which needs to be managed well at the right time to minimise the damage caused to the ecosystem.  
So, we came up with an idea to have a network of detectors spread across the forest,  helping in faster notification with precise location of disaster occurrence which in turn helps in disaster management and prevention of large scale damage.
 
Also, adding additional sensors like those which can determine the direction of wind can further help in real time analysis and prediction of the rate and direction of spread of fire. Also many other factors can be included to improve prediction.
	
## Implementation :

### How does it work ?
LittleBirds works in 3 modules as mentioned below and are thus designed for flexibility and improvement in each of the modules without affecting the other, the 3 module are
*  Data Collection
*  Data processing
*  Real-time status update

#### Data Collection
This module of the project is responsible for data accumulation and continuous transmission to the processing unit. The data transmission layout is hierarchical with 3 levels of hierarchy as shown below

1) Temperature Sensor Unit (TSU) :
A small self-sustaining temperature-sensing and data transmission unit. This unit depends on solar energy for its power requirements. This unit also has a long range data transmitter which periodically transmits its temperature readings to the local-region-sensor unit (mentioned below).
This typically will be responsible for giving the temperature of a region of about 200-300 SqMeters.

2) Local Region Sensor Unit (LRSU):  This is a small data collection and transmission unit that is responsible for receiving periodic temperature data from the  TSUs , performing minimal data pre-processing and then are used for long-range data transmission to the master-sensor-unit. 
These monitor around 100-150 TSUs each , and thus cover an area of around 5-10 kilometres in radius. 

3) Master Sensor Unit: This unit is located graphically in such a way that the unit is safe from the elements and also closer to all the LRSUs. This unit does more data pre-processing and uploads the collected data to the processing cloud.

The above mentioned units will use the [LoRa Network Protocol](https://www.postscapes.com/long-range-wireless-iot-protocol-lora/) for long range transimission .

#### Data processing
All the collected time-series data is processed on the Azure cloud , Abnormal variations in temperatures are highlighted and reported, algorithms need to be able to keep track of the variations in temperature throughout the day in that specific season.  

#### Real-time status update
The real-time status update from this application can be used to immediately alert the concerned authorities to take action on the matter.
Implementation of this module can be in different methods, such as an emergency broadcast to nearby villages and tourist, This information is more accurate than conventional central pyrometer , and thus more important in saving the vital minutes before the fire gets out of hand.

## Advantages of LittleBirds

* Using the real time data, exact predictions can be made as where the fire is heading and at what speed.
* Cost efficient as sensors are cheap.
* Power consumption is minimal and it is solar powered so maintenance cost is low.
* Neighbouring villages could be alarmed before the fire is spread.
* The forest fire prevention is just one example of its applications, this technology 
* monitoring animal habitat, monitoring health status of bridges
*  can also be used in major areas such as alarm floods, environmental detection, intelligent transportation.