# nodeMCU Terrarium

NodeMCU controlled Terrarium

## Components

*   nodemcu dev rom with DHT, net, timer... library
*   <http://prometheus.io> server for collecting metrics
*   nodeMCU module
*   2x DHT_22 modules
*   relay module
*   humidizer

## Example configuration

DHT on pin 7 is inside, DHT on pin 6 is on outside. On pin 1 is humidizer,
pin 2 is light control (not implemented auto switch).

Server responds on

*   `/metrics` - shows metrics for collecting by prometheus
*   `/forgon` - switches pin 1 on
*   `/fogoff` - turns pin 1 off
*   `/lighton` - switches pin 2 on
*   `/lightoff` - switches pin 2 off

Connection settings are in set in `wifi.lua`.