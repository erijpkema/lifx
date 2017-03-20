lights on when home
===================

This script will switch your lifx lights on when you get home and it is dark outside.
It makes use of the [lifx public api](https://community.lifx.com/).
I run it on my raspberry pi but any computer that is permanently switched on and is located at your home should work. (you might want to change the install location though)

Prerequisites
-------------

* python3, virtualenvwrapper and pip.

Installation
------------

* copy settings.py.template to settings.py and fill in the data.
  You can get your location from google maps and your lifx api token from [lifx](https://community.lifx.com/).

* `mkvirtualenv lifx --python=/usr/bin/python3`

* `pip install -r requirements.txt`

* put the `lifx.service` file in `/etc/systemd/system` and enable it with `systemctl enable lifx.service`
  You should be able to confirm that it has started after running `journalctl /home/pi/lifx/start.sh`
