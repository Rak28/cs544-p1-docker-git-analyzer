# CS544 P1: Dockerized Git Analyzer

**Course:** CS544 — Big Data Systems, UW-Madison (Fall 2025)

## Overview

A Dockerized tool that clones a Git repository, extracts the diff between two branches, and summarizes the changes using a small LLM (Large Language Model).

## Learning Objectives

- Install and configure Docker on a Linux VM
- Write Dockerfiles to define custom Docker images
- Use shell redirection and piping to send data between files/processes
- Integrate an LLM for automated code summarization

## Tech Stack

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Shell](https://img.shields.io/badge/Shell-4EAA25?style=flat&logo=gnubash&logoColor=white)

## Project Structure

```
p1/
├── Dockerfile          # Container definition
├── analyzer.sh         # Shell script: clone, diff, summarize
├── summarize.py        # LLM-powered summarization
└── README.md
```

## How It Works

1. Clone a target Git repository inside the container
2. Extract the diff between two specified branches using `git diff`
3. Pipe the diff to a local LLM to generate a human-readable summary
4. Output the summary to stdout

## Usage

```bash
docker build -t git-analyzer .
docker run git-analyzer <repo_url> <branch1> <branch2>
```

## Author

**Rakshith Sriraman Krishnaraj** · MS CS @ UW-Madison · [LinkedIn](https://www.linkedin.com/in/rakshith-s-k-95b550151/)
