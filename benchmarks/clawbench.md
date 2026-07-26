# ClawBench

ClawBench is an open-source benchmark for evaluating browser agents on everyday online tasks across live websites.

## Key Features

- Includes 283 tasks: 153 V1 tasks and 130 V2 tasks
- Covers 15 life categories such as shopping, travel, food, jobs, and personal management
- Runs each task in an isolated Docker or Podman container with Chromium
- Supports multiple selectable agent harnesses against the same browser runtime
- Records synchronized video, screenshots, HTTP traffic, browser actions, and agent messages
- Intercepts critical terminal requests before they create real-world side effects

## Evaluation

ClawBench measures end-to-end task completion rather than isolated clicks or static element grounding. Its V2 scoring pipeline first checks the intercepted request against the task schema, then uses an agentic judge to evaluate whether the captured payload fulfills the instruction.

The full five-layer trace is retained for failure analysis, allowing evaluators to inspect what the agent saw, did, requested, and reported during a run.

## Performance Metrics

The live leaderboard reports results by corpus and agent harness. V2 reports both the deterministic intercepted-request rate and judge-scored task reward.

## References

- Paper: https://arxiv.org/abs/2604.08523
- Website and leaderboard: https://claw-bench.com/
- Code: https://github.com/TIGER-AI-Lab/ClawBench
- Dataset: https://huggingface.co/datasets/NAIL-Group/ClawBench
