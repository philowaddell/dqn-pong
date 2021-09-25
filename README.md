# dqn-pong
The DQN agent successfully learned a policy that allowed the it to win consistently after 600,000 network updates. It then continued to refine this policy until the rate of improvement levelled out at 800,000 updates, with an average total reward of 10. This is equivalent to the agent winning 11-21.

The average score continued to improve slowly after 1M network updates; however, I suspect it would be necessary to further reduce below 0.1 to increase the rate of improvement. The graph shows that the agent is capable of achieving a perfect score in some games, but the current degree of exploration prevents it from fully exploiting its learned policy. This hypothesis was proven from video footage of the agent applying a strictly greedy policy, where it would often achieve a total reward of 20 or more.

Observations of its playing style reveal that it often fails to return the first serve of the episode. This could be as a result of the slight variation between the first point and all subsequent points, as the game starts with the opponents paddle hidden from the player. I suspect several thousand more training episodes would allow the agent to derive a policy for this initial serve.

The size of the replay buffer used was 50,000 experiences, this could not be made any bigger due to memory constraints. However, utilising a larger replay buffer and pre-filling it with experiences could improve learning across early episodes. The episodic reward totals plot shows a distinct lag when learning starts, after which the agent improves rapidly.
