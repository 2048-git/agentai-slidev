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
    <div class="agent-strip" aria-hidden="true">
      <div class="agent-chip">
        <img class="agent-chip-icon" src="./anthropic-official.png" alt="" />
        <span>Claude Code</span>
      </div>
      <div class="agent-chip">
        <img class="agent-chip-icon" src="./openai-knot-official.svg" alt="" />
        <span>Codex</span>
      </div>
      <div class="agent-chip">
        <img class="agent-chip-icon" src="./gemini-official.svg" alt="" />
        <span>Gemini</span>
      </div>
    </div>
    <p class="cover-credit">소프트웨어학부 22학번 강지웅</p>
  </div>

  <div class="cover-visual cover-visual-image" aria-hidden="true">
    <img class="cover-og-image" src="./openclaw-og-official.png" alt="" />
  </div>
</div>

<!--
안녕하세요, 소프트웨어학부 22학번 강지웅입니다.
오늘 저는 에이전트 AI와 오픈클로에 대해 발표하겠습니다.
요즘 AI라고 하면 단순히 답만 해주는 챗봇보다,
우리가 흔히 쓰는 클로드 코드나 코덱스 같은 코딩 에이전트처럼 실제 작업을 수행해 주는 AI를 먼저 떠올리실 겁니다.
오늘 발표에서는 이 흐름을 아우르는 에이전트 AI의 개념과,
이를 아주 직관적으로 보여주는 오픈클로 사례를 간단히 살펴보겠습니다.
-->

---
class: split-slide
transition: slide-left
---

<div class="split-layout openclaw-intro-layout">
  <section class="openclaw-intro-panel">
    <h1>에이전트 AI란?</h1>
    <p class="lead-kicker">목표를 받으면</p>
    <p class="lead-flow">계획 → 도구 사용 → 실행</p>
  </section>

  <section class="compare-block">
    <div class="compare-column">
      <p class="compare-name">기본 챗봇</p>
      <p>질문 → 답변</p>
      <p>한 번의 응답 중심</p>
      <p>설명에 강함</p>
    </div>
    <div class="compare-column strong">
      <p class="compare-name">에이전트형 AI</p>
      <p>목표 → 작업 수행</p>
      <p>여러 단계 연결</p>
      <p>행동에 강함</p>
    </div>
  </section>
</div>

<!--
에이전트 AI는 쉽게 말해 질문에 답만 하는 AI가 아니라,
목표를 주면 그걸 해결하기 위해 여러 단계를 스스로 밟아가는 AI입니다.
예를 들어 일반 챗봇은 어떤 개념을 설명하는 데 그치지만,
에이전트 AI는 스스로 웹에서 자료를 찾고, 정리해서, 초안 문서를 만드는 전체 작업 흐름을 연결할 수 있습니다.
즉, 스스로 계획을 세우고, 필요한 도구를 꺼내 쓰고, 실제로 실행하는 구조가 핵심입니다.
-->

---
class: example-slide
transition: slide-left
---

<div class="single-column example-wrap">
  <h1>여러 단계가 연결되는 요청</h1>
  <p class="section-support">검색, 파일 작성, 결과 정리까지 이어지는 작업</p>

  <div class="request-card">
    <p class="request-label">예시 요청</p>
    <p class="request-text">"OpenClaw 공식 자료를 찾아 핵심 기능을 정리하고, 발표 초안 파일로 만들어줘"</p>
  </div>

  <div class="example-flow">
    <div class="example-step">
      <p class="example-step-num">1</p>
      <p class="example-step-title">요청 이해</p>
      <p class="example-step-body">무엇을 찾고 어떤 형식으로 정리할지 판단</p>
    </div>
    <div class="example-step">
      <p class="example-step-num">2</p>
      <p class="example-step-title">자료 탐색</p>
      <p class="example-step-body">관련 문서와 정보를 수집</p>
    </div>
    <div class="example-step">
      <p class="example-step-num">3</p>
      <p class="example-step-title">정보 선별</p>
      <p class="example-step-body">핵심 기능만 골라 발표용으로 정리</p>
    </div>
    <div class="example-step">
      <p class="example-step-num">4</p>
      <p class="example-step-title">파일 작성</p>
      <p class="example-step-body">초안 문서나 메모 파일 생성</p>
    </div>
    <div class="example-step">
      <p class="example-step-num">5</p>
      <p class="example-step-title">결과 반환</p>
      <p class="example-step-body">완성된 결과와 파일 위치 전달</p>
    </div>
  </div>
