## 📌 Team
<table>
  <tr>
    <td align="center" colspan="1">
      <b>Frontend</b>
    </td>
    <td align="center" colspan="1">
      <b>Frontend</b>
    </td>
    <td align="center" colspan="1">
      <b>Backend</b>
    </td>
    <td align="center" colspan="1">
      <b>Backend</b>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://avatars.githubusercontent.com/u/101538592?v=4" width="120px" height="15%"/>
    </td>
    <td>
      <img src="https://avatars.githubusercontent.com/u/97885933?v=4" width="120px" height="15%"/>
    </td>
    <td>
      <img src="https://avatars.githubusercontent.com/u/101448999?v=4" width="120px" height="15%"/>
    </td>
    <td>
      <img src="https://avatars.githubusercontent.com/u/99639919?v=4" width="120px" height="15%"/>
    </td>
  </tr>
  <tr>
    <td align="center">
      <a href="https://github.com/Ginieee">
      강어진
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/anonymousRecords">
      민세림
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/ziiyouth">
      박지영
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/OJOJIN">
      오진영
      </a>
    </td>
  </tr>
</table>

## 📌 Summary
<table>
    <tr>
        <th>기간</th>
        <td>2023-08-29 ~ 23-08-30 (총2일)</td>
    </tr>
    <tr>
        <th>배포</th>
        <td><a href="https://wantload-fe.vercel.app/">wantload</a></td>
    </tr>
</table>

## 📌 서비스 개요
<img width="1645" alt="img" src="https://github.com/2023-venture-startup-hackathon-wantload/.github/assets/97885933/81ccac72-865a-4e0b-8705-a17e7f908e41">

> 📢 서비스명

**WantLoad** : 기다려지는 로딩화면, 원트로드

> 📢 한줄 소개

과도한 트래픽으로 인한 지연은 필연적이기 때문에 해당 로딩 시간에 사용자들에게 즐거운 경험을 갖게 해주자는 목표로 제작된 서비스 입니다.

> 📢 개발 동기

해당 트랙의 주제를 접했을 때 처음에는 서버의 성능을 높이는 MSA구조를 사용한 scale-out 방식이나 확장에 용이한 Serverless 방식으로 서버를 구상하여 문제를 해결하는게 당연하지 않을까 생각했었습니다.
하지만 팀원들과 이야기를 나누다 보니 기업 측면에서 무작정 서버를 확장한다면 **비용적 부담**이 생기기 마련이며, 아무리 잘 짜여진 구조의 서버라고 해도 매우 **단시간에 몰리는 트래픽**에 대해서는 지연을 가질 수 밖에 없다고 결론지었습니다.

만약, 엘레베이터가 느리다는 불편 건의를 받으면 어떻게 해결해야 할까요?
가장 먼저 엘레베이터의 알고리즘 혹은 하드웨어를 변경하는 방법이 있을 수 있습니다. 하지만 이 방법은 큰 비용과 많은 시간을 필요로 합니다. 우리는 이 때 엘레베이터에 거울을 설치하는 방안을 생각해 보자는 것입니다.
엘레베이터 이용자들은 거울을 보는 시간 동안 자신이 오래 기다리고 있다는 사실을 인지하려고 하지 않습니다.

이에 따라 서버에 트래픽이 몰려 이미 지연이 발생하는 상황에서 사용자가 단순히 빙빙 돌아가는 로딩 화면을 보는 것이 아닌 트래픽으로 인한 **지연을 인지하지 못하게 만드는 긍정적인 서비스 경험을 제공하는 방향**으로 문제를 해결하고자 하였습니다.

