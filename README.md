# 공공데이터 API를 활용한 스마트 사과 판매 플랫폼

## 프로젝트 개요
- 목표: 사과 판매 플랫폼 개발, 사과 가격 시장가격 API 가져와서 연결, 시각화하기
- 기술 스택: Java, Spring Boot (Maven) / HTML, CSS / Thymeleaf
- 주요 기능:
- 사용자 관리 (회원가입, 로그인, 정보 수정)
- 상품 관리 (상품 등록, 수정, 삭제)
- 주문 관리 (장바구니, 주문 처리)
- 관리자 기능 (사용자 관리, 상품 관리)

## 디렉토리 구조
```
Project_Sprint1_apple-shop
├─ .mvn
│  └─ wrapper
│     └─ maven-wrapper.properties
├─ .vscode
│  ├─ launch.json
│  └─ settings.json
├─ HELP.md
├─ mvnw
├─ mvnw.cmd
├─ pom.xml
├─ README.md
├─ src
│  ├─ main
│  │  ├─ java
│  │  │  └─ com
│  │  │     └─ project
│  │  │        └─ kyhshop
│  │  │           ├─ controller
│  │  │           │  ├─ AdminController.java
│  │  │           │  ├─ CategoryController.java
│  │  │           │  ├─ OrderController.java
│  │  │           │  ├─ PasswordController.java
│  │  │           │  ├─ ProductController.java
│  │  │           │  ├─ SellerController.java
│  │  │           │  └─ UserController.java
│  │  │           ├─ dao
│  │  │           │  ├─ AdminDao.java
│  │  │           │  ├─ CategoryDao.java
│  │  │           │  ├─ FindDao.java
│  │  │           │  ├─ OrderDao.java
│  │  │           │  ├─ ProductDao.java
│  │  │           │  ├─ SellerDao.java
│  │  │           │  └─ UserDao.java
│  │  │           ├─ KyhshopApplication.java
│  │  │           ├─ service
│  │  │           │  └─ EmailService.java
│  │  │           └─ util
│  │  │              └─ RandomString.java
│  │  └─ resources
│  │     ├─ application.properties
│  │     ├─ static
│  │     │  ├─ css
│  │     │  │  ├─ category.css
│  │     │  │  ├─ homepage2.css
│  │     │  │  ├─ list.css
│  │     │  │  ├─ login.css
│  │     │  │  └─ register.css
│  │     │  └─ images
│  │     │     ├─ [이미지 목록]
│  │     └─ templates
│  │        └─ html
│  │           ├─ admin
│  │           │  ├─ adminpage.html
│  │           │  ├─ product.html
│  │           │  ├─ sellerlist.html
│  │           │  └─ userlist.html
│  │           ├─ alert.html
│  │           ├─ common
│  │           │  ├─ categorylist.html
│  │           │  ├─ homepage2.html
│  │           │  ├─ login.html
│  │           │  ├─ my.html
│  │           │  └─ regiselect.html
│  │           ├─ order
│  │           │  ├─ cart_order.html
│  │           │  ├─ complete.html
│  │           │  └─ order.html
│  │           ├─ product
│  │           │  ├─ allproduct.html
│  │           │  └─ product.html
│  │           ├─ seller
│  │           │  ├─ [기타 seller 관련 템플릿]
│  │           ├─ user
│  │           │  ├─ [기타 user 관련 템플릿]
│  │           └─ [기타 템플릿]
│  └─ test
│     └─ java
│        └─ com
│           └─ project
│              └─ kyhshop
│                 ├─ [테스트 관련 파일]
│                 └─ [기타 파일]
```

## 팀 소개
| 이름       | 역할                                   |
|------------|----------------------------------------|
| 김정연     | 프로젝트 매니저, 총괄 관리              |
| **김민형** | 프론트 전담 및 백엔드 파트 구현 지원   |
| 안시형     | 백엔드 메인 개발, 서버 로직 및 API 설계|
| 이동연     | DB 및 백엔드 관리, 공공데이터 API 통합 |

## 기술 스택
| 구분       | 기술                                      |
|------------|------------------------------------------|
| 프론트엔드 | HTML, CSS, JavaScript                    |
| 백엔드     | Django                                   |
| 데이터베이스| MySQL                                   |
| API        | 공공데이터 API                          |

## 설치 및 실행 방법
###### Maven과 JDK 설치

###### 프로젝트 클론
```git clone <repository-url>```
```cd Project_Sprint1_apple-shop```

###### 의존성 설치
```./mvnw clean install```

###### 애플리케이션 실행
```./mvnw spring-boot:run```

## 개요
- **목적**: 합리적인 사과 구매 플랫폼 제공
- **필요성**: 신뢰할 수 있는 가격 정보 제공
- **차별점**: 계절별 상품 가격 변화 시각화
- **목표**: 사용자 친화적인 인터페이스, 효율적인 판매 시스템

## 기능
### 구매자
- 상품 판매가격 정보 제공
- 최저가 확인 기능
- 바로 구매 및 장바구니 기능

### 판매자
- 시장 판매가 통계 제공
- 상품 등록, 삭제, 수정 기능
- 주문 정보 확인 및 배송 상태 관리

### 관리자
- 회원 관리 기능
- 회원 정보 수정 및 삭제
- 카테고리 관리 기능

## 화면 흐름
- **홈페이지**: 웹사이트 로고, 카테고리, 상품 조회, 회원가입 및 로그인
- **회원가입**: 회원 유형 선택, 비밀번호 규칙 적용
- **로그인**: 아이디 및 비밀번호 찾기 기능
- **마이페이지**: 주소 설정, 개인정보 수정, 상품 관리 기능

## 테스트 과정 및 개선사항
| 문제                                      | 해결                                          |
|------------------------------------------|---------------------------------------------|
| 재고량 초과 주문 오류                    | 장바구니 데이터베이스 연동 개선           |

> 오류 테스트 및 개선 사항:  
> 테스트 과정에서 발견된 주요 문제는 재고량을 초과하여 주문이 가능한 오류였습니다. 이를 해결하기 위해 장바구니 데이터와 재고 수량을 비교하는 로직을 추가하였습니다. 또한 UX 테스트를 통해 디자인 일관성을 높이기 위한 개선 작업을 진행하였습니다.

## 향후 발전 방향
- 다양한 과일 데이터 활용 (사과 이외의 과일 등)
- 사용자 경험 개선 (보다 자연스럽고 이해가 쉬운 UI 구현)
