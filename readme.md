# Dependencies
`pip install twisted mss pillow pynput`

# Usage
One person must be controller, the other person must be controllee (being controlled). One of those persons must be server, the other one must be client.

usage: cli.py [-h] [--host HOST] [--port PORT] {controller,controllee}

Starts a control session. You can choose to be controlled, or to control someone, and you need to specify who is server and who is client

positional arguments:
  {controller,controllee}
                        Controller: You are the one who controls other computer. 
                        Controllee: You are the one being controlled

optional arguments:
  -h, --help            show this help message and exit
  --host HOST           Enter hostname here (or ip address). If you specify this then this means that you are client (you will initiate tcp connection as client). If not specified, you will host a server
  --port PORT           Which port to use when connecting/starting the server. Default is 5005



# Known issues
* Platforms other then windows are not tested. In theory this should work.
* You don't see mouse in controllee's mouse. You should just blindly trust that it is there.
* In case of multiple montior setup, a mouse can stop between the monitors when moving. If that happens controllee must either move the mouse manually a bit, or restart the software.
