# RDBMS
* Relational Database Management System
* Database > Table > row > column

## cubrid
국내의 관계형 데이터베이스 관리 시스템이며, 오픈소스 프로젝트.

## InnoDB
MySQL을 위한 데이터베이스 엔진. [트랜잭션](http://egloos.zum.com/springmvc/v/495798)을 지원함.

*** 

# NoSQL(Not Only SQL) 
일관성 모델(비관계형 모델)을 이용하는 데이터 저장소의 새로운 형태로, **관계형 데이터베이스가 갖는 한계**를 극복

1. RDBMS에 비해 저렴한 비용으로 분산 처리와 병렬 처리가 가능
2. 비정형 데이터 구조 설계로, 설계 비용이 감소
3. RDB의 relation과 join 구조를 linking과 embedded로 구현하여 성능이 빠름

### 관계형 데이터베이스가 갖는 한계
(정리하기)

## Mongo DB
* Document-oriented Storage : database > collections > documents 구조로 되어있으며, document는 'key-value' 형태의 BSON(Binary JSON)으로 되어있다.

### 장점
쌓아두고 삭제가 없는 경우 적합(로그데이터, 세션 등)
* Flexibility : Schema-less이기 때문에, 어떤 형태의 데이터라도 저장이 가능
* Performance : R/W 성능이 뛰어남. 캐싱이나 많은 트래픽을 감당할 때도 좋음.
* Scalability : 애초부터 Scale-out 구조를 채택해서 쉽게 운용 가능

### 단점
정합성이 떨어짐
* [참고링크](http://sjh836.tistory.com/98)

## Redis(Remote Dictionary Server)
'키-값' 구조의 비정형 데이터를 저장하고 관리하기 위한 비관계형(NoSQL) 데이터베이스 관리 시스템

디스크가 아닌 메모리 기반 데이터 저장소

데이터베이스로 사용될수도, 캐시로 사용될 수도 있는 기술

* [참고링크](http://codingmania.tistory.com/18)

***

# 검색엔진

## Lucene
색인과 검색 API를 제공하는 라이브러리.

## Solr
Apache Lucene을 기반으로 만들어진 검색엔진. 색인과 검색은 Lucene 엔진을 사용하면서, http요청에 대한 처리와 응답을 하는 웹 기반 검색엔진이다.

* [참고링크](https://gs.saro.me/dev?tn=406)

## Elasticsearch
* index > type > document > key:value

***

## 기타

### rsync
Remote Synchronization. local과 remote간의 데이터 동기화(두 서버 간의 데이터 백업)를 위한 유틸리티이다. 전송 시 네트워크 대역폭을 최소화하는 **델타 인코딩 알고리즘**을 사용하여 변경이 일어난 부분만 전송하므로 빠르고 효율적으로 데이터를 동기화 할 수 있다. 패키지에 client와 server 프로그램이 모두 포함되어 있다. 

> 별도의 server **daemon**으로 구동 시 TCP/UDP의 873 포트를 사용하지만, SSH 프로토콜을 기반으로 사용하면 기존의 SSH 포트를 사용하여 별도의 방화벽 오픈 등의 작업이 필요 없어지므로 이 방법으로 사용하는 것을 권장한다. 

* [참고링크](https://www.lesstif.com/display/1STB/rsync)

#### Server Daemon으로 백업하기
master 서버에서 rsync 데몬을 띄우고, backup 서버에서 master 서버에 접근하여 허용된 디렉토리의 데이터를 백업하는 방식

* Daemon : 사용자가 직접적으로 제어하지 않고, 백그라운드에서 돌면서 여러 작업을 하는 프로그램