</div>

<!--
예를 들어 사용자가 오픈클로 공식 자료를 찾고,
핵심 기능을 정리해서 발표 초안 파일까지 만들어달라고 요청했다고 해보겠습니다.
이 경우에는 단순히 설명하는 것보다,
먼저 필요한 자료를 찾고, 내용을 선별하고, 정리한 뒤,
그 결과를 실제 파일 형태로 남기는 과정까지 이어져야 합니다.
즉 에이전트형 AI의 핵심은 답변 자체보다,
목표를 해결하기 위해 여러 단계의 행동을 끝까지 연결하는 데 있습니다.
-->

---
class: agenda-slide
transition: slide-left
---

<div class="single-column">
  <h1>왜 지금 중요할까?</h1>
  <p class="section-support">답변 품질 경쟁에서 작업 수행 능력 경쟁으로 넘어가는 중</p>

  <div class="topic-grid">
    <div class="topic-card">
      <p class="topic-name">검색</p>
      <p>웹 탐색과 정보 수집</p>
    </div>
    <div class="topic-card">
      <p class="topic-name">문서</p>
      <p>정리, 요약, 초안 작성</p>
    </div>
    <div class="topic-card">
      <p class="topic-name">코드</p>
      <p>작성, 수정, 자동화</p>
    </div>
    <div class="topic-card">
      <p class="topic-name">업무</p>
      <p>이메일, 일정, 반복 작업 보조</p>
    </div>
  </div>
</div>

<!--
이 에이전트 AI가 중요한 이유는,
AI의 발전 방향이 답변의 질을 넘어서 실제 작업의 연결과 자동화로 넘어가고 있기 때문입니다.
예전에는 검색 따로, 문서 요약 따로, 작성 따로였다면,
지금은 이 단계들을 하나의 파이프라인처럼 묶어서 처리하는 게 트렌드가 되었습니다.
그래서 에이전트 AI는 단순한 챗봇의 업그레이드가 아니라,
소프트웨어 업무 자동화의 넥스트 스텝이라고 보는 게 맞습니다.
-->

---
class: split-slide
transition: slide-left
---

<div class="split-layout">
  <section>
    <div class="openclaw-intro-mark">
      <img class="openclaw-intro-icon" src="./openclaw.png" alt="" />
      <span class="openclaw-intro-label">OpenClaw</span>
    </div>
    <h1>OpenClaw란?</h1>
    <ul class="plain-list openclaw-list">
      <li>Peter Steinberger와 커뮤니티가 만든 오픈소스 개인형 AI 비서</li>
      <li>개발자와 파워 유저가 직접 운영하고 실험하기 좋은 구조</li>
      <li>메신저 기반으로 검색, 일정, 이메일, 코딩 작업까지 연결 가능</li>
    </ul>
  </section>

  <section class="media-panel openclaw-demo-panel">
    <img class="official-demo-image" src="./openclaw-whatsapp-official.jpg" alt="OpenClaw 공식 데모 이미지" />
    <p class="image-caption">OpenClaw 공식 데모 이미지</p>
  </section>
</div>

<!--
에이전트 AI 사례 중 오픈클로를 간단히 소개해드리겠습니다.
오픈클로는 피터 슈타인베르거와 커뮤니티가 만든 오픈소스 개인형 AI 비서입니다.
주로 개발자나 파워 유저처럼 자기 환경을 직접 통제하고 싶은 사람들을 위한 도구라고 볼 수 있습니다.
왓츠앱이나 디스코드 같은 메신저에서 요청을 보내면,
자료 탐색, 일정 관리, 이메일 처리, 코딩 작업 같은 일을 연결해서 수행할 수 있습니다.
또 셀프호스팅이 가능하고 자유도가 높아서 빠르게 화제가 되었고,
어제 봤을 때 깃허브 저장소도 약 34만 스타를 기록하고 있었습니다.
-->

---
class: architecture-slide
transition: slide-left
---

