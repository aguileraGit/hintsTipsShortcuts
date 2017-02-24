
### To connect to RaspberryPi via UART.
* [Reference webpage](http://elinux.org/RPi_Serial_Connection)
* Requires FTDI
* Physically connect cables and plug in RPi. Screen is blank, but connection is made. Type in user name.

### Setting up RPi for Jupyter
[Reference: Scientific-python-raspberry-pi](http://geoffboeing.com/2016/03/scientific-python-raspberry-pi/)

Enable SSH and VNC:
- `sudo rasp-config`

Update distribution:
- `sudo apt-get update`
- `sudo apt-get dist-upgrade`

Install software:
- `sudo apt-get install build-essential python-dev python-distlib python-setuptools python-pip python-wheel libzmq-dev libgdal-dev xsel xclip libxml2-dev libxslt-dev python-lxml python-h5py python-numexpr python-dateutil python-six python-tz python-bs4 python-html5lib python-openpyxl python-tables python-xlrd python-xlwt cython python-sqlalchemy python-xlsxwriter python-jinja2 python-boto python-gflags python-googleapi python-httplib2 python-zmq libspatialindex-dev python-numpy python-matplotlib python-mpltoolkits.basemap python-scipy python-sklearn python-statsmodels python-pandas python-requests python-pil python-scrapy python-geopy python-shapely python-pyproj
`

Install pip the correct way:
- `curl --silent --show-error --retry 5 https://bootstrap.pypa.io/get-pip.py | sudo python2.7`

Install Jupyter:
- `sudo pip install jupyter`


## Upstart - Breaks installation!
description "Start Jupyter Server"
author "Diego Aguilera"

start on runlevel [2345]

respawn
respawn limit 10 50

script
        export HOME="/home/pi/Projects/jupyter/home"; cd $HOME
        exec jupyter notebook --ip 10.48.2.73
end script

pre-start script
        echo "[`date`] Jupyter Notebook starting" >> /var/log/jupyterUpStart.log
end script

pre-stop script
        echo "[`date`] Jupyter Notebook stopping" >> /var/log/jupyterUpStart.log
end script
