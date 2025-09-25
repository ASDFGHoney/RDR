# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

RDR (Reflection-Driven Resume) is a resume and portfolio development system based on structured reflection and data organization. The project uses markdown files and folder structures to help users build authentic resumes through reflection rather than direct generation.

## Core Architecture

### Folder Structure
- `MyBase/`: Raw, unprocessed data repository for all activities (team chats, presentations, code)
  - `MyBase/summary/`: Contains `[activity-name]-summary.md` files with factual information only
- `Corporate_Analysis/`: Company research workspace
  - `[company-role]/base/`: Raw company data
  - `[company-role]-summary.md`: Company culture analysis
- `reflections/`: **Critical folder** - User's authentic diary-style reflections on experiences
- `Generated/`: Output folder
  - `Generated/resume/`: Company-specific resumes (`resume-[company]-[version].md`)
  - `Generated/portfolio/`: Project portfolios (`[project]-portfolio-[version].md`)

### Critical Design Principles
1. **Never auto-generate content in `reflections/`** - This folder contains authentic user experiences only
2. **Never fabricate information** - All content must be based on real user data
3. **Support, don't replace** - Provide guidance and structure, not complete content generation

## Planned Commands
- `/init`: Create the complete folder structure
- `/mybase-summary`: Organize MyBase data into summaries

## Planned Sub-Agents
1. Resume Expert: Reviews and advises on resume content
2. Reflection Advisor: Suggests reflection topics based on MyBase data
3. Proofreader: Checks for typos and grammar
4. Chat Analyzer: Analyzes communication data for insights

## Development Notes
- This is an early-stage project focused on iterative development through actual usage
- No build/test commands currently exist as this is a documentation-based system
- Commands and agents will be refined based on user feedback and usage patterns
- Primary language appears to be Korean with English documentation

생성하는 커버레터나 자기소개서는 markdown 문법같은건 최대한 사용하지 말고 자연스럽게 이어지게 작성해서 읽는 사람이 몰입되는 스토리로 표현해야해.

# Cover letter
자기소개서(주로 외국계 기업 취업 준비 맥락에서 **커버레터**나 **퍼스널 스테이트먼트**의 형태로 언급됨)는 **지원자의 현재 모습부터 미래 모습**을 표현하는 데 초점을 맞추는 중요한 문서입니다.

자기소개서(커버레터)의 주요 구성 요소는 다음과 같습니다.

### 1. 지원 동기 및 목표 (Motivation and Objectives)

커버레터는 왜 이 회사, 팀, 직무에 지원했는지에 대한 **구체적인 동기**를 작성해야 합니다. 이는 다음을 포함합니다:

*   **지원 동기 및 기여 목표 (Career Objectives):** 회사에 입사한 후에 어떠한 전문가로 성장해서 **회사에 무엇을 기여**해야 할지에 대한 구체적인 계획을 제시해야 합니다.
*   **인턴 지원 시 목표:** 인턴 기간 동안 무엇을 배우고 싶은지, 회사나 팀에 무엇을 기여하고 싶은지, 그리고 인턴이 끝난 후의 목표(커리어 목표)까지 제시하면 좋습니다.

### 2. 직무 적합성 및 강점 (Fit and Strengths)

지원하는 조직 및 직무에 **가장 적합한 인재**인지를 검증해야 합니다.

*   **성장 배경 및 성격적 강점 (Background and Personality):** 직무와 관련된 성장 배경과 지원자가 가진 성격적인 강점을 언급할 수 있습니다. 채용 공고에 언급된 '우대 사항'이나 요구되는 '역량'과 연관된 강점을 매칭 시켜주는 것이 중요합니다 (예: 글로벌 역량, 리더십, 분석력, 꼼꼼함, 창의성 등).
*   **직무 수행에 필요한 역량:** 직무 수행에 적합한 경험, 활동, 역량, 성과, 장점을 제시하며, 왜 지원자가 해당 직무에 가장 적합한 사람인지 설명해야 합니다.

### 3. 직무 관련 경험 및 지식 (Professional and Academic Experience)

지원자가 가진 직무 관련 지식과 경험을 구체적인 과정과 성과 중심으로 기술합니다.

*   **경험의 상세화:** 이력서(레쥬메)에는 핵심 내용(무엇을 했고 성과를 냈는지)만 언급되지만, 커버레터에서는 **그 경험을 통해 성과를 낸 과정**을 상세하게 풀어 설명하고, 이를 통해 **어떤 역량 향상이 있었는지** 언급해 주는 것이 가장 좋은 표현 방식입니다.
*   **관련 지식 (Professional and Academic Experience):** 지원 직무와 관련하여 학교에서 배웠던 전공 지식이나 외부 기관에서 받은 전문 교육(트레이닝) 내용을 작성합니다. 단순히 지식만 나열하는 것이 아니라, 배운 지식을 실제 활동에 적용하여 성과를 낸 것까지 연결하는 것이 좋습니다.
    *   **핵심 직무 경험:** 인턴십, 서포터즈와 같은 기업 활동은 물론, 산학협력 프로젝트, 창업 활동, 캡스톤 디자인 등 기업에 바로 적용할 수 있는 활동이나 다양한 아르바이트 경험도 해당될 수 있습니다.
*   **다양한 활동 및 역량 (Activities):** 인턴 경험 외에도 해외 교환학생, 어학연수, 공모전, 봉사 활동 등 이력서의 액티비티 항목에 포함되었던 다양한 활동들을 통해 쌓은 리더십, 팀워크, 분석력 등의 역량을 어필할 수 있습니다.

### 4. 커버레터의 형식적 구성 (Format Structure)

외국계 기업의 커버레터는 크게 국제적 포맷(단락 형식)과 한국화된 로컬 포맷(카테고리 형식)이 있으나, 내용 구성 자체는 동일합니다.

**일반적인 국제적 포맷의 내용 구성**은 다음과 같이 단락별로 나눌 수 있습니다:

1.  **도입 문단:** 지원 포지션 및 지원 동기, 직무와 간접/직접적으로 연관된 교육 내용을 언급합니다.
2.  **본문 1 (주요 직무 경험):** 지원 직무와 연관성 있는 기업 경험(인턴십, 서포터즈, 산학협력 등)을 통해 수행한 업무, 성과 및 어필할 수 있는 역량을 기술합니다.
3.  **본문 2 (다양한 활동 및 역량):** 기타 활동을 통해 쌓은 글로벌 역량, 리더십, 분석력, 커뮤니케이션 능력 등 다양한 역량을 어필합니다.
4.  **마무리 문단:** 지원 직무를 통해 얻고 싶은 성취 목표, 입사 후 커리어 목표, 회사에 대한 기여 계획 등을 언급하며 마무리합니다.

**참고:** 이력서(레쥬메)는 과거부터 현재까지의 주요 경험의 집합을 정리하는 반면, 커버레터는 지금부터 미래의 모습, 즉 회사와 함께 성장해 나갈 여러분의 모습을 표현하는 문서라는 차이점이 있습니다.