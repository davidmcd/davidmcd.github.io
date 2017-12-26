---
published: true
layout: post
tags:
  - IOT
  - HolidayProjects
---
## Azure IOT Starter Kit - #5 on Holiday Techie Fun Project List
The day after Christmas is in some ways the second best day of the year.  It's the perfect day to do whatever you want with no obligations.  I'm playing with my toys!  One of them is the [MXCHIP IoT DevKit](https://aka.ms/iot-devkit).  

Today I started by setting up the device and getting it on my Wifi.  I installed the local dev libraries including the Microsoft Code integrated samples.  Both of these setups are in the [Getting Started Guide](https://microsoft.github.io/azure-iot-developer-kit/docs/get-started/).

Next I dove into the sample [Connect to Azure IOT Hub](https://microsoft.github.io/azure-iot-developer-kit/docs/projects/connect-iot-hub/).  This was pretty darn easy to setup.  It automates the setup of a free-tier IOT Hub in your azure subscription.  Then it publishes their simple arduino app to the MXChip DevKit device.  The app polls the temp and humidity every second and sends it to the IOT hub.  You can connect to the device to monitor the sending of the data.  However the example was somewhat unsatisfying because it didn't show me how to see the data on teh Azure side.  

In order to be able to monitor the data I wanted to be able to see a real-time update through PowerBI.  Fortunately that was pretty easy too.  [Realtime visualization of sensor data](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-live-data-visualization-in-power-bi) includes the steps to create a Stream Analytics and publish the data to PowerBI.  Within PBI you just create a report that shows the Temp and Humidity data.  Voila, device to visualization in no time.  

One next step would be to convert the data from celcius to farenheit  That will require PBI desktop.  Another item is that the free tier is limited to 8K messages per day.  I should change the code to post less frequently (like very 10 seconds instead of every second).  