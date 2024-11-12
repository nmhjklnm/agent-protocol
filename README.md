# Agent Protocol

Agent Protocol is our attempt at codifying the framework-agnostic APIs that are needed to serve LLM agents in production. This documents explains the purpose of the protocol and makes the case for each of the endpoints in the spec. We finish by listing some roadmap items for the future.

LangGraph Platform implements a superset of this protocol, but we very much welcome other implementations from the community.

## Why Agent Protocol

What is the right API to serve an LLM application in production? We believe it’s centered around 3 important concepts:

- Runs: APIs for executing an agent
- Threads: APIs to organize multi-turn executions of agents
- Store: APIs to work with long-term memory

Let’s dive deeper into each one, starting with the requirements, and then presenting the Protocol endpoints that meet these requirements.

## Runs: Atomic agent executions

What do we need out of an API to execute an agent?

- Support the two paradigms for launching a run
  - fire and forget
  - waiting on a reply (blocking or polling)
- Support CRUD for agent executions
  - list and get runs
  - cancel and delete runs
- Flexible ways to consume output
  - streaming output (can reconnect on connection drop)
  - final state
  - token streaming
- Handling edge cases
  - Retry on failure
  - Bursty traffic is queued up

## Threads: multi-turn interactions

What APIs do you need to enable multi-turn interactions?

- Persistent state
  - get and update state
  - append-only log of states
  - optimized storage
- Support for concurrent inputs from user
  - Implement chatbots with more natural UX
  - Choose from 4 modes to handle this
- CRUD endpoints for threads
  - list threads by users
  - list threads that need attention (interrupted)
  - copy or delete threads

Endpoints:

- [`POST /threads`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/POST/threads) - Create a thread.
- [`POST /threads/search`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/POST/threads/search) - Search threads.
- [`GET /threads/{thread_id}`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/GET/threads/%7Bthread_id%7D) - Get a thread.
- [`GET /threads/{thread_id}/state`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/GET/threads/%7Bthread_id%7D/state) - Get the latest state of a thread.
- [`POST /threads/{thread_id}/state`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/POST/threads/%7Bthread_id%7D/state) - Create a new revision of the thread’s state.
- [`GET /threads/{thread_id}/history`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/GET/threads/%7Bthread_id%7D/history) - Browse past revisions of a thread’s state. Revisions are created by runs, or through the endpoint just above.
- [`POST /threads/{thread_id}/copy`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/POST/threads/%7Bthread_id%7D/copy) - Create an independent copy of a thread.
- [`DELETE /threads/{thread_id}`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/DELETE/threads/%7Bthread_id%7D) - Delete a thread.
- [`PATCH /threads/{thread_id}`](https://langchain-ai.github.io/agent-protocol/api.html#tag/threads/PATCH/threads/%7Bthread_id%7D) - Update the metadata for a thread.

## Store: Long-term memory

What do you need out of a memory API for agents?

- Customizable memory scopes
  - Storing memory against the user, thread, assistant, company, etc
  - Accessing memory from different scopes in the same run
    -

## Roadmap

- Add Store endpoint to perform a vector search over memory entries
- Add param for `POST /threads/{thread_id}/runs/{run_id}/stream` to replay events since `event-id` before streaming new events
- Add param to `POST /threads/{thread_id}/runs ` to optionally allow concurrent runs on the same thread (current spec makes this forbidden)
- (Open an issue and let us know what else should be here!)
