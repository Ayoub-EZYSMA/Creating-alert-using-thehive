# Creating-alert-using-thehive
# Installation guide
Installation of Shuffle is available in docker.
# Docker - *nix
The Docker setup is done with docker-compose 


1. Make sure you have [Docker](https://docs.docker.com/get-docker/) and [docker-compose](https://docs.docker.com/compose/install/) installed.
2. Download Shuffle
```bash
git clone https://github.com/Shuffle/Shuffle
cd Shuffle
```

3. Fix prerequisites for the Opensearch database (Elasticsearch): 
```bash
mkdir shuffle-database
sudo chown -R 1000:1000 shuffle-database
# IF you get an error using 'chown', add the user first with 'sudo useradd opensearch'
```

4. Run docker-compose.
```bash
docker-compose up -d
```

5. Recommended for Opensearch to work well
```bash
sudo sysctl -w vm.max_map_count=262144             # https://www.elastic.co/guide/en/elasticsearch/reference/current/vm-max-map-count.html
```



6. Run docker-compose
```bash
docker-compose up -d
```


### After installation 
1. After installation, go to http://localhost:3001 (or your servername - https is on port 3443)
2. Now set up your admin account (username & password). Shuffle doesn't have a default username and password. 
3. Sign in with the same Username & Password! Go to /apps and see if you have any apps yet. If not - you may need to [configure proxies](https://shuffler.io/docs/configuration#production_readiness)
4. Check out https://shuffler.io/docs/configuration as it has a lot of useful information to get started
