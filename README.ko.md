<p align="center">
  <a href="README.md">English</a> | 한국어
</p>

# Learning Lab

코드 기반 기술을 실제 결과물부터 만들며 배우는 Codex·Claude Code 플러그인 마켓플레이스입니다.

현재 포함된 플러그인:

- **Learn Like Gabriel Petersson** — 실제 문제 → 작동하는 결과물 → 지식 공백 발견 → 재귀 질문 → 자기 설명 → 검증 순서로 프로그래밍·AI를 학습합니다.

> Gabriel Petersson의 공개 학습 방식에서 영감을 받은 비공식 프로젝트입니다. Gabriel Petersson과 공식 제휴하거나 승인받은 제품이 아닙니다.

## 설치

### Codex CLI

터미널에서 마켓플레이스와 플러그인을 차례로 설치합니다.

```bash
codex plugin marketplace add sdhong0609/learning-lab
codex plugin add learn-like-gabriel-petersson@learning-lab
```

설치 후 새 Codex 세션을 시작하면 플러그인을 사용할 수 있습니다.

대화형으로 설치하려면 `codex`를 실행한 뒤 `/plugins`를 입력하고, `Learning Lab`에서 `Learn Like Gabriel Petersson`을 선택합니다.

### ChatGPT 데스크톱 앱

먼저 터미널에서 마켓플레이스를 추가합니다.

```bash
codex plugin marketplace add sdhong0609/learning-lab
```

그다음 Plugins Directory에서 `Learning Lab`을 선택하고 `Learn Like Gabriel Petersson`을 설치합니다. 설치 후 새 채팅을 시작합니다.

### Claude Code

터미널에서 마켓플레이스와 플러그인을 차례로 설치합니다.

```bash
claude plugin marketplace add sdhong0609/learning-lab
claude plugin install learn-like-gabriel-petersson@learning-lab
```

Claude Code 세션 안에서 `/plugin marketplace add sdhong0609/learning-lab` 후 `/plugin install learn-like-gabriel-petersson@learning-lab`를 실행해도 됩니다.

설치 후 새 Claude Code 세션을 시작합니다. 학습 요청 시 스킬이 자동으로 실행되며, `/learn-like-gabriel-petersson:learn-like-gabriel-petersson`로 직접 호출할 수도 있습니다.

## 사용 예시

- “작은 자동화 도구를 만들면서 Python을 배우고 싶어.”
- “작동하는 추천 모델을 먼저 만든 뒤 구조를 이해하고 싶어.”
- “웹 API를 직접 만들면서 서버 개발을 배우고 싶어.”

플러그인은 먼저 최소 작동 결과물을 만듭니다. 이후 사용자가 모르는 부분을 하나씩 파고들고, 자기 설명을 받아 오류와 누락을 검증합니다.

## 구조

```text
learning-lab/
├── .agents/plugins/marketplace.json
├── .claude-plugin/marketplace.json
└── plugins/
    └── learn-like-gabriel-petersson/
        ├── plugin.json
        ├── .codex-plugin/plugin.json
        ├── .claude-plugin/plugin.json
        └── skills/
```

## 상태

- 버전: `0.1.0`
- 유형: Skills-only plugin
- 공개 범위: GitHub 기반 마켓플레이스
- OpenAI 공식 Plugins Directory 등록: 아직 제출하지 않음
