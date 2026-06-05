# NFL-Offensive-Tendencies-Clustering

## Overview
This project uses unsupervised machine learning to objectively identify offensive philosophies across all 32 NFL teams, and examines whether certain philosophies correlate with sustained winning. Rather than relying on subjective labels like "run-heavy" or "spread offense", the clustering pipeline builds those categories from the ground up using play-by-play and participation data.

## Methodology
The pipeline works in two stages:

Stage 1 — Play Archetype Clustering

~32,000 individual offensive plays from the 2025 NFL regular season are clustered using K-Means (k=10, selected via elbow method) on a feature set combining game context and offensive decisions. Each cluster represents a distinct recurring combination of situation and response.

Stage 2 — Team Philosophy Clustering

Each team is represented as a distribution across the 10 play archetypes. Teams are then clustered a second time (k=9, selected via elbow method) on these distributions, grouping together offenses that deploy similar mixes of play types across similar game situations.

The trained models are then applied to the 2023, 2024 and 2025 seasons to examine how team philosophies evolve over time and whether certain philosophies consistently produce more wins.

## Key Findings

Offensive philosophy groups showed measurable differences in average win totals, with certain archetypes (e.g. High-Motion / Wide-Zone Boot System) consistently outperforming others across all three seasons examined.

Several teams shifted philosophy groups between seasons, and these changes often appeared to display large changes in win totals. 
