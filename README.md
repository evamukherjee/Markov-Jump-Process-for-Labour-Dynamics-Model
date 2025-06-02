# Markov Jump-Process for Labour Dynamics Model

## Introduction

In labor market dynamics, understanding the transition out of unemployment is crucial for analyzing job search behavior and labor force participation. Workers continuously move between states of employment (E), unemployment (U), and inactivity or being out of the labor force (O), reflecting complex behavioral and institutional factors. To capture these dynamics, we model the labor market as a continuous-time Markov jump process with three states: E, U, and O. The transition intensities between these states are encoded in a generator matrix, allowing for a probabilistic yet tractable representation of individual labor market trajectories. This framework enables us to analytically compute key quantities such as the stationary distribution—reflecting the long-run proportions of the population in each state—and the expected time to reach employment starting from either unemployment or inactivity. These theoretical insights are further supported by numerical simulations, offering a comprehensive view of absorption dynamics in the labor market.

