Naver Pay

<aside>
📌 **프로젝트 주제**

</aside>

- MVC 기반 네이버페이 웹 기능 구현 프로젝트 `팀별 프로젝트` 🫂

<aside>
🗓️ **프로젝트 일정**

</aside>

| 일정 | 기간 | 제출방법 | 비고 |
| --- | --- | --- | --- |
| 프로젝트 소개 | 22.10.31 (월) |  |  |
| 프로젝트 기간 | 22.10.31 (월) ~ 11.13 (일) |  |  |
| 프로젝트 제출일자 | 22.11.13 (일) 23:59분 | https://github.com/FastCampusKDTBackend/KDT3_Spring_ToyProject_NaverPay |  |
| 발표일정 | 22.11.14 (월) |  |  |

<aside>
📌 **프로젝트 정의서**

</aside>

- [네이버페이](https://pay.naver.com/about) 사용자 메인 페이지 기능 구현
- `주의사항` ✨
    - 구현 범위에서 `뷰` 단은 모두 제외
        - 간단하게 출력하는 식으로 뷰를 만들거나 뷰 없이 바로 `Controller` 단에서 테스트 하면 됩니다!
    - API 설계는 네이버페이와 동일하게 할 필요 없음
- 구현 범위
    - [메인 페이지](https://pay.naver.com/about) 로그인 기능
        - (https://nid.naver.com/nidlogin.login?url=http://pay.naver.com)
            
    - 네이버페이의 쇼핑 부분
        - (https://order.pay.naver.com/home)
        - (https://pay.naver.com/payments/detail/20221014NP4742258625)
        - (https://order.pay.naver.com/home/search?serviceGroup=SHOPPING&range.fromDate=2022.10.14&range.toDate=2022.10.31&tabMenu=SHOPPING)
            
            
- URL 설계
    - URL은 직접 설계 [참고](https://sanghaklee.tistory.com/57)
    - Naver Pay와 동일할 필요는 없음
    - 아직  RestAPI를 공부하기 전이므로 `GET, POST` 메소드로만 설계
    
    | 기능 | METHOD | URL | DATA | TABLE |  |
    | --- | --- | --- | --- | --- | --- |
    | 메인 페이지 접근 | GET | localhost:8080 |  |  |  |
    | 로그인 페이지 접근 | GET | localhost:8080/login |  |  |  |
    | 로그인 시도 | POST | localhost:8080/login | Member | MEMBER |  |
    | 네이버페이 접근 | GET | localhost:8080/naver/pay |  |  |  |
    | 네이버페이 쇼핑 리스트 반환 |  |  | List<Shopping> | SHOPPING |  |
    | 쇼핑 리스트 기간 검색 | GET |  |  |  |  |
    | 쇼핑 리스트 기간 검색 결과 반환 |  |  |  | SHOPPING |  |
    | 쇼핑 리스트 상세 페이지 접근 | GET |  |  |  |  |
    | 쇼핑 리스트 상세 리스트 반환 |  |  | List<ShoppingDetail> | SHOPPING / PAYMENT |  |
    | 쇼핑 리스트 상세 리스트 삭제 | POST |  |  | SHOPPING / PAYMENT |  |

<aside>
📌 **프로젝트 채점기준표**

</aside>

- 시나리오 구성 `20`
    - 사용자 페이지에서 발생할 수 있는 시나리오와 기능 및 분석
- URL 설계 `20`
    - 각 기능에 따른 URL 설계
- DB 구조 설계 `10`
    - 각 기능 개발을 위한 DB 구조 설계
- 클래스 설계 `20`
    - Entity, DTO, VO 클래스 설계 `10`
    - DAO 설계 및 기능 구현 `10`
- 시나리오 기능 개발 `30`
    - MVC 구조 계층 설계 `10`
    - 시나리오 기능 개발 및 예외처리 `20`
