# netChimes2027
A new take on an old idea, netChimes for a newer generation.

# Overview
netChimes is a globally-distributed sensor array network actuated by the ambient motion of the wind. Sensor data is delivered to the network in realtime to direct/drive ambient or otherwise generative processes. The project is composed of 4 parts:

1. Local wind chime sensors,
2. Wind chime nodes/gateways,
3. The netChimes server(s), and
4. An installation, application, object, or other project that is directed by real-time data traversing the system.

# The wind chime sensor
The wind chime sensor is a standalone, solar-powered sensor supporting a hanging sail which catches the wind. The sail is attached to the sensor body by 3d printable neck and collar which is attached to a water proof/resitant enclosure. The enclosure houses the following components:
  1. RAKwireless 4631 development board containing the RAk463 module with LoRa and Bluetooth
  2. The RAKwireless 19003 base which provides USB serial programming, solar charging/powering circuitry, battery connectivity, and basic GPIO to the microcontroller. 

     Note: The 4631 and 19003 are often sold together as a Meshtastic starter kit packaged with other accessories such as antennas [as seen here.](https://www.amazon.com/RAKwireless-WisBlock-Meshtastic-Starter-RAK19003/dp/B0DFMMTQZM/ref=sr_1_2?crid=31QK5KZ9U5E8A&dib=eyJ2IjoiMSJ9.vAQkfnF6Tfq_hOLJDW4BbYI0Te-jCuKKoGat-sFLnPBv-GmmQXdSll5smpB_6gkI_F9hij-ynLdGmS2FMHj2oyclOg4oj1n0oIC4Wx1GxhcfR643q2OzCs1hOpIXumd52nomlLHhqXyh6CQC7HoDkTNonm3SARh4E4of8ti54OJvEKqb3B-BIwEvLXplr-2YhaEe141CTaggsTsRQNomuHwauZZMcDeVc6T_pByAvqw.5ORZzQFi6U8hpOcH2ym5YyyLy1nCqXwO4j7NINcepdA&dib_tag=se&keywords=rak%2Bwireless%2Bwisblock&qid=1789422313&sprefix=rak%2Bwireless%2Bwisblock%2Caps%2C177&sr=8-2&th=1)
     
AS sensor to gateway communication is via LoRa (LOw power RAdio) utilizing the ISM (Industrial, Scientific, and Medical) frequencies. Frequencies vary from region to region (North American, Europe, Asia, etc.) and it is up to the participant to work within the frequencies allowed to them and secure the right modules for their region.

  3. An AHT20 temperature and humidity sensor with I2C, available [here](https://www.adafruit.com/product/4566) and elsewhere.
  4. A VEML7700 Lux Sensor with I2C, available [here](https://www.adafruit.com/product/4162) and elsewhere.
  5. A MCP23008 digital I/0 expander, available [here](https://www.adafruit.com/product/593) and elsewhere.
  6. 6  hall effect sensors (non-latching/omnipolar). There are may variations out there, but they must be non-latching and only activated (pulled to ground) when a magnet passes over them. These [AH1815s](https://www.sparkfun.com/hall-effect-sensor-ah1815-non-latching.html) should do the trick.
  7. A protoboard to connect all the components together. I am open to having someone sketch up a Gerber file so we can print our own, but as we are still in development we might hold off. Something like [this](https://www.adafruit.com/product/1609).
  8. External LoRa antenna like [this](https://www.digikey.com/en/product-highlight/m/molex/lora-external-antennas). Though a [spring antenna](https://www.adafruit.com/product/4269) housed inside the enclosure may work if the distance to the gateway is  not too far away (actually, I have no idea). Do get the antenna cut for your working frequency, however, otherwise you will burn out the board/radio.
  9. To equalize temperature and pressure I installed one of these [breather vents](https://www.amazon.com/dp/B0GCVF2CM8?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1).
  10. And find an enclosure that is roughly 4x4 inches (100 x 100 mm), preferably with a clear top so the lux sensor can make a reading. Though I might go with an all black box with a DIY window of clear PLA as a black box will warm in the sun and melt snow and ice in the winter months. I just don't know yet.
