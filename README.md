# OpenClaw Triage Architecture

This repository contains a design sketch for a multi-agent OpenClaw workflow that can triage GitHub issues in parallel, verify claims against source code, and draft maintainer-ready advisory comments.

## Contents

- `MULTI_AGENT_GITHUB_TRIAGE_ARCHITECTURE.md` - primary architecture sketch

## Scope

The design focuses on:

- issue scouting and prioritization
- one-worker-per-issue verification
- thread follow-up monitoring
- synthesis of evidence-backed maintainer comments
- local-LLM-friendly structured execution

## Intended Use

This is a planning repository, not an implementation yet. The goal is to capture the architecture clearly so the system can be built later in a focused way.
