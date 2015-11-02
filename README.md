# Thiking Things Open 2 FIWARE IoT Stack Integration

## Introduction
This repository holds examples about how to persist your Thinking Things Open sensors data into FIWARE IoT Stack cloud service.

Then, it will show you how to access these data using FIWARE NGSI standard APIs and its multiple connectors with external tools as Freeboard or CartoDB.

### First steps on your Thinking Things Open
If you are new with Thinking Things Open, we recommend you going first to [Thinking Things website](http://www.thinkingthings.telefonica.com/beta/index/). Also, you can find a lot of examples and tutorials at [Thinking Things Github](https://github.com/thinkingthings/Arduino)

### What is FIWARE IoT Stack?
[FIWARE](https://www.fiware.org/) is an open initiative aiming to create a sustainable ecosystem to grasp the opportunities that will emerge with the new wave of digitalization caused by the integration of recent Internet technologies. Based on this FIWARE technologies, and focused on IoT area, Telefonica created and [IoT Platform](http://iot.tid.es) to help Industrial Partners and Smart Cities building its IoT services. 

This FIWARE IoT Stack is also available for independent developers and startups, and will be used in this tutorial to persist your Thinking Things Open data in the cloud. You can go to its [ReadTheDocs](http://fiware-iot-stack.readthedocs.org/en/latest/index.html) to get familiar with it. 

NOTE: If you are a hacker participating in the [openbank Internet of Things Day Hackaton](http://internetofthingsopenbank.com/) You can get your FIWARE IoT Stack credentials [here](http://signuphackathon.ttcloud.net/)

If you are not, [contact us](mailto:iot_support@tid.es) and we will give you the steps to get access.


## Arduino sample for Thinking Things Open
If you are an Arduino lover, [this .ino example](/arduino) will be straightforward for you.

## Using FIWARE IoT Stack
You have your Thiking Things collecting data from sensors. So what?

Next step is connecting your applications with FIWARE IoT Stack to access your data and show your magic to the rest of the world.

### Step #1: Sign up to get your credentials
You can get your FIWARE IoT Stack credentials at [http://signuphackathon.ttcloud.net/](http://signuphackathon.ttcloud.net/).

You will receive an email with your API and portal credentials to send data from your Edison and use FIWARE IoT Stack APIs on your App.

Please, in case you have any trouble signing up let us know at [iot_support@tid.es](mailto:iot_support@tid.es)

### Step #2: FIWARE IoT Stack Management Portal
To check your data is correctly sent and stored, first thing is accessing the [Management Portal](http://hackathon.ttcloud.net/openbank). You can log-in using your given FIWARE user/password. In the "Entities" section (An Entity is a data object representation in FIWARE, so your Edison is represented as an Entity) you will find an Entity called "device:myTT" with a list of attributes:
* "l": Your luminosity sensor
* "p": Your button sensor

If you have connected more sensors to your ThikingThings, they will appear here with the given alias you selected in the arduino code.

If you want to, you can go to "Devices" section to provision a device for your Edison. For example, you could change your Entity ID (setting "home" instead of "device:myTT" or "luminosity" instead of "l"). Check [this guide](http://fiware-iot-stack.readthedocs.org/en/latest/quickguide/index.html#step-2-see-data) for more details

### Step #3 : Drag&Drop visualizations with Freeboard
If you just need a dashboard (like [this one](https://freeboard.io/board/0cYCHY) ) to show your sensors data in real time, you can create it using [Freeboard](https://freeboard.io) without writing a line of code. 

Please, read our 
[FIWARE Orion Datasource Freedboard Tutorial](http://fiware-iot-stack.readthedocs.org/en/latest/quickguide/index.html#step-4-show-in-a-dashboard) if you have any trouble.

### Step #4 : Use FIWARE NGSI APIs
If you want to build your own app, with your own code and UX, you are looking for an API, right?. 

Integrating external apps is done via [NGSI APIs](https://forge.fiware.org/plugins/mediawiki/wiki/fiware/index.php?title=Publish/Subscribe_Broker_-_Orion_Context_Broker_-_User_and_Programmers_Guide). [Here](http://fiware-iot-stack.readthedocs.org/en/latest/quickguide/index.html#step-3-get-data)
you have a getting started tutorial to start working with these APIs.
