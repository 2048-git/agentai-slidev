---
theme: default
title: 에이전트 AI와 OpenClaw
info: |
  소프트웨어학부 22학번 강지웅 발표용 Slidev 자료
class: minimal-cover
transition: fade
mdc: true
---

<div class="cover-inner">
  <div class="cover-copy">
    <h1 class="cover-title">
      <span class="cover-line">에이전트 AI와</span>
      <span class="brand-mark">OpenClaw</span>
    </h1>
    <p class="cover-credit">소프트웨어학부 22학번 강지웅</p>
  </div>

  <div class="cover-visual" aria-hidden="true">
    <div class="cover-icon"></div>
    <div class="cover-wordmark">OpenClaw</div>
  </div>
</div>

<!--
안녕하세요, 소프트웨어학부 22학번 강지웅입니다.
오늘은 에이전트 AI와 OpenClaw에 대해 발표하겠습니다.
요즘 AI라고 하면 단순히 답만 해주는 챗봇보다,
코딩 에이전트처럼 실제 작업을 수행하는 AI를 먼저 떠올리는 경우가 많습니다.
오늘 발표에서는 그 흐름을 조금 더 넓게 설명하는 개념인 에이전트 AI와,
그 사례로 볼 수 있는 OpenClaw를 간단히 소개해보겠습니다.
-->

---
class: split-slide
transition: slide-left
---

<div class="split-layout">
  <section>
    <p class="section-label">Definition</p>
    <h1>에이전트 AI란?</h1>
    <p class="lead-copy">목표를 받으면 계획하고, 도구를 쓰고,<br>실행까지 이어가는 AI</p>
  </section>

  <section class="compare-block">
    <div class="compare-column">
      <p class="compare-name">Chatbot</p>
      <p>질문 → 답변</p>
      <p>한 번의 응답 중심</p>
      <p>설명에 강함</p>
    </div>
    <div class="compare-column strong">
      <p class="compare-name">Agent</p>
      <p>목표 → 작업 수행</p>
      <p>여러 단계 연결</p>
      <p>행동에 강함</p>
    </div>
  </section>
</div>

<!--
에이전트 AI는 쉽게 말해서 질문에 답만 하는 AI가 아니라,
목표를 주면 그 목표를 해결하기 위해 여러 단계를 이어가는 AI입니다.
예를 들어 일반 챗봇은 개념 설명을 잘해주지만,
에이전트 AI는 자료 찾기, 정리하기, 초안 만들기 같은 작업 흐름까지 연결할 수 있습니다.
그래서 핵심은 planning, tool use, execution,
즉 계획하고, 필요한 도구를 쓰고, 실제로 실행하는 구조라고 볼 수 있습니다.
-->

---
class: agenda-slide
transition: slide-left
---

<div class="single-column">
  <p class="section-label">Why Now</p>
  <h1>왜 지금 중요할까?</h1>
  <p class="section-support">답변 품질 경쟁에서 작업 수행 능력 경쟁으로 넘어가는 중</p>

  <div class="topic-grid">
    <div>
      <p class="topic-name">검색</p>
      <p>웹 탐색과 정보 수집</p>
    </div>
    <div>
      <p class="topic-name">문서</p>
      <p>정리, 요약, 초안 작성</p>
    </div>
    <div>
      <p class="topic-name">코드</p>
      <p>작성, 수정, 자동화</p>
    </div>
    <div>
      <p class="topic-name">업무</p>
      <p>이메일, 일정, 반복 작업 보조</p>
    </div>
  </div>
</div>

<!--
에이전트 AI가 중요한 이유는,
이제 AI가 답변을 잘하는 수준을 넘어서 실제 작업을 연결해서 처리하는 방향으로 발전하고 있기 때문입니다.
예전에는 검색 따로, 정리 따로, 작성 따로였다면,
지금은 이런 단계를 하나의 흐름처럼 묶어서 처리하는 방식이 점점 중요해지고 있습니다.
그래서 에이전트 AI는 단순한 챗봇의 업그레이드라기보다,
업무 자동화 쪽으로 확장되는 흐름이라고 이해하는 게 더 맞다고 생각합니다.
-->

---
class: split-slide
transition: slide-left
---

