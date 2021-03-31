+++
date = "2021-01-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "sample_efficient_reinforcement_learning"
short_description = "Learning to learn faster"
title = "Sample Efficient Reinforcement Learning"
[[participants]]
    name = "Calvin Seward"
    is_member = true
    id = "calvin_s"

[[participants]]
    name = "Kashif Rasul"
    is_member = true
    id = "kashif_r"

[[participants]]
    name = "Ingmar Schuster"
    is_member = true
    id = "ingmar_s"
    
[[participants]]
    name = "Roland Vollgraf"
    is_member = true
    id = "roland_v"
+++

### Research Project by [Calvin Seward](/member/calvin_s), [Kashif Rasul](/member/kashif_r), [Ingmar Schuster](/member/ingmar_s) & [Roland Vollgraf](/member/roland_v)
![](/project/sample_efficient_reinforcement_learning/img/robot.png)


Reinforcement learning has seen many successes in the last years, enabling
computers to beat human masters at such difficult tasks as Go and Atari games.
In addition, reinforcement learning is showing great promise in creating
exciting consumer facing technologies such as self driving cars, while also
driving behind the scenes efficiency gains with self learning recommendation
and pricing systems.

Yet despite all these gains there are major challenges still out there.
For one we have the issue of sample efficiency, the alphaGo computer had
to play 5.4 * 10^9 games to train. Even if Jesus after his resurrection
had set his mind to learning Go and played the game at an ungodly rate of
5 matches a minute ever since, he still wouldn’t have played as many games
as the AlphaGo computer during training. So clearly state-of-the-art
reinforcement learning methods are able to beat human masters, they must
play many more games than the human master practiced with. The Go master
still beats the computer in sample efficiency.

This issue becomes more pronounced when samples are expensive. One example
is robot control: there a sample is obtained by letting the robot move around,
which can take a few minutes to gather a sample. Clearly if we’re in the regime
where hundreds of billions of samples are required, the robot will probably not
be trained before the four horsemen of the apocalypse show up and ruin the experiment.

One reason sample efficiency is so difficult is because these are all delayed
reward environments where the reward becomes apparent only after a bunch of
interactions with the environment. With Q learning, it’s been shown that reward
delay exponentially increases the time it takes to reduce the bias of the learned
Q-function. In order to address this issue, many approaches craft an auxiliary
reward structures for the agent. For example, in chess the agent can gain reward
by capturing opposing pieces, lose if by having his pieces captured. In this way
the agent learns the intermediate goal of capturing opposing pieces which is
generally necessary to achieve the actual goal: checkmate.

While the approach gets good results in specific domains, for every new domain
the agent wishes to learn a new reward structure must be crafted by hand, and in
many cases not enough knowledge exists about the domain to hand craft such a good
reward structure. In addition, this puts an unnecessary upper limit on the
performance of the whole system by introducing a target which is not aligned
with the (generally unknown) best policy.

Therefore, in order to better understand this problem we’re researching bounds
on sample efficiency in simple, delayed reward settings, both minimax lower
bounds for all methods and concrete upper bounds for popular methods. With these
bounds in hand, we can understand the weaknesses in current methods and hopefully
find new methods that get close to lower bounds.
