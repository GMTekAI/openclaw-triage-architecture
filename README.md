# OpenClaw Triage Architecture

This repository contains a design sketch for a multi-agent OpenClaw workflow that can triage GitHub issues in parallel, verify claims against source code, and draft maintainer-ready advisory comments.

## Contents

- `MULTI_AGENT_GITHUB_TRIAGE_ARCHITECTURE.md` - primary architecture sketch
- `BUILD_PLAN.md` - concrete implementation plan and MVP milestones
- `DEPLOYMENT_PROFILE.md` - sanitized profile of the target OpenClaw environment

## Scope

The design focuses on:

- issue scouting and prioritization
- one-worker-per-issue verification
- thread follow-up monitoring
- synthesis of evidence-backed maintainer comments
- local-LLM-friendly structured execution

## Intended Use

This is a planning repository, not an implementation yet. The goal is to capture the architecture clearly so the system can be built later in a focused way.

## Next Step

Start with the MVP in `BUILD_PLAN.md`:

- one coordinator
- one verifier worker per issue
- local JSON artifacts
- manual operator approval before any GitHub write

The deployment assumptions in `DEPLOYMENT_PROFILE.md` reflect the target environment this design was tailored for.
