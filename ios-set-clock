from datetime import datetime, timedelta
from netmiko import ConnectHandler
import config

# Define the device information
device = {
    'device_type': 'cisco_ios',
    'ip': '192.168.1.1',
    'username': "USERNAME",
    'password': "PASSWORD",
}

# Connect to the device
net_connect = ConnectHandler(**device)

# Get the current time in GMT
gmt_time = datetime.utcnow()

# Adjust the time by -1 hour
gmt_minus_1 = gmt_time - timedelta(hours=1)

# Format the time in the correct format for the router
time_str = gmt_minus_1.strftime('%H:%M:%S %d %b %Y')

# Set the clock
command = f"clock set {time_str}"
print (command)
net_connect.send_command_timing(command)


# Disconnect from the device
net_connect.disconnect()
