#### Auto start
[https://gist.github.com/whophil/5a2eab328d2f8c16bb31c9ceaf23164f](Reference)

#Create config
jupyter notebook --generate-config

#Create password - Open up
from notebook.auth import passwd; passwd()

jupyter.service - Install in /etc/systemd/system

[Unit]
Description=Jupyter Notebook

[Service]
Type=simple
#PIDFile=/run/jupyter.pid
ExecStart=/usr/local/bin/jupyter notebook --no-browser --config=/home/hg/.jupyter/jupyter_notebook_config.py
User=hg
#Group=hg
WorkingDirectory=/home/hg/Projects
Restart=always
RestartSec=10

[Install]
WantedBy=multi-user.target


#Look at logs if fails
https://unix.stackexchange.com/questions/225401/how-to-see-full-log-from-systemctl-status-service
