# RDR - Reflection-Driven Resume

*Read this in other languages: [English](README.md), [한국어](README.ko.md)*

> A reflection-driven approach to resume writing, inspired by spec-kit

## Overview

RDR (Reflection-Driven Resume) is a project designed to help you write resumes and portfolios through structured reflection and data organization. Instead of starting with a blank page, RDR guides you through collecting, organizing, and reflecting on your experiences to create authentic, tailored resumes.

## Problem Statement

- **Starting Challenge**: Writing a resume from scratch feels overwhelming
- **Stream of Consciousness**: Need a way to capture thoughts naturally and develop them systematically
- **Continuous Updates**: Want to easily update resumes after new projects
- **Company-Specific Tailoring**: Difficulty customizing resumes for different companies

## Core Philosophy

This project **never** writes your resume for you. Instead, it:
- Provides initial ideas and structure
- Offers advice on missing content
- Analyzes your writing style to provide guidance
- Suggests improvements based on your authentic experiences

## Folder Structure

### `MyBase/`
Raw, unprocessed data repository for all your activities:
- Team project chats
- Presentation slides
- Codebase snapshots
- Any relevant materials

**Sub-structure:**
- `MyBase/summary/`: Contains `[activity-name]-summary.md` files
- Summary files contain factual information only (no fabrication)
- Lists facts without summarization

### `Corporate_Analysis/`
Company research and analysis workspace:
- `Corporate_Analysis/[company-role]/base/`: Raw company data
- `[company-role]-summary.md`: Company culture and information analysis

### `Reflections/`
**Most Important Folder** - Your authentic reflection space:
- Write diary-style reflections on all your experiences
- Focus on problems you solved and mistakes you made
- General experiences are also valuable to include
- This content is the foundation of truth
- **Agents must never auto-generate content here**
- Used as the backbone for building resume content

### `Generated/`
Output folder for final documents:
- `Generated/resume/`: Company-specific resumes (`resume-[company]-[version].md`)
- `Generated/portfolio/`: Project portfolios (`[project]-portfolio-[version].md`)

## Planned Features

### Sub-Agents
1. **Resume Expert**: Reviews and advises on resume content
2. **Reflection Advisor**: Suggests reflection topics based on MyBase data
3. **Proofreader**: Checks for typos and grammar
4. **Chat Analyzer**: Analyzes communication data for insights

### Available Commands

#### `/init` - Project Initialization
**Korean Name**: RDR 초기화 명령어
**Purpose**: Creates the complete RDR folder structure and sets up git branching for personal data management.

**What it does**:
- Creates all required folders (`MyBase/`, `Corporate_Analysis/`, `Reflections/`, `Generated/`)
- Adds `.gitkeep` files to maintain empty directories
- Creates and switches to `personal` branch for private work
- Keeps `main` branch clean for project structure only

**Usage**: Simply run `/init` in Claude Code

---

#### `/mybase-summary` - Comprehensive Data Analysis
**Korean Name**: MyBase 종합 분석 및 요약 자동화
**Purpose**: Analyzes all MyBase data using parallel sub-agents and creates structured activity summaries.

**What it does**:
- Scans all files in MyBase folder and categorizes by project/activity
- Uses multiple specialized agents to analyze each project independently
- Extracts factual information: dates, roles, achievements, skills, collaborations
- Validates data consistency and identifies missing information
- Generates `[activity-name]-summary.md` files in `MyBase/summary/`

**Expected processing time**: 12-21 minutes depending on data volume
**Usage**: Request "MyBase 폴더의 모든 내용을 분석하고 활동별 요약 파일을 생성해주세요"

---

#### `/basecheckandtellmenew` - Update Detection & Reflection Planning
**Korean Name**: MyBase 업데이트 워크플로우
**Purpose**: Detects new additions to MyBase, updates summaries, and suggests immediate reflection opportunities.

**What it does**:
1. **Change Detection**: Analyzes recent git commits to identify new MyBase files
2. **Summary Updates**: Adds factual information from new files to existing summaries
3. **Reflection Analysis**: Determines if activities are ready for reflection or need to be postponed
4. **Question Generation**: Creates specific reflection questions for completed activities

**Usage**: "위의 MyBase 업데이트 워크플로우를 1단계부터 3단계까지 순서대로 실행해주세요"

---

#### `/letsreflection` - Chronological Reflection Question Generator
**Korean Name**: 시간 순서별 회고 질문 생성
**Purpose**: Generates systematic reflection questions based on chronological activity analysis with progress tracking.

