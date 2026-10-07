# Scalable Majority Illusion Elimination in Social Networks

Research code for my Master's thesis at the New Economic School.

This project studies whether structural interventions in a social graph
can reduce majority illusion and, consequently, opinion cascades.

The approach combines:

- graph-theoretic Majority Illusion Elimination (MIE);
- exact local optimization via mixed-integer programming;
- Louvain community decomposition for scalability;
- a real Instagram follower network;
- LLM-based agents for behavioral cascade simulation.

## Research question

A globally minority opinion may appear locally dominant to many users
because of the structure of the social graph. Can this distortion be
removed by modifying only a small number of edges, and does doing so
change subsequent opinion dynamics?

## Method

The pipeline consists of four stages:

1. Detect communities in the original social network using Louvain.
2. Identify nodes affected by majority illusion.
3. Solve a local edge-editing optimization problem inside each community.
4. Compare opinion cascades on the original and treated graphs using
   LLM-based agents.
