# Netdata monitoring using Docker

#Prerequisites
Install Docker on your machine
Install Netdata with Docker
docker run -d --name=netdata -p 19999:19999 netdata/netdata

#Access Netdata Dashboard
Open browser and go to http://localhost:19999
Explore Netdata dashboard displaying real-time system metrics: CPU, memory, disk, network, and Docker containers if present

#verify logs
>> Using Docker Logs Command
docker logs netdata
>> Accessing Logs on the Host Machine
docker exec -it netdata bash
cd /var/log/netdata
cat error.log
cat access.log
tail -f error.log(for live tailing)