**What it does**:
- Reads `reflection-tracker.md` to understand current reflection progress
- Analyzes all summary files in chronological order
- Generates targeted reflection questions by category:
  - `[기술성장]` Technical skill development
  - `[문제해결]` Problem-solving experiences
  - `[협업소통]` Collaboration and communication
  - `[가치관변화]` Value and perspective changes
  - `[미래연결]` Connections to future growth
- Updates reflection tracker with new questions and progress

**Features**:
- Avoids duplicate questions through historical tracking
- Prioritizes older unprocessed activities
- Creates meaningful, open-ended questions that encourage deep reflection
- Maintains systematic progress through your reflection journey

---

#### Additional Workflow Commands
The system also includes specialized workflow commands for:
- **Reflection tracking management**: Maintains systematic progress through reflection questions
- **Data validation**: Ensures accuracy and consistency of extracted information
- **Progress monitoring**: Tracks completion status of reflection activities

## Requirements

This project is designed to work specifically with **Claude Code** (claude.ai/code). Other AI assistants or IDEs are not supported.

## Getting Started

### Initial Setup
1. **Initialize Project**: Run `/init` command in Claude Code
   - Creates complete folder structure
   - Sets up `personal` branch for your private data
   - Adds necessary `.gitkeep` files

2. **Populate Data**: Add your raw project materials to `MyBase/`
   - Team project chats and communications
   - Presentation slides and documents
   - Code repositories and technical artifacts
   - Any materials related to your professional activities

### Data Processing Workflow
3. **Create Activity Summaries**: Use `/mybase-summary` command
   - Analyzes all MyBase files using AI agents
   - Generates factual summaries in `MyBase/summary/`
   - Takes 12-21 minutes depending on data volume
   - **Usage**: Request "MyBase 폴더의 모든 내용을 분석하고 활동별 요약 파일을 생성해주세요"

4. **Regular Updates**: Use `/basecheckandtellmenew` for ongoing maintenance
   - Detects new files added to MyBase
   - Updates existing summaries with new information
   - Suggests when activities are ready for reflection

### Reflection Process
5. **Generate Reflection Questions**: Use `/letsreflection` command
   - Creates chronological reflection questions
   - Categorizes questions by growth areas
   - Tracks your progress through systematic reflection

6. **Write Authentic Reflections**: Manually write in `Reflections/` folder
   - Use generated questions as prompts
   - Focus on problems solved and lessons learned
   - Include mistakes and growth experiences
   - **Important**: This content is never auto-generated - it must be your authentic voice

### Resume Development
7. **Use commands and agents** to develop your resume content based on your reflections
   - Summaries provide factual foundation
   - Reflections provide authentic insights and storytelling
   - Generated questions help ensure comprehensive coverage

## Command Workflow

The RDR commands are designed to work together in a systematic workflow that supports continuous reflection and resume development:

### Initial Project Setup
```
/init → Creates folder structure and personal branch
```

### First-Time Data Analysis
```
Add data to MyBase/ → /mybase-summary → Review generated summaries
```
**Timeline**: Allow 12-21 minutes for comprehensive analysis

### Ongoing Reflection Cycle
```
New activities → /basecheckandtellmenew → Updated summaries + reflection readiness
                     ↓
                /letsreflection → Generated reflection questions
                     ↓
             Manual reflection writing → Authentic insights in Reflections/
                     ↓
              Resume/portfolio development
```

### Typical Weekly Workflow
1. **Monday**: Run `/basecheckandtellmenew` to catch up on recent activity data
2. **Wednesday**: Use `/letsreflection` to generate new questions for completed activities
3. **Friday**: Spend 30-60 minutes writing authentic reflections using generated questions
4. **As needed**: Update resumes/portfolios using reflection insights

### Progress Tracking Features
- **Reflection Tracker**: `reflections/reflection-tracker.md` maintains systematic progress
- **Question History**: Prevents duplicate questions and tracks completion
- **Activity Timeline**: Chronological organization ensures comprehensive coverage
- **Postponed Activities**: Tracks in-progress projects until completion

### Integration Points
- **MyBase** → **Summary** (factual foundation)
- **Summary** → **Questions** (targeted reflection prompts)
- **Questions** → **Reflections** (authentic insights)
- **Reflections** → **Resumes** (compelling narratives)

This systematic approach ensures that no experiences are overlooked and that your professional development is thoroughly documented and reflected upon.

## Development Approach

This project follows an iterative development approach:
- Commands and sub-agents will be refined through actual usage
- The focus is on supporting authentic reflection and content development
- Tools are designed to enhance, not replace, your genuine experiences
