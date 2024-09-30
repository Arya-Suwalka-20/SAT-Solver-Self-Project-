# SAT Solver

<!-- **Author:** Arya Suwalka -->

## Description 
This repository contains a SAT (Boolean satisfiability problem) solver implemented in C++. It utilizes the DPLL algorithm with enhancements like unit propagation and pure literal elimination to efficiently search for satisfying assignments for Boolean formulas in Conjunctive Normal Form (CNF).
Input the name of DIMACS file from which input is to be taken. You will get the output.

## Implemented Techniques

* DPLL Algorithm: The core algorithm is DPLL (Davis-Putnam-Logemann-Loveland), which employs backtracking to explore the search space of possible assignments.
* Unit Propagation: This optimization identifies unit clauses (containing only one unassigned literal). Any such literal must be assigned a value to satisfy the clause, eliminating the need for backtracking decisions. It can lead to long chains of unit assignments, significantly reducing the search space.
* Pure Literal Elimination: A variable is considered "pure" if it always appears with the same polarity (positive or negative) in all clauses. Pure literals can be assigned a value that satisfies all clauses containing them, allowing them to be safely removed from the formula as they no longer impose constraints.

<!-- ## Building and Running

This section explains how to compile and run the SAT solver:

**1. Compiling the Code:**

Use a C++ compiler like `g++` to compile the `SAT_Solver.cpp` file:

```bash
g++ SAT_Solver.cpp -o sat_solver -->