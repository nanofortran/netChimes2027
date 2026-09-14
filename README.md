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
  2. The RAKwireless 19003 base which provides USB serial programming, solar charging/powering circuitry, battery connectivity, and basic GPIO to the microcontroller: https://www.amazon.com/RAKwireless-WisBlock-Meshtastic-Starter-RAK19003/dp/B0DFMMTQZM/ref=sr_1_2?crid=31QK5KZ9U5E8A&dib=eyJ2IjoiMSJ9.vAQkfnF6Tfq_hOLJDW4BbYI0Te-jCuKKoGat-sFLnPBv-GmmQXdSll5smpB_6gkI_F9hij-ynLdGmS2FMHj2oyclOg4oj1n0oIC4Wx1GxhcfR643q2OzCs1hOpIXumd52nomlLHhqXyh6CQC7HoDkTNonm3SARh4E4of8ti54OJvEKqb3B-BIwEvLXplr-2YhaEe141CTaggsTsRQNomuHwauZZMcDeVc6T_pByAvqw.5ORZzQFi6U8hpOcH2ym5YyyLy1nCqXwO4j7NINcepdA&dib_tag=se&keywords=rak%2Bwireless%2Bwisblock&qid=1789422313&sprefix=rak%2Bwireless%2Bwisblock%2Caps%2C177&sr=8-2&th=1

     Note: The 4631 and 19003 are often sold together as a Meshtastic starter kit packaged with other accessories such as antennas: 

