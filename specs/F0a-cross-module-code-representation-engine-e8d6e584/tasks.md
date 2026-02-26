# Tasks: Cross-Module Code Representation Engine

- [ ] **F0a-T1: Domain Models and AST Structures**
  Define the core data structures for representing a Project-wide AST and control flow nodes.
  *Refs: F0a-1*
  - [ ] **F0a-T1.1: Define Global AST Schema**
    Implement Node and Edge models for the Global AST including metadata for file locations and scope.
  - [ ] **F0a-T1.2: Implement Type-Hint Registry**
    Create a TypeHint registry that maps symbols to their annotated types to support Type-Hint Priority.
    *Refs: F0a-5*
- [ ] **F0a-T2: Data Flow and Reachability Services落**
  Core logic for traversing the AST and building cross-module execution paths.
  *Refs: F0a-2, F0a-3, F0a-5*
  - [ ] **F0a-T2.1: Cross-Module Call Graph Linker**
    Implement logic to link function calls in one module to their definitions in another. Verify call-return integrity.
    *Refs: F0a-2*
  - [ ] **F0a-T2.2: Data Flow Propagation Engine**
    Implement the flow-sensitive analysis engine that incorporates type-hint data to refine path resolution.
    *Refs: F0a-5*
  - [ ] **F0a-T2.3: Reachability Pruning Logic落**
    Develop the pruning algorithm to remove paths that lack valid entry points or are blocked by logic constraints.
    *Refs: F0a-3*
- [ ] **F0a-T3: Dependency Integration Adapters落**
  Integration layer for external libraries and project dependencies.
  *Refs: F0a-4*
  - [ ] **F0a-T3.1: Third-Party Dependency Scanner**
    Implement a collector that scans requirements files and installed packages to build a dependency map.落
    *Refs: F0a-4*
  - [ ] **F0a-T3.2: Library Signature Adapter落产**
    Map external library signatures to the internal AST representation to enable global tracing.
    *Refs: F0a-4*
