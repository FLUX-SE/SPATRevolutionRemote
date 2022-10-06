# SPAT Revolution Remote
A Remote control patch for SPAT Revolution object-based audio rendering and creation tool, implementing ADM-OSC, the Audio Definition Model (ADM) over Open Sound Control (OSC).

## Project Originators
[Zoltan](https://ctrlz.gumroad.com/), [FLUX::SE](https://www.flux.audio/), [Whiti Audio](https://www.whitiaudio.fr/)

## What's involved?

[Open Stage Control](https://openstagecontrol.ammd.net/) is an open-source application, a modular OSC / MIDI controller based around a server (at the core), the launcher (configuration and server start) and the client. Clients are simply any browser that reaches the web address with port #

## Getting setup

A few little steps are involved in configuring this,

- Download and install Open Stage Control. The application (server) that runs in the background and allow a client access
  - [MacOS](https://github.com/jean-emmanuel/open-stage-control/releases/download/v1.17.0/open-stage-control-1.17.0-osx.zip)
  - [Windows (64-bit)](https://github.com/jean-emmanuel/open-stage-control/releases/download/v1.17.0/open-stage-control-1.17.0-win32-x64.zip)

- Download the [Open Stage Control - SPAT Revolution patch file](https://github.com/FLUX-SE/SPATRevolutionRemote/blob/c787847ea1c1651f66c6f4466f60f0cc3aad559f/Source/SPATRevolutionRemote.json). This file is the actual patch file that the server is running. It is as well available via the [FLUX Center Application](https://www.flux.audio/download/) which downloads all the resources (patch & config files) to the local computer.
 - Default location:
    - macOS: ```Library/Application Support/Flux/SPAT Remote Server```
    - Windows: ```Program Files/Flux/SPAT Remote Server```

- Open the Open Stage Control application and configure it. This can be done manually but config file are available for both macOS and Windows. The config file can be simply loaded to Open Stage Control pressing the three dots on the right side of the interface

  - macOS:[SPAT_Remote_Config_macOS.config](https://github.com/FLUX-SE/SPATRevolutionRemote/blob/c787847ea1c1651f66c6f4466f60f0cc3aad559f/Source/SPAT_Remote_Config_macOS.config)
  - Windows: [SPAT_Remote_Config_Windows.config](https://github.com/FLUX-SE/SPATRevolutionRemote/blob/c787847ea1c1651f66c6f4466f60f0cc3aad559f/Source/SPAT_Remote_Config_Windows.config)

![Load Config](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteLoadConfig.png)

![SPAT Revolution Remote Config](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteConfig.png)

- The provided config file will have a predetermined path for loading the patch. This path is the default path where the FLUX:: Center will download the resources.
  - macOS: ```Library/Application Support/Flux/SPAT Remote Server/SPATRevolutionRemote.json```
  - Windows: ```Program Files/Flux/SPAT Remote Server/SPATRevolutionRemote.json```
![Loading the patch file macOS](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteLoadFilemacOS.png)
![Loading the patch file Windows](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteLoadFileWindows.png)

- The last step is to simply run the server.Simply press the Play button and the server will be up and running. The console will show all the client session info for all the available network interfaces with the computer.
![Run Server](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteRunServer.png)
![Server Info](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteServerInfo.png)

- You can optionally, engage the autostart so everytime Open Stage Control is open, the server will run.
![Autostart](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteAutostart.png)

## Configuring SPAT Revolution application

Configuring SPAT Revolution requires to set the OSC Connection Input and Output port for the SPAT Remote Server. Predefined presets simply needs to be chosen for the input and the output. These presets include the ADM-OSC transformation presets which includes the ability to scale the normalized data to the desired range (The object positioning zone). By default, it is scaling to a scene a 10 m3.

- Access the SPAT Revolution preference page and reach the OSC Connection section

- Add the input | SPAT Remote server preset
![SPAT Revolution OSC Connection Input](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteSPATOSCConnectionIn.png)

- Add the output| SPAT Remote server preset
![SPAT Revolution OSC Connection Output](https://media.githubusercontent.com/media/FLUX-SE/doc_images/main/SpatR/ThirdParty/SPATRevolutionRemoteSPATOSCConnectionOut.png)

> These above presets used the default ports of the Open Stage Control Config files supplied with by default the local 127.0.0.1 port which is required when running the server locally with SPAT Revolution (most common scenario)

## Contributing to the SPAT Revolution Remote Project
TBA

## License

The SPAT Revolution Remote patch is covered by a GNU General Public License v3.0
