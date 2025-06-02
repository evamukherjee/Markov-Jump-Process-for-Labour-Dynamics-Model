# Markov Jump-Process for Labour Dynamics Model

## Introduction

In labor market dynamics, understanding the transition out of unemployment is crucial for analyzing job search behavior and labor force participation. Workers continuously move between states of employment (E), unemployment (U), and inactivity or being out of the labor force (O), reflecting complex behavioral and institutional factors. To capture these dynamics, we model the labor market as a continuous-time Markov jump process with three states: E, U, and O. The transition intensities between these states are encoded in a generator matrix, allowing for a probabilistic yet tractable representation of individual labor market trajectories. This framework enables us to analytically compute key quantities such as the stationary distribution—reflecting the long-run proportions of the population in each state—and the expected time to reach employment starting from either unemployment or inactivity. These theoretical insights are further supported by numerical simulations, offering a comprehensive view of absorption dynamics in the labor market.

## Definition of the Model

We define the discrete state space $S$ for an individual's employment status as:
* $E$: Employed
* $U$: Unemployed
* $0$: Out of Labour Force

The model allows for transitions between all pairs of these states. For an individual in state $i$, they can transition to state $j$ ($i \neq j$) with a constant rate $\lambda_{ij} \ge 0$. These rates represent the intensity of the random events causing status changes:
* $\lambda_{EU}$: Rate of job loss (E $\to$ U)
* $\lambda_{EO}$: Rate of leaving the labor force from employment (E $\to$ O)
* $\lambda_{UE}$: Rate of finding a job from unemployment (U $\to$ E)
* $\lambda_{UO}$: Rate of leaving the labor force from unemployment (U $\to$ O)
* $\lambda_{OE}$: Rate of entering employment from out of the labor force (O $\to$ E)
* $\lambda_{OU}$: Rate of entering unemployment from out of the labor force (O $\to$ U)

The holding time in each state $i$ before a transition occurs is exponentially distributed with rate $q_i = \sum_{j \neq i} \lambda_{ij}$.
