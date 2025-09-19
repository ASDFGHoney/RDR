# RDR - Reflection-Driven Resume

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

### `reflections/`
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

### Commands
1. `/mybase-summary`: Organize MyBase data into summaries
2. `/init`: Create the folder structure
3. More commands to be developed during usage

## Requirements

This project is designed to work specifically with **Claude Code** (claude.ai/code). Other AI assistants or IDEs are not supported.

## Getting Started

1. Run `/init` to create the folder structure
2. Populate `MyBase/` with your raw project data
3. Write authentic reflections in `reflections/`
4. Use commands and agents to develop your resume content

## Development Approach

This project follows an iterative development approach:
- Commands and sub-agents will be refined through actual usage
- The focus is on supporting authentic reflection and content development
- Tools are designed to enhance, not replace, your genuine experiences
