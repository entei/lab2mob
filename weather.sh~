#!/bin/sh
if [ "--help" = "$1" ]
	then
	echo "weather [options]"
	echo "weather forecast for the near future"
	echo "messages timeout was set in config.ini"
	echo "options:"
	echo "\t--help,\tshow help"
else
	timeout=$(sed -n 's/.*interval *= *\([^ ]*.*\)/\1/p' < ./config.ini)
	if ping -c1 informer.gismeteo.ru > /dev/null
		then
		rm -rf ./temp
		mkdir ./temp
		cd temp
		while true
			do
			rm -rf 26850.xml
			wget --no-proxy -q informer.gismeteo.ru/rss/26850.xml
	else
		echo "Connection problem"
	fi
fi
return 0