## 📌 세부 내용
### 🔗 핵심기능 1 - 오늘의 운세
동접자 500명 이하의 일시적 트래픽일 때, 
단시간 동안 사용자의 이목을 끌며 상품 홍보 효과까지 얻을 수 있는 오늘의 운세 서비스
- 재물운, 금전운, 성공운 중 사용자가 보고 싶은 항목의 운세를 선택 가능한 방식이다.
- 하단에는 나의 대기 번호를 볼 수 있고, 번호가 0이 되면 다음 페이지로 넘어가는 버튼이 활성화된다.
- 선택 뒤에는 운세와 함께 짧은 문구, 설명, 운세와 어울리는 항목의 아이템을 추천해준다.
### 🔗 핵심기능 2 - 카드 뒤집기 게임
동접자 500명 이상의 장기적 트래픽일 때, 
긴 시간 동안 사용자가 게임을 즐기며 지루함을 덜어줄 수 있는 카드 게임 서비스
- 상품 이미지들로 이루어진 카드 뒤집기 게임을 제공한다.
- 하단에는 나의 대기 번호를 볼 수 있고, 번호가 0이 되면 다음 페이지로 넘어가는 버튼이 활성화된다.
- 고득점자에게 상품을 걸어 쿠폰과 같은 혜택 제공하는 보상 방식을 도입한다.

### 🔗 트래픽 모니터링 방식
AWS에서 제공하는 AWS Virtual Waiting Room 서비스를 구축하여 서비스의 사용자들을 대기 시켜두고 대기자 수를 파악하려 했지만… CloudFormation, AWS Lambda, AWS DynamoDB, AWS SQS, AWS ElasticCache for Redis 등 사용해보지 않은 기술들이 다수였다. 답답한 마음을 가지고 멘토분들에게도 여쭤보니 하루 안에 제대로 동작하게 만들기는 힘들 것이라는 답변을 듣고 조금 더 시도해보다가 CloudFormation 에서 stack설정하는 부분부터 막혔다. 
결국 임시로 유저의 트래픽 정도를 알 수 있게 EC2 내에서 빠른 접근이 가능한 Redis를 통해 대기자 수를 담아 가상의 유저 수를 1초마다 들어오고 나가는 것을 구현하는 방향으로 동시 접속자 트래픽을 가정하였다.

### 🔗 사용 기술 및 인프라
- 사용 기술 :
  - **Front-end** : React, TypeScript, ReactQuery 및 Axios
  - **Back-end** :
      - Spring : Server 구축, API 설계
      - Mysql : 상품 등 각종 정보를 담는 RDB 구축
      - Redis : AWS Virtual Waiting Room 서비스 구축 실패에 따른 가상 트래픽을 가지는 Waiting room 자체 구현, 게임 서비스 “”의 리더보드 구축
  - **Infra** :
      - AWS EC2 : Spring Boot 서버 배포, Redis 관리
      - AWS RDS : Mysql 구축한 클라우드 스토리지
      - AWS S3 : 상품 이미지를 담는 클라우드 오브젝트 스토리지

### 🔗 플로우차트/서비스 구조도
<img width="673" alt="image" src="https://github.com/2023-venture-startup-hackathon-wantload/.github/assets/97885933/514871d6-c12e-4cab-95ec-dc2f4dec0365">
<img width="679" alt="image" src="https://github.com/2023-venture-startup-hackathon-wantload/.github/assets/97885933/1289c649-a44e-4960-b188-8e753f430f1f">

## 📌 기대 효과
- 과도한 트래픽이 한 번에 도달했을 때는 서버리스 혹은 로드밸런싱도 한계가 있기 때문에 이러한 접근 방식이 기술적으로도 도움이 될 것이라고 생각함.
- 트래픽 과부화로 인한 로딩 페이지 접속 시 사용자의 지루함을 다양한 방식으로 해소하여 사용자 이탈을 막고자 함.
- 해당 로딩 페이지에서 본 이커머스 서비스에 대한 정보와 판매 상품 등을 좀 더 홍보하는 창구로 이용해 자연스레 행사 상품에 대한 관심을 늘려 이커머스 서비스의 매출에도 도움을 주고자 함.
- 현재는 가상으로 사용자의 트래픽을 받아왔지만 추후 인프라를 제대로 구축한다면 AWS Virtual waiting room을 통해 트래픽을 처리할 수 있을 것임.
