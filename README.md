# my-first-agent

A private practice repository for learning how to build an AI agent.

This is a personal learning project. It is not connected to any employer,
company, or real project.

## What this project will be

A small **ticket-review agent** that works only on **fictional tickets** in a
**toy project** that lives inside this repository.

- **First version:** the agent reads one sample ticket and writes a
  *review plan*: what the ticket asks for, what is unclear, and what should
  be checked before the work counts as done.
- **Later versions:** the agent may also look at a small toy code change and
  run a test to see whether the change does what the ticket asks.

## Safety boundaries

This agent is for practice only. It must **not**:

- connect to real ticket systems (such as Jira, GitHub Issues, or Linear),
- read from or write to real work projects or repositories,
- make external changes of any kind (no sending messages, no pushing code,
  no calling outside services on its own).

Everything the agent reads and does stays inside this repository and uses
made-up data.

## Beginner concepts

### What is an agent?

A normal chatbot answers one message and stops. An **agent** is a program
built around an AI model that works toward a goal in steps. It can:

1. read its instructions and the task,
2. decide what to do next,
3. take an action,
4. look at the result, and
5. repeat until the goal is reached or it decides to stop.

This "think → act → check" cycle is often called the **agent loop**.

### What are "tools"?

On its own, an AI model can only read text and write text. **Tools** are
small, well-defined functions that the program gives the model so it can do
specific things, for example:

- `read_ticket`: open a sample ticket file and return its text,
- `read_file`: show the contents of a file in the toy project,
- `run_tests`: run the toy project's tests and report the results.

The model doesn't run these functions itself. It asks for a tool by name, the
program runs the tool, and the program sends the result back to the model.
Because you choose which tools to provide, tools also set the agent's limits:
an agent with no tool for contacting real systems can't contact them.

## Learning roadmap

1. **Instructions:** write clear instructions that describe the agent's role,
   goal, and safety boundaries.
2. **Sample ticket:** add one fictional ticket and have the agent turn it into
   a review plan.
3. **Tool use:** give the agent a few simple, local tools (such as reading a
   ticket or a file) and watch how it decides when to use them.
4. **Testing:** add a tiny toy code change and a test, let the agent run the
   test, and check that its review matches the result.

## Status

Just started. There is no code yet, only this README.