<div class="split-layout">
  <section>
    <p class="section-label">Case Study</p>
    <h1>왜 OpenClaw인가?</h1>
    <ul class="plain-list">
      <li>오픈소스 기반의 개인형 에이전트 AI 플랫폼</li>
      <li>직접 운영하고 실험해볼 수 있는 구조</li>
      <li>채팅 요청을 행동으로 연결하는 흐름이 선명함</li>
    </ul>
  </section>

  <section class="quote-panel">
    <p class="pull-quote">중요한 건 AI가 무엇을 아는가보다,<br>AI가 무엇을 하게 되는가다.</p>
  </section>
</div>

<!--
OpenClaw를 가져온 이유는,
에이전트 AI가 실제로 어떤 모습으로 구현될 수 있는지 보여주기 좋기 때문입니다.
OpenClaw는 오픈소스 기반이라 구조를 직접 보고 이해할 수 있고,
개인이 실험해보기도 비교적 좋습니다.
중요한 건 AI가 단순히 답을 아는 데서 끝나는 게 아니라,
요청을 받고 필요한 기능을 사용해서 실제 행동으로 이어진다는 점입니다.
그래서 에이전트 AI의 사례로 설명하기에 적절합니다.
-->

---
class: architecture-slide
transition: slide-left
---

<div class="single-column">
  <p class="section-label">Architecture</p>
  <h1>OpenClaw의 구조</h1>

  <div class="flow-line">
    <div class="flow-stage">사용자 요청</div>
    <div class="flow-arrow">→</div>
    <div class="flow-stage emphasis">에이전트 판단</div>
    <div class="flow-arrow">→</div>
    <div class="flow-stage">행동 또는 응답</div>
  </div>

  <div class="flow-support">
    <div class="flow-support-item">
      <p class="topic-name">Tools</p>
      <p>실제 기능 호출</p>
    </div>
    <div class="flow-support-item">
      <p class="topic-name">Skills</p>
      <p>언제, 어떻게 행동할지에 대한 가이드</p>
    </div>
    <div class="flow-support-item">
      <p class="topic-name">Plugins</p>
      <p>외부 서비스와의 연결과 확장</p>
    </div>
  </div>
</div>

<!--
OpenClaw의 구조를 보면 에이전트 AI가 왜 단순 모델과 다른지 더 잘 보입니다.
Tools는 검색이나 실행 같은 실제 기능이고,
Skills는 어떤 상황에서 어떤 기능을 써야 하는지에 대한 행동 가이드입니다.
Plugins는 외부 서비스나 환경과 연결해주는 확장 요소입니다.
결국 에이전트 AI는 모델 하나가 똑똑한 것으로 끝나는 게 아니라,
생각하는 부분, 행동하는 도구, 연결 구조가 함께 있어야 제대로 작동한다는 걸 보여줍니다.
-->

---
class: split-slide
transition: slide-left
---

<div class="split-layout">
  <section>
    <p class="section-label">Risks</p>
    <h1>한계와 위험</h1>
    <ul class="plain-list">
      <li>Prompt Injection 같은 보안 위험</li>
      <li>AI에 과도한 권한을 줄 때의 문제</li>
      <li>로그, 메모리, 개인정보 노출 가능성</li>
    </ul>
  </section>

  <section>
    <p class="section-label">Takeaway</p>
    <ol class="takeaway-list">
      <li>에이전트 AI는 행동하는 AI다</li>
      <li>OpenClaw는 그 구조를 보여주는 사례다</li>
      <li>앞으로의 핵심은 성능과 안전한 통제다</li>
    </ol>
  </section>
</div>

<!--
물론 이런 시스템은 강력한 만큼 위험도 큽니다.
대표적으로 프롬프트 인젝션, 과도한 권한 부여,
그리고 로그나 메모리, 개인정보 노출 같은 문제가 있습니다.
일반 챗봇은 틀린 답을 하는 데서 끝날 수 있지만,
에이전트 AI는 경우에 따라 실제 행동까지 할 수 있기 때문입니다.
정리하자면 에이전트 AI는 대답하는 AI에서 행동하는 AI로 넘어가는 흐름이고,
OpenClaw는 그 흐름을 잘 보여주는 사례입니다.
앞으로 중요한 것은 AI가 무엇을 아느냐뿐 아니라,
무엇을 얼마나 안전하게 하게 둘 것인가라고 생각합니다.
감사합니다.
-->

---
class: thanks-slide
transition: fade
---

<div class="thanks-wrap">
  <p class="section-label">Closing</p>
  <h1>감사합니다.</h1>
</div>
