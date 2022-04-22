# D. 응용 SW 기초 기술 활용

## OSI 참조 모델

### OSI(Open System Interconnection) 참조 모델

ISO(국제표준화기구)에서 제안한 통신 규약

물데네 전세 표응

![](/img/OSI.png)

<table><thead><tr><th>계층</th><th>기능</th><th>프로토콜<br>(굵은 표시: 본문에 없는 내용)</th><th>장비</th><th>데이터 전송 단위</th></tr></thead><tbody><tr><td>응용<br>(Application)</td><td><strong>사용자가 OSI 환경에 접근</strong>, 정보 교환/파일 전송/가상 터미널</td><td>FTP, SMTP, Telnet, SNMP, DNS, HTTP, POP3</td><td></td><td>메시지</td></tr><tr><td>표현<br>(Presentation)</td><td><strong>서로 다른 데이터 표현</strong>, <strong>확장자</strong> 형태 상호 접속, 코드 변환/데이터 암호화/데이터 압축/구문 검색/포맷 변환/문맥관리</td><td>SMB, MPEG, <strong>AFP, JPEG, XDR, ASN.1</strong></td><td></td><td>메시지</td></tr><tr><td>세션<br>(Session)</td><td><strong>동기화</strong>, <strong>포트 연결</strong>, 신뢰성 보장</td><td>SSL, TLS, SSH, <strong>RPC, NetBIOS</strong></td><td></td><td>메시지</td></tr><tr><td>전송<br>(Transport)</td><td>송수신 측의 <strong>실질적 연결</strong>, <strong>전체 메시지의 전송</strong> 책임, 종단 시스템 간 투명한 데이터 전송</td><td>TCP, UDP, RTCP, <strong>SCTP, SPX</strong></td><td>게이트웨이</td><td>TCP - Segment<br>UDP - Datagram</td></tr><tr><td>네트워크<br>(Network)</td><td>데이터 전송 시 <strong>네트워크 연결 관리</strong>, <strong>라우팅(최적의 경로 설정)</strong></td><td>IP, IPSec, IGP, RIP, OSPF, EGP, BGP, ICMP, IGMP, ARP, RARP</td><td>라우터</td><td>Packet</td></tr><tr><td>데이터링크<br>(Data Link)</td><td><strong>MAC 주소 사용</strong>, 연결 설정/유지/종료, <strong>오류제어, 순서 제어, 흐름 제어</strong>, <strong>동기화</strong></td><td>Ethernet, IEEE 802, HDLC, X.25, ATM, <strong>Token Ring, PPP, LAPB, LLC, MAC, LAPD, Frame relay, ISDN, FDDI</strong></td><td>랜카드, 브리지, 스위치</td><td>Frame</td></tr><tr><td>물리<br>(Physical)</td><td><strong>두 장치 간 실제 접속 및 절단</strong>, 데이터의 신호변환</td><td>RS-232C, PSTN, <strong>X.21, DSU, CSU, 10 BASE-T, DSL</strong></td><td>허브, 리피터</td><td>Bit</td></tr></tbody></table>

### 문제

    송수신 측 간의 관련성을 유지하고 프로세스 간의 `대화 제어`(DialogueControl) 및 `동기점`(Synchronization Point)을 이용한 `효율적인 데이터 복구`를 제공하는 `OSI 참조 모델의 계층`을 쓰시오

> 세션

## 네트워크 관련 장비

- 네트워크 인터페이스 카드(NIC, Network Interface Card)

  랜카드

- 허브(Hub)

  컴퓨터 연결

  - 더미
  - 스위칭

- 리피터(Repeater)

  신호 증폭 (4개 이하로 쓰자)

- 브리지(Bridge)

  허브 + 허브 할때 (동일한 프로토콜 연결한것)

- 스위치(Switch)
- 라우터(Router)

  최적의 경로 설정

- 게이트웨이(Gateway)

  출입구 / 다른 프로토콜을 연결

### 문제

    다음이 설명하는 네트워크 관련 장비를 쓰시오.

```
- 디지털 회선의 중간에 위치하는 것으로, `거리가 증가할수록
 감쇠`하는 디지털 신호의 장거리 전송을 위해 수신한 신호를
 새로 재생시키거나 출력 전압을 높여 전송하는 장치이다

- OSI 참조 모델의 물리 계층에서 동작하는 장비이다.
```

> 리피터

## TCP/IP

    인터넷에 연결된 서로 다른 기종의 컴퓨터들이 데이터를 주고받을
     수 있도록하는 표준 프로토콜

![](/img/tcp.png)

- ARP, RARP

  ip >> mac (ARP), ip << mac (RARP) 주소를 바꾸는 거

- ICMP

  ip 에서 발생하는 문제를 처리하기 위한 프로토콜

- TCP

  신뢰성 있는 전송 연결성형 서비스

- IP

  비신뢰성, 비연결성 서비스

- UDP

  비 신뢰성, 비연결형 서비스

- SNMP

  네트워크를 관리, 감시하고 총괄 프로토콜

- TFTP

  더 단순한 방식으로 송수신
  FTP(file transfer protocol) : 파일을 송수신하는 프로토콜

### 문제

    다음이 설명하는 프로토  콜을 쓰시오.

```
- 컴퓨터와 컴퓨터 또는 컴퓨터와 인터넷 사이에서
파일을 주고받을 수 있도록 하는 원격 파일 전송 프로토콜이다.

- TCP/IP 응용 계층의 주요 프로토콜이다.
```

> FTP (file transfer protocol)

## 데이터 교환 방식/라우

### 데이터 교환 방식

![](/img/DT.png)

## 데이터 교환 방식/라우팅

### 라우팅(Routing, 경로 제어)

- IGP

  내부에서 사용되는 라우팅

  - RIP

    소규모, 가장 널리 사용, 홉 15개 제한

  - OSPF

    대규모, 라우팅 정보에 변화가 생길때만

- EGP

  외부에서 사용되는 라우팅

- BGP

  EGP 단점 보안

### 문제

    단말장치 상호간 논리적인 가상 통신 회선을 미리 설정하여
     송신자와 수신자 사이의 연결을 확립한 후에 설정된 경로를
     따라 패킷들을 순서적으로 운반하는 패킷 교환 방식의 명칭을
      쓰시오.

> 가상 회선 방식
