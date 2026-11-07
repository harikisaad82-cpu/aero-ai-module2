# Behaviorist AI: Learning Through Rewards and Penalties

**Team:** Aero AI
**Module:** Hardware, Networks & Behaviorist AI
**Topic leader:** El Mehdi Lamghari
**Status:** Peer-reviewed (V2.0)

## Learning Outcomes

After this section, learners should be able to:

- Explain how an agent learns from rewards and penalties.
- Name and use the terms agent, environment, state, action, reward, and policy.
- Calculate cumulative reward and explain why it matters more than a single reward.
- Explain exploration versus exploitation.

**Prerequisite:** none. Learners only need to know what a computer program is.

## 1. Introduction to Behaviorist AI

Behaviorist AI is an approach to artificial intelligence inspired by **behaviorism**, a psychological theory that studies how behavior changes through experience and feedback. For example, B. F. Skinner studied how the consequences of an action make animals more or less likely to repeat it.

In AI, an important related approach is **Reinforcement Learning (RL)**. It allows an intelligent agent to learn by interacting with its environment and receiving rewards or penalties. RL borrows the idea of learning from consequences, but it is a computational method, not the same thing as behaviorist psychology.

Instead of being told exactly what to do every time, the agent tries different actions and learns which actions produce better results.

**Simple example:** imagine a robot learning to move through a maze.

- When it moves in the correct direction, it receives a positive reward.
- When it hits a wall, it receives a penalty.
- When it reaches the destination, it receives a large reward.

After many attempts, the robot can learn a better path.

### Main idea

Learning happens through three important steps:

1. The agent performs an action.
2. The environment gives feedback.
3. The agent uses this feedback to improve its future decisions.

## 2. Important Vocabulary

| Term | Simple explanation |
|---|---|
| Agent | The learner or decision-maker, such as a robot. |
| Environment | The world where the agent operates. |
| State | The current situation or position of the agent. |
| Action | Something the agent decides to do. |
| Reward | A positive or negative signal received after an action. |
| Policy | The strategy used by the agent to choose actions. |
| Reinforcement Learning | A learning method based on actions and feedback. |
| Exploration | Trying new actions to discover better choices. |
| Exploitation | Choosing actions already known to give good results. |
| Immediate reward | The reward received directly after an action. |
| Cumulative reward | The total reward collected over multiple actions and time steps. |

## 3. How Does Reinforcement Learning Work?

Reinforcement Learning follows a continuous learning cycle:

1. The agent observes its current state.
2. It chooses an action.
3. The environment responds to that action.
4. The agent receives a reward or penalty.
5. It updates its knowledge and chooses future actions.

This process continues until the agent learns a useful strategy.

### The learning cycle

```text
   +----------------------------------+
   |                                  |
   v                                  |
[1. Agent observes the state]         |
   |                                  |
   v                                  |
[2. Agent chooses an action]          |
   |                                  |
   v                                  |
[3. Environment responds]             |
   |                                  |
   v                                  |
[4. Agent gets a reward or penalty]   |
   |                                  |
   v                                  |
[5. Agent updates its knowledge] -----+
```

**Explanation:** the agent learns from the consequences of its actions. Better decisions can produce higher rewards over time.

## 4. Immediate Rewards vs. Cumulative Rewards

An important concept in Reinforcement Learning is the difference between immediate rewards and cumulative rewards.

- **Immediate reward:** the reward received directly after performing an action. Example: a robot moves closer to its target and receives +5 points.
- **Cumulative reward:** the total reward collected over a sequence of actions, including future rewards.

**Example:** a robot receives +5 for moving closer, −1 for an unnecessary movement, and +20 for reaching its destination. Its total reward is:

5 − 1 + 20 = **24 points**

The main difference is that an action with a high immediate reward is not always the best long-term decision. An intelligent agent should consider how its current actions affect its future rewards.

**Key takeaway:** Reinforcement Learning aims to maximize cumulative reward over time, not simply obtain the highest immediate reward.

## 5. Worked Example: A Robot Learning to Find Its Way

A robot must move through a simple environment to reach a target. It receives these rewards:

| Situation | Reward |
|---|---|
| Moves closer to the target | +5 |
| Hits a wall | −5 |
| Reaches the target | +20 |
| Makes an unnecessary move | −1 |

### Step by step (one run)

At the beginning, the robot does not know the best route.

1. **Step 1:** the robot moves forward and hits a wall. It receives **−5** and learns that this action was not useful in this situation.
2. **Step 2:** it chooses another direction and moves closer to the target. It receives **+5**.
3. **Step 3:** it continues in the correct direction and reaches the target. It receives **+20**.

**Cumulative reward for this run:** −5 + 5 + 20 = **20 points**.

Over many runs, the robot compares its results and adjusts its **policy**, its strategy for choosing actions in each state. Eventually it prefers the actions that lead to the highest cumulative reward.

### Important: actions depend on the current state

An action is not always good or bad by itself. Its usefulness depends on the robot's current state and position in the environment. For example:

- Moving left may be useful when the robot is near the right side of a maze.
- Moving left may be harmful when there is a wall immediately to its left.
- Moving forward may be the best choice in one position but a mistake in another.

