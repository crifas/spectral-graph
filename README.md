# Spectral Graph: Centrality vs. Spectral Clustering

A Python model that tests whether standard centrality metrics can be trusted to find the key players in a network, and shows that spectral clustering recovers the real structure when they can't.

## The Problem

Centrality metrics (degree, betweenness) are a common way to flag "important" nodes in a network, such as the leaders of a covert group. But they can be fooled. A well-connected decoy hub looks important, while the people who actually coordinate the network sit quietly in the background.

## What This Project Does

- Builds synthetic networks with two scenarios: a **decoy hub** (a highly connected but unimportant node) and a **hidden command tree** (a concealed hierarchy of coordinators)
- Ranks nodes by **degree** and **betweenness centrality** and shows where those rankings point at the wrong nodes
- Applies **spectral clustering** and **max-flow** analysis to the same networks to uncover the underlying structure
- Compares the methods side by side on which nodes each one identifies as key players

## Tech Stack

Python, NetworkX, scikit-learn

## Getting Started

```bash
pip install networkx scikit-learn
python spectral_graph.py
```

## Status and Next Steps

This is an ongoing, multi-year research project. The current version runs on synthetic networks. Next steps are extending the analysis to real-world network data and adding statistical testing, with the goal of a publication-quality paper.

## Author

Chase Rifas, Mathematics (B.S.) with a Data Science minor, Texas Christian University
