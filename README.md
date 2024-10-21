# 📉 AI-Project : 작업자의 실시간 데이터를 이용한 위험 예측 분석 프로젝트

## 📢 프로젝트 소개

* 프로젝트 명 : 작업자 위험 예측 분석 웹서비스
* 수요 기업 : 강남건설, 강남 앤 인코누스 (건설 작업 안전 관리 시스템 개발)
* 문제 정의 : 작업 중 작업자의 안전상태를 실시간으로 감지하여 사고를 예방하는 시스템 부재
* 목표 : 웨어러블 디바이스를 통해 작업자의 생체 신호 및 환경 데이터를 실시간으로 분석하여 위험을 예측하고 작업 환경을 개선하는 웹서비스 구현

## ⏰ 개발 기간

* 2024.8.28(수) ~ 2024.10.7(화)

## 🙋‍♂️ 개발자 소개

* 박동헌 : 팀장, 데이터 분석

* 김현우 : 데이터 분석

* 문동윤 : 백엔드 개발

* 이창수 : 프론트엔드 개발

## 📟 프로젝트 기능 및 화면 소개

* 프로젝트 기능
    * 실시간 위험 모니터링 : 현재 각 작업자의 상태에 대하여 정상/위험 표시, 작업자에 대한 위험 알림
    * 작업자 생체 및 위험 예측 데이터 시각화 : 관리자가 전체 작업자의 정보 관리
    * 경고 및 알림 시스템 구축 : 작업자 위험 상태면 관리자에게 알림 기능

* 화면 소개

  * 메인 화면

     * 실시간 데이터 수신 및 시각화
          * 웹소켓 연결 : 위험 예측 데이터를 실시간으로 수신
          * 시각적 업데이트 : 작업자 상태에 따라 아이콘 색상 변화를 시각화, 외부 온도 실시간 업데이트

     * 작업자 위치 표시(위도, 경도 기반)
          * 지도 랜더링 : 네이버 지도 API로 작업 현장 지도 표시
          * 아이콘 배치 : 작업자의 위도, 경도에 따라 아이콘 표시
          * 위치 업데이트 : 위치 정보 변경 시 아아콘 실시간 갱신

![메인화면](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%EB%A9%94%EC%9D%B8%ED%99%94%EB%A9%B4.png)

   * 작업자별 상태

     * 작업자 상태 모달
          * 작업자 아이콘 클릭시 해당 작업자의 상태창열림
          * 실시간 그래프 시각화(작업자 심박수, 체온)
          * 실시간 상태 정보 표시(심박수, 체온, 위험 예측, 활동)

![작업자 정보 이미지 - 정상](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%EC%9E%91%EC%97%85%EC%9E%90%20%EC%A0%95%EB%B3%B4%20%EC%9D%B4%EB%AF%B8%EC%A7%80%20-%20%EC%A0%95%EC%83%81.png)

![작업자 정보 이미지 - 주의](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%EC%9E%91%EC%97%85%EC%9E%90%20%EC%A0%95%EB%B3%B4%20%EC%9D%B4%EB%AF%B8%EC%A7%80%20-%20%EC%A3%BC%EC%9D%98.png)
   
   * 위험 알림
     
        * 실시간 웹소켓 데이터 수신
             * 백엔드 Flask API로부터 예측 분석 데이터 수신
             * 실시간 위험 알림 팝업: 예측 데이터에 따라 관리자에게 위험 알림 팝업을 표시

![위험 이미지](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%EC%9C%84%ED%97%98%EC%9D%B4%EB%AF%B8%EC%A7%80.png)

   * 일별 전체 위험 빈도 확인
        * REST API를 활용하여 log 테이블에 기록된 위험 예측 이전 데이터 요청 후 화면에 출력
        * 그래프 시각화 (막대 그래프) : 위험, 주의 빈도 수를 비교

![일별 위험 예측](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%EC%9D%BC%EB%B3%84%20%EC%9C%84%ED%97%98%20%EB%B0%8F%20%EC%A3%BC%EC%9D%98.png)

   * 마이페이지
        * 비밀번호 검증 후 접근 가능
        * 비빌변호 변경, 부서 변경 가능
        * 회원 탈퇴 기능 (탈퇴 시 DB에서 해당 데이터 제거)

![마이페이지 - 비밀번호 검증](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%ED%9A%8C%EC%9B%90%20%EC%A0%95%EB%B3%B4%20%EC%88%98%EC%A0%95%20%ED%8E%98%EC%9D%B4%EC%A7%80%20-%20%EB%B9%84%EB%B0%80%EB%B2%88%ED%98%B8%20%ED%99%95%EC%9D%B8.png)

![마이페이지 - 메인](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%ED%9A%8C%EC%9B%90%20%EC%A0%95%EB%B3%B4%20%EC%88%98%EC%A0%95%ED%8E%98%EC%9D%B4%EC%A7%80%20-%20%EB%A9%94%EC%9D%B8.png)

   * 공지사항
        * 페이지네이션 (React Pagination)
        * 글쓰기 및 수정 가능

![공지사항 메인](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%EA%B3%B5%EC%A7%80%EC%82%AC%ED%95%AD%20%EB%A9%94%EC%9D%B8%ED%8E%98%EC%9D%B4%EC%A7%80.png)

![공지사항 상세](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%EA%B3%B5%EC%A7%80%EC%82%AC%ED%95%AD%20%EC%83%81%EC%84%B8%20%ED%8E%98%EC%9D%B4%EC%A7%80.png)

   * 로그인 및 회원가입
        * 로그인
             * 아이디와 비밀번호 입력 후 로그인
             * 로그인 성공 시 토큰 생성
             * 로그아웃 시 토큰 제거
        * 회원가입
             * 아이디 중복확인
             * 비밀번호 검증
             * 회원가입시 DB에 회원 정보 데이터 저장

![로그인](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%EB%A1%9C%EA%B7%B8%EC%9D%B8%20%ED%8E%98%EC%9D%B4%EC%A7%80.png)

![회원가입](https://github.com/Leechangsuuu/project_RiskAnalysis/blob/main/images/%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85%20%ED%8E%98%EC%9D%B4%EC%A7%80.png)

## 결론 및 소감
* 결론 : 실시간으로 작업자의 행동 및 생체 신호를 분석하여 위험 상황을 감지하고 관리자에게 알림을 경고함으로써 작업 현장의 안정성을 중앙 집중 관리
* 소감 : AI 프로젝트는 데이터 분석, 백엔드, 프론트엔드로 역할을 나누어 1달 정도를 진행하었다. 실무에서 작업하는 것처럼 서로의 아이디어를 소통하며 프로젝트를 진행해볼 수 있는 기회가 주어져서 좋았다. 나는 프론트엔드로 진행하였는데 벡엔드와 함께 여러 기능을 웹페이지에 구현하며 하나하나 구현될 때마다 뿌듯했다. 프론트엔드에 더 흥미가 생기는 프로젝트였고 열심히 진행하여 좋은 결과물을 얻어서 뜻깊은 시간이었다. 


      
  
  
