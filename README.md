# Mechaphonix
## An experimental multimedia performance suite
The goal of this project is to enable performers to use several different brower devices to interact with a master node.js server that will send MIDI messages to a computer music software system called [ChucK](http://chuck.cs.princeton.edu/) and create visualizations.  

This project will have the following components:
### The Node.js Server
This is primarily responsible for receiving data from the peripheral controllers (phone accellerometers, camera trackers, microphone) via WebSockets (probably [socket.io](https://socket.io/)), doing some magic to them to them and emitting some MIDI that will eventually control the instruments.  It will also serve the front-end, which should be minimal.
### The Front-End
This will consist of a simple menu to choose what controller you are using based on what peripherals the device has available to it (accellerometer, camera, mic), and the code that will actually send the signals through the WebSocket.
### ChucK
[ChucK](http://chuck.cs.princeton.edu/) is going to actually be making the noise.  All of its input will come from the MIDI that the Node server is emitting and create the sounds on the master device.  ChucK is a live coding environment, so we will have a number of synthesizers saved, but that code can be modified on the fly to create totally unique sounds.  It will also provide some visualizations.
### Initial wireframe
![img_4247](https://user-images.githubusercontent.com/8572233/35753959-46ab540a-0827-11e8-989b-924d4a2f37f6.JPG)

### DIY EEG tutorials
We made our eeg device out of a Nurosky MindFlex toy and an arduino by following this tutorial: http://www.frontiernerds.com/brain-hack

Other EEG devices should work similarly but will requier changes to mind-app.js to pulling your EGG's data.

![img_4251](https://user-images.githubusercontent.com/8572233/35826225-bf4336dc-0a7d-11e8-8243-cfac2b832661.JPG)


# CRAZY SOUNDS, PRETTY LIGHTS, INTERACTIVITY
