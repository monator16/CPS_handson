

# Step 2 – 사용자 지정 커넥터 초기 설정

> **Step 1을 완료하셨나요?**  
> 이제 Power Platform에서 **Ticketmaster API를 호출할 사용자 지정 커넥터**를 만들어 봅니다.  
> **모든 스텝은 실제 화면을 기준으로 작성**했으며, 스크린샷/아이콘 링크도 함께 제공합니다.

---

## 🔧 준비물 (Prerequisites)

- Power Platform(또는 Power Apps / Power Automate) 접근 권한
- Ticketmaster **API Key** (Step 1에서 발급받은 키)
- 사용할 **아이콘 이미지** (예: Ticketmaster 로고)

---

## 1. Power Platform에서 새 사용자 지정 커넥터 만들기

1. **Power Platform** 포털에 접속합니다.  
2. **새 사용자 지정 커넥터(New custom connector)** 생성 > **빈 상태에서 만들기(Blank)** 선택  
3. 이름을 식별 가능하게 지정합니다.  
   - 예: `TicketMaster20250724`

![새 커넥터 만들기](https://github.com/user-attachments/assets/b80fc5ae-8718-47af-8872-8372628ac012)
![빈 상태에서 만들기 선택](https://github.com/user-attachments/assets/8bbb3225-27c7-4a38-847e-289eab37de2c)



---

## 2. 일반(General) 탭 – 기본 정보 입력

- **Host(기본 호스트 URL)**: `app.ticketmaster.com`  
- **Base URL**: `/discovery/v2` *(선택 입력, 나중에 엔드포인트에서 다시 지정해도 됨)*  
- **Icon**: 아래 링크에서 Ticketmaster 로고를 다운받아 업로드합니다.  
  - 로고 다운로드: https://github.com/monator16/CPS_handson/blob/main/ti7179b1bb-ticketmaster-logo-brand-assets-ticketmaster-uk-business.png

![일반 탭 설정 예시](https://github.com/user-attachments/assets/2407d66f-e19f-479e-bc16-e487e113e7c8)


---

## 3. 보안(Security) 탭 – API Key 인증 설정

1. **Authentication Type**을 **API key**로 선택합니다.  
2. Ticketmaster 문서에 따라 **Parameter label**과 **Parameter name**을 `apikey`로 설정합니다.  
3. **Pass in(전달 위치)**는  **Query**로 지정합니다.


![API 키 인증 설정](https://github.com/user-attachments/assets/9f638705-5e73-4142-bcb6-fbdbafb215fe)

> ⚠️ **중요**: `apikey` 철자를 정확하게 입력하세요. 오타가 나면 인증이 되지 않습니다.

---



## 👉 다음 단계로 이동하기

Step 2를 마쳤다면, 다음 문서 [여기](https://github.com/ChangJu-Ahn/Copilot-Studio-Hands-on/blob/main/%EC%8B%9C%EC%8A%A4%ED%85%9C%20%EC%97%B0%EB%8F%99%20%EC%97%90%EC%9D%B4%EC%A0%84%ED%8A%B8/Step%203%3A%20'%EC%9D%B4%EB%B2%A4%ED%8A%B8%20%EA%B0%80%EC%A0%B8%EC%98%A4%EA%B8%B0'%20%EC%9E%91%EC%97%85%20%EC%A0%95%EC%9D%98.md)로 넘어가세요!  

---

