Positron Rover Ground Control Station

Bitbucket repository: https://bitbucket.org/positioningpartners/pos-69-controller-ui/src/main/

Created by Positioning Partners for use with our Positron unmanned ground vehicle (UGV).
Visit us at: https://djm1271.uta.cloud/

GUI created with the help of PySimpleGUI: https://github.com/PySimpleGUI/PySimpleGUI

The Positron Rover Ground Control Station is a rover controller, developed in Python, that allows 
the user to control the Positron UGV.

This ground control station (GCS) allows the user to upload a mission for the Positron Rover to execute. A
mission consists of a series of latitude, longitude, and job tuples seperated by a comma. We've included an 
example mission.txt in the above repository. The GCS can activate Positron's paint module as well as track 
Positron's mission waypoints and *current location.

Prerequisites

Before you begin, ensure you have met the following requirements:

You've installed the latest version of Python (3.9.0 or higher)
You're using a Windows 10 machine. MAC OS is not supported.
You have read this README as well as the Positron user manual.
You have a telemetry device in your systems USB port that matches the one found on the Positron.
The 'the_connection = mavutil.mavlink_connection('com7', 57600)' statement on line 37 of controller_UI.py
will need to be modified to reflect the 'com#' port shown for your telemetry device.

Installation

To install Positron Rover Ground Control Station Software, follow these steps:

Navigate to our code repository given above and download the repository. Unzip the repository to a location
of your choosing. Open Windows Command Prompt and navigate to the newly installed CONTROLLER UI folder.

Dependencies

Install PySimpleGUI using 'python -m pip install PySimpleGUI --user'
Install folium using 'python -m pip install folium --user'
Install pymavlink using pip 'install pymavlink'
Install pygetwindow using 'pip install pygetwindow'

Execution

To run the program navigate to the CONTROLLER UI folder using Windows Command Prompt. Once inside this
directory use the 'python controller_UI.py' command to execute.

Example Run

When the Positron Ground Control Station starts the user is presented with a window that contains
six buttons. The six buttons have a text terminal seperating them with three on top and three beneath. 
There are two drop down menu options on the toolbar of the window.

To start an example run of the program use the "Mission" drop down menu and select "Load". Enter 'mission.txt'
to load the example mission. Next arm the rover by using the "Rover" drop down menu and selecting "Arm". 
Once Positron is armed all GCS functions can be executed. To view your mission map click the "MAP" button. 
To add a waypoint click the "WAYPOINTS" button. To remove the last added waypoint click the "X" button. 
*To send Positron to the next waypoint click the "GO" button. *To stop Positron click the "STOP" button. 
To activate Positron's paint module click the "PAINT" button. To save a mission to a file use the "Mission" drop 
down menu and select "Save". Enter 'example.txt' to save your current mission.

*These functions were not fully implemented but can be with the addition of the corresponding Mavlink commands.

Contributors

Thanks to the following people who have contributed to this project:
Daniel Marks 
Nathan Fusselman 
Oscar Mariscal 
Deborah Jahaj 
Kamal Karkidholi 

Visit us at: https://djm1271.uta.cloud/

License
This project uses the following license: GPL3.0 https://www.gnu.org/licenses/gpl-3.0.en.html.
