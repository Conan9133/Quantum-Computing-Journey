Before running the Quantum programs on a Quantum computer, it is better to check the validity and the performance under the same simulated conditions.
This can be done by using Quantum Simulators. These are tools that mimic the behaviour of quantum systems using classical hardware.
These are useful for developing and testing Quantum algorithms without requiring access to actual Quantum hardware.
There are many types of simulators. Some of the important ones are 

1. Aer Simulators: (qiskit_aer)
   a. qasm_simulator
   b. statevector_simulator
   c. others

2. Fake backends:
   These mimic the behaviour of IBM QPUs by using QPU snapshots

Even in simulators, we cannot simulate bigger circuits as the cost of simulating quantum circuits scales exponentially with the number of qubits.
In those situations, one can use either test for smaller versions of circuits or modify the circuits so that they can be easily classically simulable (less accurate).
These modified circuits are called Stabilized circuits or Clifford circuits.


