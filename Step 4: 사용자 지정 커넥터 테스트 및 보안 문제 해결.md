
# Step 4 – 사용자 지정 커넥터 테스트 및 보안 문제 해결

> **목표:** Power Platform 사용자 지정 커넥터의 **테스트(Test)** 탭에서 실제 호출을 수행하고, **보안/인증 관련 오류를 해결**합니다.


---

## 🔧 준비물 (Prerequisites)

* **Step 3**까지 완료된 사용자 지정 커넥터
* Ticketmaster **API 키(API key)**

---

## 1. 테스트(Test) 탭에서 연결 생성 및 선택

1. 커넥터 편집 화면에서 **테스트(Test)** 탭으로 이동합니다.
2. 아직 연결이 없다면 **새 연결 만들기(Create a new connection)** 버튼을 클릭합니다.

   * 창이 뜨면 **API 키(apikey)** 입력 후 저장합니다.

![새 연결 만들기 화면](https://github.com/user-attachments/assets/938d21f7-388b-4748-8382-96c6b8847e56)
![API 키 입력 화면](https://github.com/user-attachments/assets/3cf463a5-a2a8-46be-a8d7-2b0c6709005e)

3. 연결을 만든 뒤 테스트 탭으로 돌아오면, 오른쪽 상단의 **새로고침(Refresh)** 버튼을 눌러 방금 만든 연결을 선택합니다.

![연결 선택 화면](https://github.com/user-attachments/assets/fb41fce6-d7de-4a0c-8d22-a12dfc4239fe)

---

## 2. 파라미터 입력 후 테스트 실행

1. `keyword(키워드)` 파라미터에 `Oasis` 등 원하는 검색어를 입력합니다.

   * 필요 시 `city(도시)`, `startDateTime(시작일시)` 등 다른 파라미터도 입력 가능
2. **테스트 작업(Test operation)** 버튼을 클릭합니다.
3. 아래처럼 응답(JSON)이 성공적으로 표시되면 테스트 성공입니다.

![테스트 성공 예시](https://github.com/user-attachments/assets/a267afe1-22a7-43ae-a89c-d06c7d4e4c38)

---




