Before running the Quantum programs on a Quantum computer, it is better to check the validity and the performance under the same simulated conditions.
This can be done by using Quantum Simulators. These are tools that mimic the behaviour of quantum systems using classical hardware.
These are useful for developing and testing Quantum algorithms without requiring access to actual Quantum hardware.
There are many types of simulators. Some of the important ones are 

1. Aer Simulators: (qiskit_aer)
   
   a. qasm_simulator
   
   b. statevector_simulator
   
   c. others

3. Fake backends: These mimic the behaviour of IBM QPUs by using QPU snapshots
   
Even in simulators, we cannot simulate bigger circuits as the cost of simulating quantum circuits scales exponentially with the number of qubits.
In those situations, one can use either test for smaller versions of circuits or modify the circuits so that they can be easily classically simulable (less accurate).
These modified circuits are called Stabilized circuits or Clifford circuits.

To test and debug the Quantum programs:

1. For simulating using Qiskit Runtime, use Fake Backends

   Simulates real IBM Quantum devices including noise models, coupling maps, and gate errors.
   
2. For simulating small circuits, use the reference primitives

   These reference primitives perform local state vector simulations.

   Do not support modelling device noise.

   Uses "Statevector Estimator" and "Statevector Sampler" functions for Estimator primitive and Sampler primitives, respectively.

3. For simulating large circuits as well as noise models in simulation, use Qiskit Aer

   QiskitAer is a high-performance quantum circuit simulator that one can use as a substitute for reference primitives for better performance and include noise models.

   Uses QiskitAer primitives such as Estimator and Sampler.

4. Modifying the circuits to efficiently simulate stabilizer circuits

   These circuits consist only of the following circuits: CX, H, S, and measurement.

The above information is adopted from the Qiskit Guides page. For more information, please see the [..........]

Add a file that has example of those.



   
