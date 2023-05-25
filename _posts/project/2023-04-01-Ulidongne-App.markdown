---
index: 2
permalink: /project/Ulidongne-App
---

#### **Introduction**

"우리동네"는 동일한 동네에 사는 사람들을 위한 안드로이드 어플리케이션이며, 사용자들이 공유하는
취미와 관심사를 기반으로 다른 사람들과 온라인 및 오프라인에서 일정을 잡을 수 있다.
사용자들은 앱을 통해 자신의 취미, 관심사를 등록하고, 동일한 동네에 있는 다른 사용자들과
쉽게 소통하며 일정을 조율할 수 있다.
이를 통해 우리 동네에서 다양한 활동을 공유하고 함께 즐길 수 있는 기회를 제공한다.

<br>

#### **Functionality**

| 페이지           | 세부기능             | 설명                                                       |
| ---------------- | -------------------- | ---------------------------------------------------------- |
| 메인화면         | 추천모임             | 내관심사와 동일한 모임 회원수 기준 추천                    |
|                  | 우리 동네 일정       | 우리동네 일정 출력                                         |
|                  | 신규 모임            | 최근 개설된 모임 추천                                      |
| 모임 상세 페이지 | 모임 가입            | 모임 가입 신청                                             |
|                  | 모임 탈퇴            | 모임 탈퇴                                                  |
|                  | 일정 참여/취소       | 일정 참여, 불참                                            |
|                  | 회원 채팅            | 같은 모임 회원간 채팅                                      |
|                  | 가입 승인/거절       | 모임장이 가입 신청 승인/ 거절                              |
| 더보기           | 내 정보 수정         | 내 정보 수정                                               |
|                  | 내 관심사 수정       | 관심사를 수정 (3~5개)                                      |
|                  | 가입한 모임 조회     | 내가 가입한 모임을 조회                                    |
| 위치 설정        | 위치 검색            | 모임, 회원 위치 등을 설정                                  |
| 모임 검색        | 키워드 검색          | 자신의 동네를 기준으로 키워드를 통해 모임을 검색           |
|                  | 관심사 + 키워드 검색 | 자신의 동네를 기준으로, 키워드와 관심사를 통해 모임을 검색 |
| 설정             | 공지사항             | 공지사항을 출력.                                           |
|                  | 회원탈퇴             | 회원에서 탈퇴                                              |
| 모임 만들기      | 모임 생성            | 모임을 생성                                                |
| 일정 만들기      | 일정 생성            | 해당 모임의 일정을 생성                                    |

<br>

#### **Development Environment**

<table>
  <tbody>
    <tr>
      <td>OS</td>
      <td>Windows 10</td>
    </tr>
    <tr>
      <td>Language</td>
      <td>Java, JavaScript, HTML/CSS, Kotlin</td>
    </tr>
    <tr>
      <td>Tool</td>
      <td>VS Code, SpringBoot, IntelliJ, Bootstrap5, Github</td>
    </tr>
    <tr>
      <td>Server</td>
      <td>Tomcat 9</td>
    </tr>
    <tr>
      <td>DB</td>
      <td>MariaDB, AWS RDS</td>
    </tr>
    <tr>
      <td>Deploy</td>
      <td>Github Actions, AWS Code Deploy, AWS S3, AWS EC2</td>
    </tr>
  </tbody>
</table>

<br>

#### **ERD**

![Figure2](/assets/project/Mysoho-Shopping-Mall-Website/Figure1.PNG)

<br>

#### **Deploy**

GitHub Actions를 통해 소스 코드를 빌드하고, AWS S3에 아티팩트를 업로드했다. 다음으로, AWS CodeDeploy를 설정하고, 배포 대상 EC2 인스턴스에 애플리케이션을 배포한 후, 결과를 확인하는 과정을 거쳤다.

![Figure2](/assets/project/Mysoho-Shopping-Mall-Website/Figure2.PNG)

다음으로 구글 플레이 스토어에 앱을 배포하였다. 과정은 다음과 같다.

1. 구글 플레이 콘솔에 접속하여 개발자 계정을 생성
2. 앱의 기본 정보를 등록하고, APK 파일을 빌드하여 생성
3. 앱이 개인정보를 수집하는 경우, 개인정보 처리 방침을 제공
4. 배포 정보를 설정하여 앱을 등록.
5. 구글 플레이 스토어의 정책을 준수하고, APK 파일과 배포 정보를 제출
6. 앱이 심사를 통과하면 구글 플레이 스토어에 배포

![Figure2](/assets/project/Ulidongne-App/Figure3.jpg)

<br>

#### **Demo Video**

[![시연 영상](http://img.youtube.com/vi/99-g5Yfwi38/0.jpg)](https://www.youtube.com/watch?v=99-g5Yfwi38)

<br>

#### **Report**

[완료보고서](https://github.com/psk910903/UlidongneProject/blob/main/우리동네%20완료보고서.pdf)

<br>

#### **Reference**

[우체국 주소 데이터](https://www.epost.go.kr/search/zipcode/cmzcd002k01.jsp)
