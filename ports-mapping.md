# Ports mapping
Pre-defined ports to be used

## Internal Ports

|Module | Internal port | Service port |
|--- | --- | --- |
| Config-app | 11003 | 11003 |
| Core-API | 8080 | 8080 |
| Auction-engine | 8080 | 8180 |
| Infinispan | 8080 | 8280 |
| Kafka | 9092 | 9092 |
| Solr | 8983 | 12001 |
| Zookeeper | 2181 | 2181 |


## External Ports

|Module | Internal port | Service port | Proxy uri |
|--- | --- | --- | --- |
| Admin Gateway | 8080 | 8180 | admin-gateway.tdaux.com:443 |
| Admin Web | 8080 | 8280 | admin-web.tdaux.com:443 |
| Mobile Gateway | 8080 | 8380 | mobile-gateway.tdaux.com:443 |
| Openfire | 7070 | 7070 | openfire.tdaux.com:443 |
| Tdaux | 8080 | 8080 | www.tdaux.com:443 |
