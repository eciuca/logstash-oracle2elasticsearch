# logstash-oracle2elasticsearch

## Pre-requisites

1. Install docker
2. Have an elasticsearch instance running locally at localhost:9200
3. Have an oracle db instance running locally at localhost:1521

## How to:

1. Clone the repository: `git clone https://github.com/eciuca/logstash-oracle2elasticsearch.git`

2. Open `oracle2elasticsearch-pipeline/oracle2elasticsearch.conf` and change the variables marked with square brackets `[ ]`

3. Run the following command from the project root

```
docker run --rm --network=host --add-host elasticsearch:127.0.0.1 -v %cd%\config\pipelines.yml:/usr/share/logstash/config/pipelines.yml -v %cd%\resources:/usr/share/logstash/resources -v %cd%\oracle2elasticsearch-pipeline:/usr/share/logstash/oracle2elasticsearch-pipeline docker.elastic.co/logstash/logstash:6.2.2
```


