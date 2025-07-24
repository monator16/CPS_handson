# Step 3 – ‘이벤트 가져오기’ 작업 정의

> **목표:** Power Platform 사용자 지정 커넥터의 **Definition(정의)** 섹션에서 Ticketmaster API 호출용 **“이벤트 가져오기(GetEvents)” 액션**을 만들고, **요청 파라미터**와 **응답 스키마**를 자동으로 정의합니다.


---

## 🔧 준비물 (Prerequisites)

* **Step 2**에서 생성한 사용자 지정 커넥터
* Ticketmaster **API Key**
* 웹 브라우저(Chrome/Edge 등) – JSON 응답 확인용

---

## 1. Definition 탭에서 새 동작(New action) 만들기

1. 사용자 지정 커넥터 편집 화면으로 이동 → **정의** 탭 선택
2. **새 동작** 클릭
3. 아래 예시와 같이 기본 정보 입력

   * **요약**: `이벤트 가져오기`
   * **작업 ID**: `GetEvents`
   * **설명**: 'Ticketmaster에서 이벤트 검색'
   * **표시 여부**: `important`

     * `important`: 사용자에게 항상 우선적으로 표시
     * `advanced`: 추가 메뉴 아래에 숨김
     * `internal`: 사용자에게 숨김

![동작 생성 화면](https://github.com/user-attachments/assets/884f7948-6321-401f-919f-939c55d61b1a)

---

## 2. 샘플 요청으로 파라미터 자동 생성

1. **요청** 영역에서 **샘플에서 가져오기** 클릭
2. 아래 값 입력

   * **동사(HTTP 메서드)**: `GET`
   * **URL**:
     `https://app.ticketmaster.com/discovery/v2/events.json?keyword=Oasis&startDateTime=&city=Manchester`

     > 파라미터 자동 추출을 위한 URL 예시입니다.
     > **apikey는 넣지 않아도 됩니다.** 보안 탭에서 Query로 이미 설정했기 때문입니다.
3. **가져오기** 클릭

   * `keyword`, `startDateTime`, `city` 등 파라미터가 자동으로 생성됩니다.

![샘플 요청 가져오기](https://github.com/user-attachments/assets/2af9fdbf-a002-4bbd-95c6-77bb3f31cd6e)
![추출된 파라미터 확인](https://github.com/user-attachments/assets/fe5bea40-2cfd-4e81-95b8-76b87c19f067)


---

## 3. 샘플 응답 제공으로 응답 스키마 정의

> 실제 JSON 응답을 붙여넣어 **응답** 스키마를 자동으로 생성하면, 커넥터 사용 시 반환 데이터 구조를 명확하게 볼 수 있습니다.

### 3-1. 브라우저에서 JSON 응답 얻기

1. 다음 샘플 URL을 브라우저에 입력합니다. (이번에는 **apikey 필수!**)
   `https://app.ticketmaster.com/discovery/v2/events.json?size=5&apikey={apikey}&keyword=Oasis`

   * `size=5`로 설정해 다양한 필드가 포함된 응답 확보
2. 브라우저에 표시된 **JSON 응답 전체를 복사**합니다.

![브라우저에서 JSON 응답 확인](https://github.com/user-attachments/assets/76ab43f3-03c6-4bbf-a06a-9f95e5499453)

### 3-2. 커넥터 편집 화면에서 응답 스키마 생성

1. 다시 **정의** 탭의 **응답** 영역으로 이동
2. **기본 응답 추가** 클릭
3. 본문(Body) 입력란에 JSON 전체를 붙여넣고 **가져오기**
4. `default` 박스를 클릭해 저장된 샘플 응답을 확인합니다.

![기본 응답 추가](https://github.com/user-attachments/assets/85a4d7b5-bdeb-49b4-b268-d24a70ad2175)
![default 응답 스키마 확인](https://github.com/user-attachments/assets/10efea53-dd8f-46a1-acf0-26e21d254803)


---

## 4. 커넥터 저장 & 만들기

* 화면 상단의 **Create connector(커넥터 만들기)** 또는 저장 버튼을 눌러 변경 사항을 반영합니다.

![커넥터 만들기 버튼](https://github.com/user-attachments/assets/fe315e73-7968-4011-9252-6434e466aa5c)

---

## 👉 다음 단계로 이동하기

**Step 4: 사용자 지정 커넥터 테스트 및 보안 문제 해결**
[여기](https://github.com/ChangJu-Ahn/Copilot-Studio-Hands-on/blob/main/%EC%8B%9C%EC%8A%A4%ED%85%9C%20%EC%97%B0%EB%8F%99%20%EC%97%90%EC%9D%B4%EC%A0%84%ED%8A%B8/Step%204%3A%20%EC%82%AC%EC%9A%A9%EC%9E%90%20%EC%A7%80%EC%A0%95%20%EC%BB%A4%EB%84%A5%ED%84%B0%20%ED%85%8C%EC%8A%A4%ED%8A%B8%20%EB%B0%8F%20%EB%B3%B4%EC%95%88%20%EB%AC%B8%EC%A0%9C%20%ED%95%B4%EA%B2%B0.md)를 클릭하세요.

---

