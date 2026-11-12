# Experiments

This directory contains test plans, testbed descriptions, protocols, and experiment reports.

## Initial testbed concept

A first testbed may use approximately ten nodes across several network segments, with at least two transport types, local services, and a distributed data repository.

The exact hardware and topology remain to be selected. No particular device count or transport is a fixed requirement until the test objectives and resource constraints are reviewed.

## Experiment lifecycle

1. **Question** — define the behaviour to be tested.
2. **Baseline** — document normal operation before disruption.
3. **Intervention** — introduce one controlled failure or network condition.
4. **Observation** — collect logs, metrics, and user-visible outcomes.
5. **Recovery** — restore connectivity and observe resynchronization.
6. **Analysis** — compare results with predefined success criteria.
7. **Reproduction** — provide enough detail for another researcher to repeat the test.

## Minimum report fields

- Experiment ID, title, date, and author.
- Objective and hypotheses.
- Hardware, operating systems, software versions.
- Topology, addressing, and transport configuration.
- Baseline measurements.
- Failure conditions and exact procedure.
- Logs, metrics, and observed outcomes.
- Limitations, anomalies, and interpretation.
- Evidence label and next steps.

Do not publish credentials, private keys, personal data, or sensitive network details in experiment reports.
