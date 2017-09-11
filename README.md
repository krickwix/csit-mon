# csit-mon
Overview
--------
This set of ansible playbooks deploy the components necessary to collect and visualize resource usage from servers.
The components used are well known:
* collectd
* influxdb
* grafana

It also deploys a log collection and query platform using:
* logstash
* elasticsearch
* kibana


Usage
-----
the inventory file will be populated with the required targeted hosts information.
Gathering hosts facts is a way to check the hosts connectivity from ansible.

$ ansible -i inventory/static -m setup all

Should return facts from every host in the inventory

$ ansible-playbook -i inventory/static playbooks/mon.yml

