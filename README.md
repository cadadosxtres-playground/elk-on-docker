# Install Elasticsearch Kibana and Logstash with Docker

Repo got from video, https://www.youtube.com/watch?v=jXU_1GADENQ



## Issues

### Elasticsearch Container Stopped with Exit 78 in Ubuntu
* This issue is due to the vm.max_map_count is configured with 65530, even in the latest version such as 22.04
* Before, running docker compoes, run first ```sudo sysctl -w vm.max_map_count=262144```. If this change needs to be persistant then place a file in /etc/sysctl.d/ with the value
* More information, https://github.com/laradock/laradock/issues/1699