Therefore, the robot must consider its current state before selecting an action.

**Result:** after several runs, the robot can learn to prefer actions that lead to higher cumulative rewards and avoid actions that repeatedly produce penalties. This shows how feedback can improve an AI agent's behavior.

## 6. Summary Table: Agent and Environment

| Component | Example in the robot task |
|---|---|
| Agent | The robot |
| Environment | The maze |
| State | The robot's current position |
| Action | Move left, right, forward or backward |
| Reward | Points received after moving |
| Goal | Reach the destination successfully |

The environment provides feedback, while the agent uses that feedback to improve its decisions.

## 7. Practical Activities

### Activity A: Predict the robot's next action

A robot is learning to move through a maze. It has two possible actions:

- **Action A:** move left and receive +10 points.
- **Action B:** move right and receive −5 points.

Assume the robot has already tried both actions several times and chooses the action that gives the higher reward.

1. Which action should the robot prefer?
2. What would happen if moving left repeatedly led to a wall and a −10 penalty instead?

### Activity B: Find the mistake

A student describes Reinforcement Learning as follows:

> "The AI agent receives rewards and penalties, but it never changes its decisions. It always performs the same action."

3. What is the mistake in this explanation?
4. Explain how feedback helps the agent improve its behavior.

### Activity C: Immediate or cumulative?

Use the reward table from Section 5. The robot can take two routes:

- **Route A:** closer (+5), closer (+5), hits a wall (−5), unnecessary move (−1), closer (+5), reaches the target (+20).
- **Route B:** unnecessary move (−1), closer (+5), closer (+5), closer (+5), reaches the target (+20).

5. Which route gives the higher reward on the first step?
6. Calculate the cumulative reward of each route. Which route is better, and why?

### Activity D: Explore or exploit?

A robot has found a path that always gives a total of 20 points. It has never tried the path on the left.

7. What could the robot miss if it only exploits what it already knows?
8. Why would a robot that only explores also be a bad learner?

## 8. Answers and Explanations

**Answer 1.** Action A, because +10 is higher than −5. The agent tries to choose actions that produce better rewards.

**Answer 2.** Action B (−5) is now better than Action A (−10), so the robot should switch to moving right. The agent should learn from new feedback and change its choice when another action gives a better result.

**Answer 3.** The mistake is saying that the agent never changes its decisions. Reinforcement Learning lets an agent update its strategy based on the rewards and penalties it receives.

**Answer 4.** Feedback shows the agent which actions are useful and which should be avoided. By learning from experience, the agent can improve its future decisions and increase its expected cumulative reward.

**Answer 5.** Route A (+5 on the first step, against −1 for Route B).

**Answer 6.**
- Route A: 5 + 5 − 5 − 1 + 5 + 20 = **29**
- Route B: −1 + 5 + 5 + 5 + 20 = **34**

Route B is better. Its first step has a lower immediate reward, but it avoids the wall, so its cumulative reward is higher. This is why RL aims to maximize cumulative reward, not just the next reward.

**Answer 7.** It might never discover a shorter or higher-scoring path, because it never tries anything new.

**Answer 8.** It never uses what it has learned, so it keeps repeating random actions and wastes rewards. A good agent balances exploration and exploitation.

## 9. Real-World Applications of Reinforcement Learning

Reinforcement Learning is used in different fields to help intelligent systems make better decisions through experience.

1. **Robotics:** robots can learn to walk, balance and perform tasks through repeated attempts. Example: a robot learns to walk without falling by receiving feedback about its movements and balance.
2. **Video games:** AI agents can learn strategies by playing games and receiving rewards for successful actions.
3. **Autonomous systems:** intelligent systems can improve decisions in changing environments. Example: a simulated self-driving vehicle learns to keep a safe distance from other vehicles.
4. **Industrial automation:** machines can improve their operations by learning from feedback. Example: an industrial robot learns to perform a repetitive task more efficiently while reducing unnecessary movements.
5. **Resource management:** AI systems can learn how to distribute limited resources efficiently. Example: a data center system learns to allocate computing resources to reduce energy use while maintaining performance.

These examples show how learning through feedback can help intelligent systems improve in practical situations.

## 10. Conclusion

Behaviorist AI introduces the idea that intelligent behavior can improve through experience and feedback. Reinforcement Learning applies this idea by allowing agents to learn through rewards and penalties.

The agent observes its environment, takes actions, receives feedback and improves its strategy over time. An action's usefulness depends on the current state, and the best decision should consider both immediate and future rewards.

**Key takeaway:** an intelligent agent does not need to know the perfect action from the beginning. It can learn better decisions through experience, feedback and repeated interaction with its environment.

## 11. References

- Sutton, R. S., & Barto, A. G. (2018). *Reinforcement Learning: An Introduction* (2nd ed.). The MIT Press. http://incompleteideas.net/book/the-book-2nd.html
- Skinner, B. F. (1938). *The behavior of organisms: An experimental analysis.* Appleton-Century.
- Further reading (not needed for beginners): Sutton, R. S. (1988). Learning to predict by the methods of temporal differences. *Machine Learning, 3*, 9–44. https://doi.org/10.1007/BF00115009
