# on MAC
system_profiler SPBluetoothDataType     # get list of active bluetooth devices
                                        # find Apple Magic keyboard's Address: XX-XX-XX-XX-XX-XX 

# on rpi
ssh pi@[IP]                             # SSH if no keyboard

sudo service bluetooth status           # starting Bluetooth service...
sudo bluetoothctl
scan on                                 # enabling discovery
pair XX:XX:XX:XX:XX:XX                  # XX:..:XX is devices Address
    # [agent] Confirm passkey 00000 (yes/no): yes
trust XX:XX:XX:XX:XX:XX
connect XX:XX:XX:XX:XX:XX
exit