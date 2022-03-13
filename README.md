# presentation
import machine
led = machine.Pin(18,machine.Pin.OUT)
led.off()

import network
sta = network.WLAN(network.STA_IF)
if not sta.isconnected():
    print('connecting to network...')
    sta.active(True)
    #sta.connect('your wifi ssid', 'your wifi password')
    sta.connect('iPhone de Amelie', 'but in double')
    while not sta.isconnected():
        pass
print('network config:', sta.ifconfig())
