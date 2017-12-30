---
published: true
layout: post
tags:
  - homeautomation
  - HolidayProjects
---
## Google AIY VoiceKit - #7 on Holiday Techie Fun Project List

TOday was a few more hours of geeky fun during my holiday break.  Today's task was to setup and experiment with [Google AIY VoiceKit](https://aiyprojects.withgoogle.com/voice).

#Project Overview
This project demonstrates how to get a natural language recognizer up and running and connect it to the Google Assistant, using your AIY Projects voice kit. Along with everything the Google Assistant already does, you can add your own question and answer pairs. All in a handy little cardboard cube, powered by a Raspberry Pi.

#Thoughts
The setup was pretty easy.  I supplied my own Raspberry Pi 3.  It uses a custom Raspian image downloaded and installed.  The book that comes with the kit is published by MagPi.  Setup took a little over an hour.  It includes a speaker, a special voice recogntion hat and a microphone board.  It was pretty darn easy to setup up.  Setup requires creating your Google Cloud account (free tier) and enabling voice API recognition.  

#Challenge
Ok, I spent more time trying to get the python module to auto-start.  It turns out there there is a developer command prompt that has to be used to run the python, else you get a module load error.  I'm still looking for a solution because i'd like to be able to just plug in the device and have it run so I can just say "Hey Google".  
