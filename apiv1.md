## FunctionDef status_get
**status_get Function**: The function of this Function is to retrieve and return the current system status information, specifically the temperatures of system sensors.

This function utilizes the psutil library to fetch the current system temperatures, which are then returned as a JSON response.

The function is designed to provide a simple and straightforward way to access system status information, making it suitable for use in various applications that require real-time monitoring or logging of system temperatures.

**Note**: This function relies on the psutil library, which must be installed and imported for this function to work correctly.

**Output Example**: A possible appearance of the return value of this function might be a JSON object containing key-value pairs, such as:
```
{
    "cpu": {
        "coretemp": {
            "core0": 42.5,
            "core1": 43.2,
            "core2": 41.8,
            "core3": 42.1
        }
    },
    "fans": {
        "fan1": 600,
        "fan2": 700
    },
    "gpus": {
        "gpu0": {
            "core": 55.5,
            "mem": 75.2
        },
        "gpu1": {
            "core": 56.8,
            "mem": 76.5
        }
    },
    "hdds": {
        "hdd1": {
            "temperature": 35.2
        },
        "hdd2": {
            "temperature": 36.5
        }
    }
}
```
This JSON object contains information about the CPU, fans, GPUs, and HDDs, including their temperatures and other relevant metrics.
## FunctionDef net_get_info
**net_get_info Function**: The function of this Function is to retrieve network information.

This function is designed to fetch network information from a network manager and return it as a JSON response. It utilizes the `network.manager.get_info()` method to retrieve the network information, which is then serialized into a JSON format using the `flask.jsonify()` function.

The function does not take any parameters and returns a `flask.Response` object containing the network information in JSON format.

**Note**: The `network.manager.get_info()` method is assumed to be properly configured and initialized before calling this function.

**Output Example**:
{
    "network_info": {
        "ip_address": "192.168.1.100",
        "subnet_mask": "255.255.255.0",
        "gateway": "192.168.1.1",
        "dns_servers": ["8.8.8.8", "8.8.4.4"]
    }
}
***
