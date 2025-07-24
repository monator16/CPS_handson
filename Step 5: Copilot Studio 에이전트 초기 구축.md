# Step 5: Copilot Studio 에이전트 초기 구축


1. Copilot Studio 환경으로 이동합니다.
    - 커넥터가 빌드된 동일한 Power Platform 환경(copilot workshop12 등)에 있는지 확인합니다.
    - New agent(새 에이전트 만들기) 를 클릭하여 에이전트 만들기를 시작합니다.
      <img width="1495" height="431" alt="image" src="https://github.com/user-attachments/assets/505e0623-95f4-489b-9f8e-bbd0fbd0bd20" />


2. 에이전트 설정
   - 에이전트 이름을 "Events Agent"와 같이 지정하고, 에이전트가 수행할 작업에 대한 초기 지침을 정의합니다. 정의한 후 **만들기**버튼을 클릭하여 에이전트를 생성합니다.
     > 예를 들어, "이 에이전트는 사용자 지정 커넥터를 사용하여 예정된 이벤트에 대한 세부 정보를 가져올 수 있습니다(this agent will be able to get details about upcoming events using a custom connector)"와 같은 설명을 추가합니다.
     > 지침은 아래 예시처럼 대화로 입력하지 않고, 구성으로 건너뛰기를 클릭하여 명시적으로 지침을 입력하여도 괜찮습니다.
     
     <img width="1542" height="638" alt="image" src="https://github.com/user-attachments/assets/c1e67486-ff35-4578-98c2-0ccc7a445353" />

3. 에이전트 세부 세팅
     - 에이전트가 일반적인 지식 데이터(예: 2023년의 Oasis 정보)를 사용하지 않고, 오직 우리가 구축할 사용자 지정 커넥터를 통해서만 실시간 데이터를 조회하도록 '일반 지식(general knowledge)' 기능을 비활성화합니다.
      - 상단의 설정에 들어갑니다.
        <img width="1467" height="225" alt="image" src="https://github.com/user-attachments/assets/43f74733-73b0-4b00-b637-b0358966fd87" />
      - 생성형 AI 설정의 "일반 참조 자료 사용"을 끄기로 변경한 후 저장합니다.
        <img width="1435" height="877" alt="image" src="https://github.com/user-attachments/assets/5d89be62-fa61-42f8-a230-e35e7a641f5e" />

