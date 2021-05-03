# pyspark-notebok-docker

# spark on docker

# command to launch:
docker run -it -p 8888:8888 jupyter/pyspark-notebook

# to login to CLI
docker exec -it <container-name> /bin/sh

# upload files from local to docker files/folder
docker cp /hostfile  (container_id):/(to_the_place_you_want_the_file_to_be)

e.g.
docker cp people.json 35ff6a76ecdb:/home/jovyan/work/people.json
docker cp vermont_vendor_payments.csv 35ff6a76ecdb:/home/jovyan/work/vermont_vendor_payments.csv

# stop and remove
docker stop $(docker ps -aq)
docker rm $(docker ps -aq)
