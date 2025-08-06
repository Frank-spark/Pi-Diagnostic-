# Pi-Diagnostic-



`htop`
Displays real-time CPU usage per core, memory consumption, process list, and system load. Useful for spotting high load or unresponsive processes.

`sudo apt update`
`sudo apt install htop`
Installs `htop` if not already available.

`uptime`
Shows how long the system has been running and the average load over the past 1, 5, and 15 minutes.

`vcgencmd get_throttled`
Reports undervoltage, frequency capping, or overheating events. Any non-zero value indicates power or thermal instability.

`vcgencmd measure_volts core`
Reports CPU core voltage. Values below 0.85V suggest undervoltage and system instability.

`dmesg | grep -i voltage`
Checks kernel logs for voltage-related warnings.

`lsusb`
Lists all connected USB devices such as Ethernet adapters and audio interfaces.

`lsusb -t`
Displays the USB device tree and connection speeds. Useful for verifying correct USB bus usage and speed negotiation.

`dmesg | grep -i usb`
Shows USB connection, disconnection, and error events from the system log.

`usb-devices`
Prints detailed information about each connected USB device, including vendor, product ID, and driver.

`ip link show`
Lists all network interfaces and their state (up or down).

`ip addr`
Displays IP and MAC addresses for all interfaces. Confirms proper IP assignment and identification.

`ethtool eth0`
Displays link status, speed, and duplex mode for the onboard Ethernet port or USB NIC.

`ping 10.0.0.1`
Tests connectivity to the PLC module and verifies network communication.

`raspi-gpio get`
Shows the state and mode of all GPIO pins. Helps verify correct pin configuration and activity.

`dmesg | grep gpio`
Finds GPIO-related messages in the system log. Useful for catching driver or overlay issues.

`i2cdetect -y 1`
Scans the I2C bus for connected devices. Confirms presence of devices like RTCs.

`sudo hwclock -r`
Reads the current time from the real-time clock module.

`dmesg | grep rtc`
Searches logs for RTC driver messages to confirm proper initialization.

`aplay -l`
Lists detected ALSA audio playback devices. Confirms presence of USB audio interfaces.

`dmesg | grep snd`
Displays audio system messages to help diagnose detection or driver loading issues.

