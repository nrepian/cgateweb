cgateweb
========

MQTT interface for C-Bus written in Node.js

Usage:

1) Put your settings in settings.js
2) Run node index.js

Detailed guides and supporting articles will be posted on my blog: https://blog.addictedtopi.com/category/project/cbus/

Updates get published on these topics:

cbus/read/#1/#2/#3/state  -  ON/OFF gets published to these topics if the light is turned on/off

cbus/read/#!/#2/#3/level  -  The level of the light gets published to these topics

Publish to these topics to control the lights. Wildcards don't work:

cbus/write/#1/#2/#3/switch  -  Publish ON/OFF to these topics to turn lights on/off

cbus/write/#1/#2/#3/ramp  -  Publish a % to ramp to that %. Optionally add a comma then a time (e.g. 50,4s or 100,2m). Also, INCREASE/DECREASE ramp by 5% up or down and ON/OFF turns on/off. 

This requests an update from all lights:

cbus/write/#1/#2//getall - current values get published on the cbus/read topics

 #1,#2 and #3 should be replaced by your c-bus network number, application number, and the group number.

Other notes:
I made this for working with OpenHAB
It assumes the default cgate ports
