# Mqtt

You can use [Mosquitto](http://mosquitto.org/) or [Mosca](http://mcollina.github.io/mosca/) as your own mqtt broker

## Mosquitto

### Install

#### Linux

* apt-get update
* apt-get install mosquitto mosquitto-clients python-mosquitto

`Mosquitto` is the MQTT broker (i.e. server)

`Mosquitto-clients` are the command-line clients, which I recommend you install

`Python-mosquitto` are the Python bindings, which I also think you should install

The server will start after install

##### Or (perhaps have problems, not suggest)

* wget http://mosquitto.org/files/source/mosquitto-1.4.tar.gz
* tar zxfv mosquitto-1.4.tar.gz
* cd mosquitto-1.4
* sudo make install

#### Mac

* brew install mosquitto
