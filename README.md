# 일정 관리 앱 만들기 프로젝트

# 개요


# 실행방법


# 프로젝트 구조

# API 명세서 (요청응답코드 수정예정)

| FUNCTION         | METHOD | URL                        | REQUEST                                                                                                                                                 | RESPONSE                                                                                                                                                                  | STATUS CODE   |
|------------------|--------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| 스케줄 등록      | POST   | /api/schedules             | 요청 body  {  "scheduleName" : "버거킹"  "sponserName" : "서울오빠"  "sponserOffers" : "50,000원"  "location" : "서울 강남"  "deadline" : "25.04.12"  } | 등록 정보  {  "scheduleId : 1"  "scheduleName" : "버거킹"  "sponserName" : "서울오빠"  "sponserOffers" : "50,000원"  "location" : "서울 강남"  "deadline" : "25.04.12"  } | 200: 정상등록 |
| 스케줄 삭제      | DELETE | /api/schedules{scheduleId} | 요청 params  {  scheduleId : 1  }                                                                                                                       | 삭제 정보  {  scheduleId : 1  }                                                                                                                                           | 200: 정상삭제 |
| 스케줄 편집      | PUT    | /api/schedules{scheduleId} | 요청 body                                                                                                                                               | 수정 정보                                                                                                                                                                 | 200: 정상수정 |
| 스케줄 단건 조회 | GET    | /api/schedules{scheduleId} | 요청 params                                                                                                                                             | 단건 응답 정보                                                                                                                                                            | 200: 정상조회 |
| 스케줄 다건 조회 | GET    | /api/schedules{scheduleId} | 요청 params                                                                                                                                             | 다건 응답 정보                                                                                                                                                            | 200: 정상조회 |

# ERD

---



# API 

| FUNCTION                 | METHOD | URL                        | REQUEST                                                                                                                                                          | RESPONSE                                                                                                                                                          | STATUS CODE |
|--------------------------|--------|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Schedule updates         | POST   | /api/schedules             | request body {  "scheduleName" : "burgerking" "sponserName" : "seoul ouba" "sponserOffers" : "50,000won" "location" : "seoul gangnam" "deadline" : "13.04.25"  } | response info  {  "schedulName" : "burgerking" "sponserName" : "seoul ouba" "sponserOffers" : "50,000won" "location" : "seoul gangnam" "deadline" : "13.04.25"  } | 200         |
| Schedule deletions       | DELETE | /api/schedules{scheduleId} | Request params                                                                                                                                                   | deletions info                                                                                                                                                    | 200         |
| Schedule edit            | PUT    | /api/schedules{scheduleId} | Request body {  }                                                                                                                                                | edit info                                                                                                                                                         | 200         |
| Schedule search          | GET    | /api/schedules{scheduleId} | Request params                                                                                                                                                   | One response info                                                                                                                                                 | 200         |
| Schedule multiple search | GET    | /api/schedules{scheduleId} | Request params                                                                                                                                                   | Several response info                                                                                                                                             | 200         |
