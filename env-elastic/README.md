[![Docker Repository on Quay](https://quay.io/repository/7insyde/elastic/status "Docker Repository on Quay")](https://quay.io/repository/7insyde/elastic)


Example to run Elasticsearch as Master Node:
```
docker run -d -e ELASTIC_NODE_MASTER=true -p 9300:9300 quay.io/7insyde/elastic 

```

to run Elasticsearch as Data Node:
```
docker run -d -v /data/elastic:/data/elastic -e ELASTIC_NODE_DATA=true -p 9300:9300 quay.io/7insyde/elastic
```

to run Elasticsearch as Client Node:
```
docker run -d -e ELASTIC_HTTP_ENABLE=true -p 9200:9200 -p 9300:9300 quay.io/7insyde/elastic
```
