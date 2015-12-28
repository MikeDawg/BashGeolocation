# BashGeolocation
A very minimalistic tool to geolocate any IP address in the world (CLI tool) No lib needed

## How to use it
Open a terminal and type:

```
chmod u+x ./geolocation
./geolocation <IP address>

```

If you don't give any arguments it will show you your own location.

## copy it in your /usr/bin directory.

`sudo cp ./geolocation /usr/bin`

And then execute it by typing (in any directory):

`geolocation <IP address>`

## Output only selected infos

Default output for this command line are ip,hostname,city,region,country,loc,org,postal ([example of output](#example-of-output)).

You can select the informations you want to be printed by adding a sed filter:

```
./geolocation <IP address> | | sed -n '/ip/p;/loc/p'
```

It will output the IP you given and the Country.

## Example of output
_Personal infos were hidden._


```
ip:167.xx.xx.118
hostname:NoHostname
city:Ada
region:Michigan
country:US
loc:43.xxxx-85.xxxx
org:xxxxxxxxxxxxxxxx
postal:49355
```