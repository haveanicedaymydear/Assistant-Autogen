# Assistant-Autogen

A personal multi-agent document automation project built to explore how LLM agents can collaborate in a structured, cloud-based pipeline.

## Overview

This repository studies how a multi-agent architecture can be used to generate, validate, refine, and export complex long-form documents in an automated workflow.

Rather than relying on a single prompting step, this project uses multiple specialised agents with different responsibilities, coordinated through an orchestration layer.  
The full pipeline is designed around cloud storage, parallel processing, iterative correction, and structured output generation.

## Core Idea

The project follows a staged workflow:

1. preprocess source documents
2. assign section-level generation tasks
3. validate each section with dedicated review agents
4. apply correction loops when issues are detected
5. merge validated outputs
6. export the final result into a structured Word document

This makes the system more reliable and traceable than a one-shot document generation approach.

## Key Features

- multi-agent architecture with specialised agent roles
- cloud-based document pipeline using Azure Blob Storage
- concurrent section generation and validation
- iterative write-validate-refine loop
- versioned intermediate outputs for traceability
- structured export to `.docx`
- configuration-driven workflow
- modular instruction files for reusable agent guidance
- logging and archived run records
- container-ready deployment workflow

## Why This Project Matters

This project demonstrates my interest in:

- LLM orchestration beyond simple chat interfaces
- multi-agent collaboration design
- workflow reliability and fault tolerance
- cloud-native AI system architecture
- automated document generation with structured outputs

It is especially relevant for real-world use cases where quality control, traceability, and repeatability matter.

## Agent Structure

### Writer Team
Responsible for drafting and revising section content.

### Validator Team
Responsible for reviewing structure, factual consistency, and rule compliance.

### Orchestration Layer
Coordinates task flow, retries, correction loops, output merging, and logging.

## Tech Stack

- Python
- AutoGen
- Azure Blob Storage
- Azure OpenAI
- asyncio
- Docker
- docxtpl

## Project Structure

```text
documentation/
instructions/
logs/
outputs/
src/
templates/
.env.example
Dockerfile
requirements.txt