<div class="single-column architecture-wrap">
  <h1 class="architecture-title"><span class="architecture-brand">OpenClaw</span>의 핵심 아키텍처</h1>
  <p class="architecture-flow">사용자 요청 → 에이전트 판단 → 행동 또는 응답</p>
  <div class="architecture-grid">
    <div class="architecture-card">
      <div class="architecture-icon">T</div>
      <p class="architecture-card-title">도구 (Tools)</p>
      <p class="architecture-card-body">웹 브라우저 제어, 터미널 명령 실행, API 호출 등 에이전트가 외부 시스템과 직접 상호작용하는 실제 기능 모음입니다.</p>
    </div>
    <div class="architecture-card">
      <div class="architecture-icon">S</div>
      <p class="architecture-card-title">스킬 (Skills)</p>
      <p class="architecture-card-body">특정 상황에서 어떤 도구를 어떻게 조합해 써야 하는지 AI에게 알려주는 핵심 행동 가이드라인입니다.</p>
    </div>
    <div class="architecture-card">
      <div class="architecture-icon">P</div>
      <p class="architecture-card-title">플러그인 (Plugins)</p>
      <p class="architecture-card-body">메시지 연동이나 외부 서비스 연결처럼 에이전트의 활용 범위를 바깥으로 확장해 주는 연결 계층입니다.</p>
    </div>
  </div>
</div>

<!--
오픈클로의 내부를 보면 에이전트 AI가 왜 단순 모델과 다른지 더 명확해집니다.
이 시스템은 크게 도구, 스킬, 플러그인으로 구성되어 있습니다.
생각만 하는 언어 모델 하나로는 부족하기 때문에 행동을 위한 부품들이 필요한 거죠.
도구는 검색이나 터미널 실행 같은 실제 기능이고,
스킬은 어떤 상황에 어떤 도구를 써야 하는지 알려주는 가이드라인입니다.
그리고 플러그인은 외부 서비스와 연결해 주는 역할입니다.
결국 에이전트 AI는 생각하는 뇌, 행동하는 도구, 그리고 이 둘을 연결하는 구조가 합쳐져야 제대로 작동한다는 걸 알 수 있습니다.
-->

---
class: risk-slide
transition: slide-left
---

<div class="single-column risk-wrap">
  <h1>한계와 위험</h1>
  <div class="risk-grid">
    <div class="risk-item">
      <p class="risk-name">프롬프트 인젝션</p>
      <p>외부 입력이 지시를 오염시키는 공격</p>
    </div>
    <div class="risk-item">
      <p class="risk-name">과도한 권한</p>
      <p>잘못된 행동이 실제 실행으로 이어질 수 있음</p>
    </div>
    <div class="risk-item">
      <p class="risk-name">정보 노출</p>
      <p>로그, 메모리, 개인정보가 남거나 새어 나갈 수 있음</p>
    </div>
  </div>
</div>

<!--
물론 이런 시스템은 강력한 만큼 위험도 큽니다.
대표적으로 프롬프트 인젝션 공격, 에이전트에게 과도한 권한이 부여됐을 때의 위험,
그리고 로컬 메모리나 로그가 노출되는 보안 문제가 있습니다.
일반 챗봇은 틀린 답을 하는 데서 끝나지만,
에이전트 AI는 엉뚱한 파일을 지우거나 중요한 시스템을 건드리는 실제 행동을 할 수 있기 때문입니다.
-->

---
class: summary-slide
transition: fade
---

<div class="single-column summary-wrap">
  <h1>핵심 정리</h1>
  <ol class="summary-points">
    <li><span>에이전트 AI는 행동하는 AI다</span></li>
    <li><span>OpenClaw는 그 구조를 보여주는 사례다</span></li>
    <li><span>앞으로의 핵심은 성능과 안전한 통제다</span></li>
  </ol>
</div>

<!--
정리하자면, 에이전트 AI는 대답하는 AI에서 행동하는 AI로 넘어가는 거대한 흐름입니다.
앞으로 우리가 고민해야 할 것은 AI가 얼마나 똑똑한가를 넘어서,
AI에게 어떤 권한을, 얼마나 안전하게 쥐여줄 것인가라고 생각합니다.
-->

---
class: thanks-slide
transition: fade
---

<div class="thanks-wrap">
  <h1>감사합니다.</h1>
</div>

<!--
발표 들어주셔서 감사합니다.
-->

---
class: thanks-slide
transition: fade
---

<div class="thanks-wrap">
  <h1>Q&amp;A</h1>
</div>
