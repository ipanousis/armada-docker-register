Runs a docker-gen container with a template that prints container to a JSON file

Define environment variable NOTIFY in your extending Dockerfile and make use of available
JSON file /tmp/containers.json within your NOTIFY script

e.g.

ENV NOTIFY python /tmp/my-own-script.py

where /tmp/my-own-script.py

```
#!/usr/bin/env/python

dict=eval(open('/tmp/containers.json','r').read())

print dict

```
