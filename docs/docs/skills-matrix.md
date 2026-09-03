# Skills matrix: what rises, falls and changes shape

The matrix rates **relative differentiation**, not whether a skill becomes useless.

| Skill | Direction | Why | Evidence to build |
|---|---:|---|---|
| Manual boilerplate and syntax recall | ↓↓ | Agents already automate common implementation | Read and debug fluently; stop optimizing typing speed |
| Memorizing framework APIs | ↓↓ | APIs are retrievable and frameworks turn over quickly | Learn on demand; keep durable mental models |
| Standard CRUD and simple UI delivery | ↓↓ | Common, well-specified patterns are highly delegable | Use them to test ideas, not as a moat |
| Prompt tuning without evals | ↓↓ | Local wins are brittle and hard to reproduce | Versioned eval set and regression result |
| Code review by visual diff scanning | ↓ | Output volume exceeds human attention | Review contracts, tests, behavior and risk boundaries |
| Deep coding fluency | ↔ | Less scarce for production, still essential for diagnosis | Explain and repair agent failures without dependence |
| System design | ↑ | Cheap components increase integration and state complexity | ADRs, invariants, load/failure tests, rollback |
| Problem framing | ↑↑ | Agents need bounded objectives and acceptance criteria | Spec that another person/agent can execute correctly |
| Evaluation engineering | ↑↑ | Probabilistic behavior needs measurement | Gold/adversarial sets, oracle, error taxonomy |
| Security and permissions | ↑↑ | Agents add tool authority and attack surface | Threat model, least privilege, red-team regression |
| Observability and incident response | ↑↑ | More autonomous action demands reconstruction and control | Traces, replay, SLOs, postmortem-to-test time |
| Domain expertise | ↑↑ | Domain judgment improves task selection and recovery | Correct handling of real exceptions and economics |
| Product discovery | ↑↑ | Building gets cheaper; choosing stays expensive | Paid use, retention, measured workflow change |
| Executive/customer communication | ↑↑ | Adoption and trade-offs remain social | Decision memo that changes roadmap or rollout |
| Distribution and trust | ↑↑ | Code can be copied faster than relationships | Repeatable acquisition channel and expansion |
| Multi-agent orchestration | ↑, conditional | Useful only when parallelism beats added coordination cost | Controlled comparison against a simpler baseline |

## Skills that change shape

### Coding fluency

Do not stop learning how software works. Shift from recall and greenfield typing toward:

- reading unfamiliar code quickly;
- diagnosing state, concurrency and integration failures;
- recognizing insecure or implausible output;
- shaping interfaces that constrain generated implementations;
- deciding when to discard rather than repair agent work.

### Code review

The merge decision remains human-owned in many systems, but line-by-line review cannot scale with agent output. Move review upstream and downstream:

- upstream: spec, threat model, invariants, migration and rollback;
- downstream: executable tests, runtime behavior, canary metrics and audit evidence.

### Architecture

Architecture becomes more important, not because every system needs more layers, but because cheap generation makes accidental complexity cheap too. Demand evidence for every agent, queue, abstraction and model call.

### Product management

Engineers and technical founders need more direct product skill. When a prototype costs hours, the bottleneck becomes finding a painful, frequent and reachable problem, then proving behavior change.

## Durable learning order

1. Evaluation and statistics.
2. Distributed systems and failure semantics.
3. Security, identity and permissions.
4. Observability and incident management.
5. Product discovery and domain economics.
6. Agent/framework mechanics as needed by the current project.
