![](https://www.rainbird.com/images/RainBirdLogo.gif) 
# pyrainbird ![](https://img.shields.io/badge/python-3+-blue.svg)
> Python module for interacting with WiFi LNK module of the Rain Bird Irrigation system

This project has no affiliation with Rain Bird. This module works with the Rain Bird LNK WiFi Module.
 For more information see http://www.rainbird.com/landscape/products/controllers/LNK-WiFi.htm

----

This module communicates directly towards the IP Address of the WiFi module it does not support the cloud.
 You can start/stop the irrigation and get the currenltly active zone.

I'm not a Python developer, so sorry for the bad code. I've developed it to control it from my domtica systems.


**Please, feel free to contribute to this repo or chip in some cents for the effort and [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=TFXBL7W9VEQZC)

On the bottom of the module is some test code. Feel free te test it with your own

```python


# Test for controller
logging.basicConfig(filename='pypython.log',level=logging.DEBUG)


_LOGGER = logging.getLogger(__name__)
_LOGGER .setLevel(logging.DEBUG)
ch = logging.StreamHandler()
ch.setLevel(logging.DEBUG)
formatter = logging.Formatter('%(asctime)s - %(name)s - %(levelname)s - %(message)s')
ch.setFormatter(formatter)
_LOGGER.addHandler(ch)

controller = RainbirdController(jsoncommands)
controller.setConfig("####IP#####","####PASS#####")
controller.startIrrigation(4,5)
time.sleep(4)
controller.stopIrrigation()
```
