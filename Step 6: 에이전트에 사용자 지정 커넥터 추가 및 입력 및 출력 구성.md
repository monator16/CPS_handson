

# Step 6 – 에이전트에 사용자 지정 커넥터 추가 및 입력/출력 구성

> **목표:** Copilot Studio 에이전트에 **사용자 지정 커넥터**(Ticketmaster)를 도구(Tool)로 추가하고, **입력(Inputs)·출력(Outputs) 구성**을 설정합니다. (Step 1\~5와 톤/구성 통일)

---

## 1. 도구(Tool) 추가

1. 상단의 **도구(Tools)** 섹션으로 이동합니다.
2. **도구 추가(Add a tool)** 버튼을 클릭합니다.

![도구 추가 화면](https://github.com/user-attachments/assets/b13435fb-cde3-4e04-8fdb-0dcd4014ef73)

3. 생성해 둔 **Ticket Master 커넥터**(예: `Ticketmaster20250724`)를 찾아 선택 후 에이전트에 추가합니다.

![커넥터 선택 화면](https://github.com/user-attachments/assets/e0f16c33-e549-4b39-9990-09989f007542)

---

## 2. 도구 세부 설정

1. 추가된 커넥터 목록에서 **“이벤트 가져오기”** 동작을 클릭합니다.

![이벤트 가져오기 클릭](https://github.com/user-attachments/assets/d5edef74-1edc-442b-9cc5-a1abdc7368e1)

2. **설명(Description)** 영역에 에이전트가 이 도구로부터 받은 결과를 **어떻게 요약/표현할지**를 작성합니다.

   * 예: “Ticketmaster에서 이벤트를 검색합니다. 사용 가능한 이벤트를 글머리 기호(불릿) 형식으로 요약합니다.”

![설명 작성 예시](https://github.com/user-attachments/assets/ca2d6cc8-2661-4930-bfa2-999e0492952d)

---

### 입력(Inputs) 설정

1. **Inputs** 섹션에서 각 매개변수에 대한 \*\*설명(Description)\*\*을 추가합니다. 대표적으로 다음과 같이 작성할 수 있습니다.

![입력 설정 화면 1](https://github.com/user-attachments/assets/dd3ba87f-2595-4373-b78c-adbfc42bb5ca)
![입력 설정 화면 2](https://github.com/user-attachments/assets/60e75626-11b0-48d6-a654-5043c3887f07)

* **City(도시)**: “이벤트가 열릴 도시를 식별합니다. 제공되지 않으면 비워 둡니다.”


* **Keyword(키워드)**: “아티스트(또는 팀) 이름이 제공되면 포함해야 합니다. 제공되지 않으면 비워 둡니다.”


* **Start Date/Time(시작 날짜/시간)**: “이벤트가 발생할 시작 날짜입니다. 예: 5월 1일을 지정하면 5월 1일 이후의 이벤트를 찾습니다. 제공되지 않으면 비워 둡니다.”
  ![Start Date/Time 설명 예시](https://github.com/user-attachments/assets/0e4b2f13-ca45-4cb0-adcf-3109314c1b06)




2. 각 입력 매개변수의 **‘사용자에게 프롬프트헤야 합니다(Should prompt user)’** 옵션은 체크하지 않은 상태로 둡니다.

   * 사용자 경험 개선을 위해 현재 실습 단계에서는 체크하지 않은 상태로 두었지만, 이후 설정을 변경할 수 있습니다.



