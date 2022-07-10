# uptime-kuma-api

A wrapper for the Uptime Kuma WebSocket API
---
uptime-kuma-api is a Python wrapper for the Uptime Kuma WebSocket API.

Installation
---
uptime-kuma-api is available on the Python Package Index (PyPI).

You can install it using pip:

```
pip install uptime_kuma_api
```

Examples
---
Once you have installed the python package, you can use it to communicate with an Uptime Kuma instance.

To do so, import `UptimeKumaApi` from the library and specify the Uptime Kuma server url, username and password to initialize the connection.

```python
from uptime_kuma_api import UptimeKumaApi

api = UptimeKumaApi('INSERT_URL')
api.login('INSERT_USERNAME', 'INSERT_PASSWORD')
```

Now you can call one of the existing methods of the instance. For example create a new monitor:

```python
>>> result = api.add_monitor(type_=MonitorType.HTTP, name="new monitor", url="http://192.168.1.1")
>>> print(result)
{'msg': 'Added Successfully.', 'monitor_id': 1}
```
