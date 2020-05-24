# TouchDesigner and Open Stage Control

This guide is for setup a basic environemnt for live performance using [TouchDesigner](https://derivative.ca/) and [Open Stage Control](https://openstagecontrol.ammd.net/) to receive and send OSC messages via UDP protocol.

There are already some software that enables this kind of comunication, like TouchOSC and the TouchOSC Bridge, both of which I've personally tried and they sure do their job flawlessy.

But many people don't wanna spend money on apps for experiments, or maybe they want more customization than the one provided by TouchOSC Editor.

In this case, Open Stage Control is the perfect choice to go: it's Open Source, and it's written and compiled in Electron, which gives us some of the cool features of Javascript and CSS for styling.

Index of contents:
- Installation
- Open Stage Control Setup


## Installation
First you must download both TouchDesigner and Open Stage Control.
When you have them, run TouchDesigner and create a blank project.
*For Windows only* 
Since the OSC messages will be passed over the local network, we have to make sure that the firewall of Windows is not blockin them.
To do so go to Control Panel>System and Security> Windows Firewall > Allow App through Windows Firewall.

This will bring you to a list, scroll down until you find TouchDesigner and allow by clicking the checkbox for both public and private network.

## Open Stage Control Setup
When you open Open Stage Control you will be prompted to a setup window.
The only thing that we wanna insert here is in the first row where it says "send" which defines to which address should the next window of panel editor send the messagges.
In our example I've insert the following:
`localhost:3746`
meaning that we'll send to our local machine at the port `3746`.