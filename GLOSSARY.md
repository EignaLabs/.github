# EignaLabs organization

This context holds the terms that the organization page and the shared contributor rules use. All EignaLabs repositories use these terms.

## Product

**Eigna**:
Owned AI for companies. Each company gets its own model and keeps control of its data and of where the model runs.
_Avoid_: the platform, the assistant

**Eigna Local**:
The Eigna offer that runs on the company's own machine, in its own building.

**Eigna Hybrid**:
The Eigna offer that runs sensitive work on site and heavy work in the company's region.

**Eigna Cloud**:
The Eigna offer that runs on a dedicated GPU in the region that the company selects.

**Adapter**:
The part of a model that belongs to one company. Eigna trains it on a frozen open base model.
_Avoid_: fine-tune, custom weights

**Dedicated model**:
A model with fully separate weights for one company. It costs more than an adapter.

## Contributor rules

**Spec**:
A GitHub issue that describes one piece of work. It has exactly one `P0`, `P1` or `P2` label.

**Feature stack**:
A set of related pull requests that `gh stack` links and that `gh stack merge` merges together.
_Avoid_: PR chain

**Coordinator work queue**:
The open GitHub issues with the owner label of the coordinator, `ready-for-agent`, and priority `P0` or `P1`.
_Avoid_: backlog, remembered queue

**Lead**:
The one `implement-spec` agent that owns a P0 spec until the spec is closed.

**Chief**:
The agent that receives the status lines from leads, such as `STARTED`, `MERGED` and `BLOCKED`.

**Local gates**:
The format, lint, type and test checks that a contributor runs before each push.
