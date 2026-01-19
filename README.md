# 📝 프로그램 개요서: 업무 말투 변환기 (Biz-Talk Converter)
본 프로그램은 사용자가 입력한 핵심 정보를 바탕으로, 수신자(상사, 동료, 고객)의 특성에 최적화된 비즈니스 메시지로 변환해주는 서비스입니다.

## 1. 프로젝트 목적
* 커뮤니케이션 효율화: 메신저나 이메일 작성 시 말투 고민에 소요되는 시간 단축
* 전문성 유지: 상황별(보고, 협조 요청, 공지 등) 적절한 비즈니스 에티켓 적용
* 오해 방지: 정중하고 명확한 표현을 통해 업무 협업 효율 증대

## 2. 주요 기능
멀티 페르소나 변환:
* 상사(Upward): 정중함, 격식체, 결론 중심 보고형
* 타팀 동료(Lateral): 친절함, 협조 요청형, 명확한 데드라인 명시
* 고객(External): 극존칭, 서비스 마인드 강조형, 안내/사과 중심

간편 입력: 핵심 키워드(Who, When, What, Why)만 입력해도 문장 완성

복사 및 전송: 변환된 메시지 즉시 복사 기능

## 3. 기술 스택 (Tech Stack) 및 시스템 아키텍처
#### Frontend: 
* 사용자 인터페이스 제공 및 변환 요청 전송
* 간단한 HTML, CSS, JavaScript(Vanilla JS)
#### Backend:
* 클라이언트 요청 수신 및 Gemini API 연동 처리
* Python Flask 프레임워크
* 라우팅 및 API 엔드포인트 처리
* Gemini API: 입력된 텍스트를 대상에 맞는 말투로 재구성(Prompt Engineering 적용)하는 역할은 AI 모델을사용하는 Gemini API 활용
#### Deploy:
* Firebase Hosting
* 전체 애플리케이션 호스팅 및 백엔드 함수(Functions) 실행

## 4. 단계별 개발 계획
#### 1단계: 환경 설정 및 API 연동
* Google AI Studio API 키 발급
* Flask 서버 기본 구조 설정 및 Gemini API 연동 테스트

#### 2단계: 프론트엔드 UI 개발
* 입력창(Input), 대상 선택(Radio/Select), 결과창(Result) 구현
* 사용자 경험을 고려한 반응형 CSS 적용

#### 3단계: 백엔드 로직 구현
* 수신자별 프롬프트 템플릿 설계
* Flask 엔드포인트(. /convert) 개발

#### 디렉토리 규칙
backend와 frontend 코드는 
#### 4단계: 배포 (Firebase)
* Firebase 프로젝트 생성 및 설정
* firebase-tools를 이용한 Hosting 및 Cloud Functions 배포