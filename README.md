## Bucketplace api Automation
Postman을 사용하여 Kakao API를 테스트하는 자동화 프로젝트입니다. GitHub Actions를 통해 CI/CD 파이프라인에서 자동으로 테스트를 실행합니다.

## 요구 사항
GitHub 계정
Postman 컬렉션 파일
Kakao API Key (GitHub Secrets 설정 필요)

## 설정 방법
### 1. GitHub Secrets에 Kakao API Key 추가
GitHub 리포지토리로 이동합니다.
오른쪽 상단의 Settings를 클릭합니다.
왼쪽 메뉴에서 Secrets and Variables > Actions를 선택합니다.
New repository secret 버튼을 클릭합니다.
Name에는 KAKAO_API_KEY, Value에는 Kakao API Key를 입력합니다.
Add secret 버튼을 클릭하여 저장합니다.

### 2. Postman 테스트 자동화 실행
GitHub Actions에서 Postman 테스트를 실행하려면, main 브랜치에 푸시할 때 자동으로 실행되도록 설정되어 있습니다. 또한, 수동 실행 및 스케줄 기반 실행이 가능합니다.

#### 수동 실행
Actions 탭에서 수동으로 워크플로우를 실행할 수 있습니다.

#### 스케줄 기반 실행
평일 오전 11시에 Kakao API 테스트가 자동으로 실행됩니다. (크론 표현식에 의해 설정됨)

### 3. GitHub Actions 워크플로우
이 워크플로우는 main 브랜치에 푸시될 때, 또는 수동으로 트리거될 때 Kakao API를 테스트합니다.

## API 테스트
테스트는 Kakao API의 스타벅스, 설탕벅스 검색 기능을 기반으로 실행됩니다. API 요청과 응답을 확인하고, 지정된 조건을 만족하는지 검증합니다.
