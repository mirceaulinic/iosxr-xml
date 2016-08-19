[![PyPI](https://img.shields.io/pypi/v/iosxr-xml.svg)](https://pypi.python.org/pypi/iosxr-xml)
[![PyPI](https://img.shields.io/pypi/dm/iosxr-xml.svg)](https://pypi.python.org/pypi/iosxr-xml)

## ABOUT

iosxr-xml is a Python library to manage IOS-XR devices through the [XML agent](https://supportforums.cisco.com/document/61436/introduction-xml-asr9000).


#### Requirements:

* netmiko >= 0.5.2
* lxml >= 3.4.2

### Install via pip:

````bash
pip install iosxr-xml
````

## USGAE

Firstly make sure that the XML agent is properly enabled on the device:

    # xml agent tty iteration off

#### Connect to the device:

````python
from iosxr_xml import Device

dev = Device(host='edge01.bjm01', user='netconf', password='!Love105-XR')
dev.open()
dev.make_rpc_request('<Get><Operational><Interfaces/></Operational></Get>')
dev.close()
````

## LICENSE

Copyright 2016 CloudFlare, Inc.

Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0
