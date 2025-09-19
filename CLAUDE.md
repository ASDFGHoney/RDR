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