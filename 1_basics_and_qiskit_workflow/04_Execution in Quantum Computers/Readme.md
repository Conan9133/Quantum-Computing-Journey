This step of a Qiskit workflow involves running your circuits on hardware and producing the quantum computation outputs.
The Quantum programs/circuits can be executed on a quantum computer using Primitives.
A primitive is like the smallest processing instruction, the simplest building block from which one can create something useful for a given abstraction level.
It is optimized for two core tasks in Quantum Algorithm development: Expectation value estimation (Estimator) and circuit sampling (Sampler).
There are two types of Qiskit primitives: Base Classes and their implementations. The base classes are just two in number, one for each task.
Ex: BaseEstimatorV2 (for estimator) and BaseSamplerV2 (for sampler).
Whereas the implementations are just how these base classes work in different environments, such as

1. Qiskit Runtime primitives: EstimatorV2, SamplerV2

2. Reference primitives: StatevectorEstimator, StatevectorSampler

3. Backend primitives: BackendEstimatorV2, BackendSamplerV2


For different types of Quantum workloads, there will be different ways of scheduling tasks. This job is done by the "Execution Modes" module in Qiskit. Execution modes determine how the jobs are scheduled. And, choosing the right execution mode allows your workload to run efficiently within your budget. 
There are three execution modes depending on tasks: Job, Session, and Batch.
