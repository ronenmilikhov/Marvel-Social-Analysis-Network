# Marvel Universe Social Network Analysis

## Composers
* **Ronen Milikhov**
* **Shachar Wilk**
* **Or Sadof**
* Institution: Ruppin Academic Center
* Course: Graph Algorithms

## Overview
This project models the Marvel Comics Universe as a massive, undirected social network to uncover its underlying structural mechanics. By applying graph theory algorithms, we analyze a dataset of over 6,400 characters and 167,000 co-occurrence connections to find key influencers, detect natural character factions, and predict future team-ups.

## Key Features & Research Questions
* **Centrality & Influence:** Evaluated characters using **Degree Centrality** and approximate **Betweenness Centrality** to distinguish popular "hubs" (e.g., Captain America) from structural "bridges" (e.g., Spider-Man, Wolverine) that connect disparate parts of the universe.
* **Blind Community Detection:** Applied the **Louvain Algorithm** to autonomously partition the network into 26 communities (Modularity Score: Q = 0.4228). We validated the detected structure against source-level co-occurrence records in `edges.csv`: 61.46% of reconstructed character-pair edges remained within communities, compared with a 15.05% community-size baseline.
* **Link Prediction (Network Heuristics):** Designed a controlled classification experiment by masking 1% of existing edges. Using structural heuristics (**Common Neighbors, Jaccard Coefficient, Adamic-Adar Index**), all three heuristics produced the same binary predictions under the selected threshold, with an **Accuracy of 82.18%** and an **F1-Score of 84.87%**.

## Repository Structure
* `Graph_Algorithms_Final_Project.ipynb` - The complete, self-contained Python notebook containing all data processing, algorithm implementations, and visualization code.
* `Graph Algorithms Final Project - Summary Report.pdf` - A comprehensive academic report detailing our methodology, controlled experiment setup, and narrative interpretation of the results.
* `Graph_Algorithms_Presentation.pdf` - The slides used to present the project's motivation and key findings.