# FlightDynamicsProblems

## About 

Hello and thank you for your application for the position of Flight Dynamics Software Engineer at Poincaré Trajectories: you have been shortlisted for the position! If you are interested in this but you hadn't applied for the position, please join [our discord](https://discord.gg/aHBYj9tb), and let's have a chat.

Note that, until we are ready to open up to investors, our team will be operating on a work-for-equity model. Specifically [this model](https://slicingpie.com/learn-slicing-pie-model/). Reach out with any questions about it.

Here are some problems to help us understand how you work/think/program/write/communicate.


## Problem 1 - Orbital Mechanics

- Using the Julia programming language, and the DiffEq library, in particular, implement the [Hénon–Heiles system](https://arxiv.org/pdf/2206.04467.pdf).
- Numerically integrate the system using all the parameters of Section (1), page 19, together with $p_y = y = 0$. Use the best-suited solver and associated inputs. Plot the trajectory in the following planes: $(p_y, y), (x, y)$.
- Assuming the second component of the initial condition:
$$y \sim \mathcal{N}(\mu,\,\sigma^{2}) $$
$$\mu = 0 $$
$$\sigma = 0.01 $$

perform a Monte Carlo to estimate and represent the evolution of the first four statistical moments of the four components of the state. 

## Problem 2 - Koopman Generator

[This script](https://github.com/PoincareTrajectories/KoopmanGenerator.jl/blob/main/src/kk/linearies_.jl) builds on [this work](https://arxiv.org/abs/2111.07485v1) to obtain an analytical approximation of the Koopman Generator of the Duffing Oscillator.

In this problem you are asked to:

- Estimate the minimum Order of the basis functions such that: 
```julia
maximum(q-xn) < 0.01
```
$$
\forall	(q_0, p_0) \in [0, 1] \times [0, 1]
$$

- Assuming an initial condition:

$$q_0 \sim \mathcal{N}(\mu,\,\sigma^{2}) $$
$$\mu = 0.5 $$
$$\sigma = 0.01 $$

estimate minimum Order of the basis functions such that the maximum offset between the numerically and analytically computed expectation of the position is below a given threshold:

$$
\max (\Delta \mathbb{E}(q(t))) < 0.01
$$

## Utils

- The evaluation will be done against a GitHub private repository to be shared with us after the deadline.

- There is no need to write a report: documentation of the scripts you develop is however important.

- Together with documented codes, we will look into figures and data: please store in your repo all the output you believe relevant. Reproducibility is key.

- You can and you are encouraged to ask for clarifications: a new category "Flight Dynamics" has been created for this in the Discord. Let's try not to communicate outside the public group chat to avoid information asymmetries.

- The deadline is 2022-09-30, 11.59 pm CET. 

Have a nice week! :rocket: :rocket: :rocket: