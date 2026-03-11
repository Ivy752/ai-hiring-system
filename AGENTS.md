74261"}
# AI Hiring System

This repository contains the implementation of an AI-powered recruiting platform with autonomous hiring agents.

The goal is to build a system that can:

- search candidates
- rank candidates
- generate outreach messages
- manage recruiting pipeline
- assist recruiters with hiring decisions

The system should follow clean architecture and modular design.

---

# System Architecture

Frontend:
Next.js (TypeScript)

Backend:
Python FastAPI

AI Layer:
LLM + embeddings + ranking

Databases:

Postgres (structured data)
Vector DB (semantic search)
Neo4j (talent graph)

---

# Repository Structure

frontend/
Next.js recruiter interface

backend/
FastAPI services

agents/
AI agents for recruiting workflow

ai/
embedding generation
ranking
LLM integrations

talent_graph/
graph schema
candidate relations

data_pipeline/
candidate ingestion pipeline

infra/
deployment scripts

docs/
documentation

---

# Key Product Features

Natural language talent search

Example:

"Find senior LLM engineers who worked on distributed systems at AI startups"

The system should:

1 parse the job description
2 extract skills and signals
3 search candidates using vector search
4 rank candidates
5 generate outreach messages

---

# Candidate Data Model

Candidate

id
name
title
company
location
skills
experience
linkedin
github
summary
embedding

---

# Agent System

The system contains multiple agents.

RoleUnderstandingAgent

Understands job descriptions and extracts requirements.

SourcingAgent

Searches candidates using semantic search and talent graph.

EvaluationAgent

Scores and ranks candidates.

OutreachAgent

Generates personalized outreach messages.

PipelineAgent

Tracks candidate stages in the hiring process.

---

# Agent Loop

Agents should follow this loop:

observe
plan
act
reflect

Example:

Goal: hire ML infrastructure engineer

observe job description

plan search strategy

act by searching candidates

reflect by evaluating results

---

# APIs

POST /search

Input

{
 "query": "LLM infrastructure engineer from top AI labs"
}

Output

candidate list


GET /candidate/{id}

Returns candidate profile


POST /agent/start

Starts recruiting agent for a role


POST /outreach/send

Sends outreach messages

---

# Development Phases

Phase 1

Basic backend
candidate schema
search API

Phase 2

embedding pipeline
semantic search

Phase 3

recruiting agents

Phase 4

outreach automation

Phase 5

frontend recruiter dashboard

---

# Coding Standards

Backend

Python
FastAPI
Pydantic
service layer architecture

Frontend

Next.js
TypeScript
component based architecture

---

# Output Expectations

When generating code, ensure:

clear folder structure
modular services
readable code
basic docume
