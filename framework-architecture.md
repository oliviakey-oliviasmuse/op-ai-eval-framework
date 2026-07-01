Framework Architecture
The Four-Layer Model
Standard AI evaluation tests one thing: does the agent produce the right output? The Operational AI Agent Evaluation Framework tests four things in sequence:

Layer 1: Functional Correctness - Is the output correct? Layer 2: Operational Safety - Is it correct in THIS environment? Layer 3: Regulatory Compliance - Is it compliant TODAY? Layer 4: Catastrophic Failure Prevention - Does it catch the worst cases?

An agent that passes Layer 1 but fails Layer 2 is a deployment risk. An agent that passes Layers 1-3 but fails Layer 4 is a liability.

Why Four Layers
Layer 1 is necessary but not sufficient. Operational context is not in training data. Regulations change. Training data does not. Catastrophic scenarios are rare by definition. Standard evaluation misses them.

Scoring Model
Six dimensions x four layers = 24 scoring touchpoints per evaluation.

The six dimensions are universal. The layer-specific emphasis varies by industry.

Deployment Decision Matrix
Layer 1 PASS + Layer 2 PASS + Layer 3 PASS + Layer 4 PASS = Approved Layer 1 PASS + Layer 2 PASS + Layer 3 PASS + Layer 4 FAIL = Conditionally Approved (Layer 4 re-test required) Layer 1 PASS + Layer 2 PASS + Layer 3 FAIL = Not Approved Layer 1 PASS + Layer 2 FAIL = Not Approved Layer 1 FAIL = Not Approved

Conditionally Approved requires: Layer 4 re-test after Layer 2 remediation.
