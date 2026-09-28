Smooth Cubic Surfaces over a Non-Algebraically Closed Field

Computational work carried out as part of a TÜBİTAK research project using the Orbiter mathematical software system.

Overview

This repository contains my implementations, experiments, and computational results developed during the project. The work focuses on computational problems involving finite fields, projective geometry, algebraic curves, graph theory, and incidence structures using Orbiter.

My Contributions

During the project, I extended the Orbiter source code with new functionality and implemented computational procedures for the assigned problems.

Problem 1 — Repeated Double Cover Graph Construction

For Problem 1, I implemented a repeated double cover graph construction in Orbiter.

A new command was added:

-yusuf_eray_double_cover depth

The implementation required modifications to several parts of Orbiter, including command-line parsing, graph creation, graph theory domain functionality, header declarations, adjacency matrix construction, and the build configuration.

The construction starts from a one-vertex graph and recursively builds the next graph by expanding the adjacency matrix from N × N to (2N+1) × (2N+1). The previous adjacency matrix is copied into two blocks, and a new vertex is added and connected to one copy of the previous vertex set.

The resulting graphs were analyzed using Orbiter's graph-theoretic activities, including:

eigenvalue computation
eigenvalue reports
automorphism group computation
adjacency matrix export

For depths from 0 to 7, the construction produced graphs with 1, 3, 7, 15, 31, 63, 127, and 255 vertices.

The corresponding adjacency-matrix ranks were 0, 2, 6, 14, 30, 62, 126, and 254.

The computed examples follow the pattern:

rank(A) = |V| - 1

Detailed implementation steps and computational results are available in Q1_REPORT.pdf.

Problem 2 — Kovalevski Configurations of Quartic Curves

For Problem 2, I investigated Kovalevski configurations of smooth quartic curves over finite fields using Orbiter.

For each successfully constructed curve, I computed:

rational points on the curve
bitangents
Kovalevski points
incidence structures
incidence matrices
flag counts

The computations were carried out over GF(9), GF(11), and GF(17).

The obtained results were:

Field	Points on Curve	Bitangents	Kovalevski Points	Incidence Matrix	Flags
GF(9)	28	28	63	28 × 63	252
GF(11)	0	28	21	28 × 21	84
GF(17)	12	28	15	28 × 15	60

In every successfully computed case, each Kovalevski point is incident with exactly four bitangents. This agrees with the reported flag counts:

GF(9):  63 × 4 = 252
GF(11): 21 × 4 = 84
GF(17): 15 × 4 = 60

The q = 13 case could not be completed in my Orbiter build. The normal-form construction stopped with the following error:

grassmann::rank_lint error, does not have full rank

Further details and the generated incidence matrix drawings are included in Q2_REPORT.pdf.

Repository Structure
.
├── Q1_REPORT.pdf
├── Q2_REPORT.pdf
│
├── Question_1/
│   ├── Makefile
│   ├── modified Orbiter source files
│   ├── header files
│   └── outputs
│
└── Question_2/
    ├── Makefile
    └── outputs/
        ├── Orbiter-generated reports
        └── incidence matrix drawings
Technologies
C++
Orbiter
Make
LaTeX
Finite Field Computation
Graph Theory
Projective Geometry
Algebraic Geometry
References
Anton Betten, Orbiter User's Guide
Anton Betten, Graph Theory with Orbiter
Orbiter source code
