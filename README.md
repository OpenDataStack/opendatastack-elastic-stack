# Pull and run Elastic stack 
```
$ git clone git@github.com:angrycactus/ods-elastic-stack.git
$ cd ods-elastic-stack
$ docker-compose up -d
```
## Test stack
Open http://localhost:9200. A similar output should be displayed:
```
{
  "name" : "PDnOU3L",
  "cluster_name" : "docker-cluster",
  "cluster_uuid" : "TvBm67CRQZqAVOsDrHEqBg",
  "version" : {
    "number" : "5.6.2",
    "build_hash" : "57e20f3",
    "build_date" : "2017-09-23T13:16:45.703Z",
    "build_snapshot" : false,
    "lucene_version" : "6.6.1"
  },
  "tagline" : "You Know, for Search"
}
```
Open http://localhost:5601. The Kibana homepage should be dispayed.