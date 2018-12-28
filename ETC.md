## rsync
* rsync는 **r**emote **sync**hronization의 약자로 samba 의 핵심 개발자인 Andrew Tridgell 이 만든 로컬과 리모트간에 데이타 동기화를 위한 유틸리티이다.
* 전송시에 네트워크 대역폭을 최소화하는 델타 인코딩 알고리즘을 사용하여 변경이 일어난 부분만 전송하므로 빠르고 효율적으로 데이타를 동기화한다.
* rsync는 패키지에 client와 server 프로그램이 모두 포함되어 있으며 별도의 server 데몬으로 구동시 TCP/UDP의 873 포트를 사용하지만 ssh 프로토콜을 기반으로 사용하면 기존 ssh 포트를 사용하여 별도의 방화벽 오픈등의 작업이 필요 없어지므로 이 방법으로 사용하는 것을 권장한다.
[참고링크](https://www.lesstif.com/display/1STB/rsync)

* 두 서버 간의 데이터 백업을 위해서 사용
*  master서버에서 rsync데몬을 띄우고, backup 서버에서 master서버에 접근하여 허용된 디렉토리의 데이터를 백업하는 방식과, ssh를 이용하여 데이터를 미러링 하는 방법 두가지가 있다.
[참고링크](https://www.sharedit.co.kr/posts/1579)

### rsync 알고리즘
롤링 체크섬을 사용해서 두 파일에 대한 신속한 비교를 제공하며, 링크 지연에 미치는 영향을 최소화

## Daemon
사용자가 직접적으로 제어하지 않고, 백그라운드에서 돌면서 여러 작업을 하는 프로그램


## Solr
* Solr는 Apache Lucene을 기반으로 만들어진 검색엔진이다.  
* Lucene은 색인과 검색 API를 제공해주는 라이브러리다.  Solr는 색인과 검색은 **Lucene 엔진을 사용하면서 Http 요청에 대한 처리와 응답을 하는 웹 기반 검색엔진**이라고 할 수 있다.  
* 
https://gs.saro.me/dev?tn=406

## Message Queue
* 사용자의 입력(키보드/마우스)을 메시지로 전달하는 윈도우즈 시스템에서 어떤 프로세스에 대한 메시지를 저장하기 위해 할당된 큐
* 사용자의 입력이 메시지로 프로세스에 전달되면 프로세스에서는 메시지 큐에 저장해서 순차적으로(?) 처리한다.

## RabbitMQ
* 표준 [AMQP (Advanced Message Queueing Protocol)](http://www.amqp.org/)메세지 브로커 소프트웨어(message broker software) 오픈소스
* [참고링크](http://blog.saltfactory.net/install-rabbitmq/)

## MQ(Message Queueing)
* 프로그램 인스턴스 또는 프로세스가 데이터를 서로 교환할 때 사용
* 데이터를 서로 교환할 때 시스템이 관리하는 메세지 큐를 이용하는 것이 특징(?)

### AMOP
* Advanced Message Queueing Protocol

## Redis
* Remote Dictionary Server
* 'key-value' 구조의 비정형 데이터를 저장하고 관리하기 위한 비관계형 데이터베이스 관리 시스템
* 디스크가 아닌 메모리 기반 데이터 저장소
* 데이터베이스로 사용될 수 있으며, 캐시로도 사용될 수 있는 기술
* NoSQL DBMS로 분류된다
* [참고링크](http://codingmania.tistory.com/18)

## cubrid
관계형 데이터베이스 관리 시스템, 오픈소스


## interface
* 클래스에서 구현부가 빠진 것
* 어떠한 객체가 이러한 프로퍼티, 혹은 메소드를 가진다고 선언하는 것
* 실질적인 구현은 이를 구현한다고 선언하는 클래스에 맡긴다.
* 일단 인터페이스를 구현하기로 했으면, 해당 인터페이스에 있는 프로퍼티 및 메소드를 전부 가지거나 구현해야 한다.'
* 인터페이스로는 객체 인스턴스를 생성할 수 없으므로 주로 타입 검사를 위해서 활용된다.
* optional property: 선택적으로 구현하는 프로퍼티, 프로퍼티 식별자 뒤에 ?를 붙여서 사용
[참고링크](https://hyunseob.github.io/2016/10/17/typescript-interface/)

## index signature

## CSS Preprocessor
* CSS 전처리기
* CSS가 동작하기 전에 사용하는 기능
* CSS의 불편함을 상쇄시켜주는 확장 기능
* 웹에서는 CSS만 동작, CSS 전처리기로는 직접 동작시킬 수 없음
* 더 많은 기능을 지원하는 전처리기로 작성한 후에 CSS로 컴파일해서 동작시킴
* 전처리기 3대장 : Less, Sass(SCSS), Stylus
* SCSS : Sass의 3버전, CSS와 더 유사

## polyfill
* 낡은 브라우저에서 모던 코드를 사용할 수 있게 해주는 방법
* 크로스 브라우징을 고려한 것

## 
