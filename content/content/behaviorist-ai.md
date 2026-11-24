# Behaviorist AI: Learning Through Rewards and Penalties

**Team:** Aero AI
**Module:** Hardware, Networks & Behaviorist AI
**Topic leader:** El Mehdi Lamghari
**Status:** Final version (Stage 3)

## Learning Outcomes

After this section, learners should be able to:

- Explain how an agent learns from rewards and penalties.
- Name and use the terms agent, environment, state, action, reward, and policy.
- Calculate cumulative reward and explain why it matters more than a single reward.
- Explain exploration versus exploitation.
- Explain why the best action depends on the agent's current state.
- Show, using the maze activity, that changing a reward can change the best route.

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

**Explanation:** the agent learns from the consequences of its actions. Better decisions can produce higher rewards over time. The cycle is a beginner-friendly overview: real RL algorithms use different update methods and may include additional calculations. A picture of the cycle is in `Figure3_RL_Cycle.png` (see Section 12).

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

Therefore, the robot must consider its current state before selecting an action. The policy connects each state to a suitable action.

**Result:** after several runs, the robot can learn to prefer actions that lead to higher cumulative rewards and avoid actions that repeatedly produce penalties. This shows how feedback can improve an AI agent's behavior.

## 6. Exploration vs. Exploitation

**Exploration** means trying an unfamiliar action to discover whether it could produce a better result. **Exploitation** means using an action the agent already believes works well.

- If the robot only exploits, it may never discover a better route.
- If the robot only explores, it may waste time repeating trials instead of using what it has learned.

A useful learning strategy balances both. You will experience this trade-off yourself in Activity 7.

## 7. Summary Table: Agent and Environment

| Component | Example in the robot task |
|---|---|
| Agent | The robot |
| Environment | The maze |
| State | The robot's current position |
| Action | Move left, right, forward or backward |
| Reward | Points received after moving |
| Goal | Reach the destination successfully |

The environment provides feedback, while the agent uses that feedback to improve its decisions.

## 8. Practical Activities

Activities 7 to 11 are numbered the same way in the Study Guide, the slides and the Test Bank. For each one, try your own answer before reading the feedback.

### Activity 7: Play the Robot: Rewards Change the Route

**Goal:** experience reward, cumulative reward, exploration versus exploitation and policy change by acting as the learning agent, using only paper, a pen and a coin.

**Preparation:** draw the 3×3 grid below. Columns are A, B, C from left to right. Rows are 1, 2, 3 from bottom to top.

```text
        A      B      C
  3   [   ]  [   ]  [ G ]      G = Goal (C3)
  2   [   ]  [Pit]  [   ]      Pit = B2 (centre)
  1   [ S ]  [   ]  [   ]      S = Start (A1)
```

**Rules**

- You can move up, down, left or right (no diagonals).
- Every move costs −1.
- Entering the Pit (B2) adds −10.
- Reaching the Goal (C3) adds +20 and ends the run.
- **No square may be entered twice in one run.** Without this rule, a robot could loop in and out of a rewarding square again and again and collect unlimited points.

**Task**

1. Predict the best route and its total reward.
2. Do 5 runs. Before each run, flip the coin: heads = exploit (repeat your best route so far), tails = explore (try a route you have not tried). On run 1, always explore. Record each run's route and total reward.
3. Change the rules: the Pit now gives **+10** instead of −10. Do 3 more runs with the same coin rule.

**Optional extension:** turn this into a small Python or Colab program. If you do, say honestly which method it uses (fixed rules, search or reinforcement learning).

**Observation:** make a table with the columns Run, Heads/Tails, Route and Total reward.

**Reflection:** how did the best route change when the reward changed? What did exploring cost you? What would have happened if you only exploited from the start?

**Hint:** count the moves first, then add the special squares.

#### Feedback

The shortest routes from A1 to C3 have 4 moves. There are six of them:

| Route (4 moves) | Passes through the Pit? | Total with Pit = −10 | Total with Pit = +10 |
|---|---|---|---|
| A1 → B1 → C1 → C2 → C3 | No | −4 + 20 = **16** | **16** |
| A1 → A2 → A3 → B3 → C3 | No | −4 + 20 = **16** | **16** |
| A1 → B1 → B2 → B3 → C3 | Yes | −4 − 10 + 20 = **6** | −4 + 10 + 20 = **26** |
| A1 → B1 → B2 → C2 → C3 | Yes | **6** | **26** |
| A1 → A2 → B2 → B3 → C3 | Yes | **6** | **26** |
| A1 → A2 → B2 → C2 → C3 | Yes | **6** | **26** |

Longer routes that never enter a square twice cost more moves and score lower than the best 4-move route, so they never win. For example, the 6-move route A1 → A2 → B2 → B1 → C1 → C2 → C3 scores 4 with the Pit at −10 and 24 with the Pit at +10.

- With the Pit at **−10**, the best score is **16**, by avoiding the Pit.
- With the Pit at **+10**, the best score is **26**, by going through the Pit.

The best policy changed because the reward changed. If you had only exploited a 16-point route, you might never have discovered the 26-point route after the change.

### Activity 8: Predict the Robot's Next Action

**Goal:** reason about feedback and how a changed reward can change a decision.

**Preparation:** use the two actions below. Assume the robot has tried each several times and currently estimates their rewards as shown.

- **Action A:** move left and receive +10 points.
- **Action B:** move right and receive −5 points.

**Task**

1. Which action should the robot prefer?
2. Now moving left repeatedly leads to a wall and a −10 penalty instead. Which action should it prefer under the new feedback?

**Observation:** record the preferred action before and after the change.

**Reflection:** why should an agent update its choice when the environment or reward information changes?

**Hint:** compare the two numbers; the higher one is better.

#### Feedback

**Answer 1.** Action A, because +10 is higher than −5. The agent tries to choose actions that produce better rewards.

**Answer 2.** Action B (−5) is now better than Action A (−10), so the robot should switch to moving right. The agent should learn from new feedback and change its choice when another action gives a better result. This simplified comparison assumes the values are comparable estimates for the current state.

### Activity 9: Immediate or Cumulative?

**Goal:** calculate cumulative reward and explain why a lower first reward can lead to a better route.

**Preparation:** use the reward table from Section 5. The robot can take two routes:

- **Route A:** closer (+5), closer (+5), hits a wall (−5), unnecessary move (−1), closer (+5), reaches the target (+20).
- **Route B:** unnecessary move (−1), closer (+5), closer (+5), closer (+5), reaches the target (+20).

**Task**

1. Which route gives the higher reward on the first step?
2. Calculate the total reward of each route. Show every addition.
3. Which route is better, and why?

**Reflection:** why is choosing the biggest immediate reward not enough?

**Hint:** add each route one step at a time.

#### Feedback

**Answer 1.** Route A (+5 on the first step, against −1 for Route B).

**Answer 2.**

- Route A: 5 + 5 − 5 − 1 + 5 + 20 = **29**
- Route B: −1 + 5 + 5 + 5 + 20 = **34**

**Answer 3.** Route B is better. Its first step has a lower immediate reward, but it avoids the wall, so its cumulative reward is higher. This is why RL aims to maximize cumulative reward, not just the next reward.

### Activity 10: Explore or Exploit?

**Goal:** explain the trade-off between trying new actions and using known successful actions.

**Preparation:** imagine a robot has found a familiar path that always gives a total of 20 points. It has never tried the path on the left.

**Task**

1. What could the robot miss if it only exploits what it already knows?
2. Why would a robot that only explores also be a bad learner?
3. Suggest a simple strategy that balances both.

**Observation:** write one possible benefit and one possible cost of each approach.

**Reflection:** why is learning a balance between discovery and using experience?

**Hint:** think of choosing where to eat: always the same place, or always a new place.

#### Feedback

**Answer 1.** It might never discover a shorter or higher-scoring path, because it never tries anything new.

**Answer 2.** It never uses what it has learned, so it keeps repeating random actions and wastes rewards.

**Answer 3.** A balanced strategy sometimes tests a new action, while usually choosing the actions with strong expected outcomes. The coin flip in Activity 7 is one simple example.

### Activity 11: Draw a State-Dependent Policy

**Goal:** show that the best action depends on the agent's current state.

**Preparation:** draw three maze positions:

- **(A)** an open path to the right;
- **(B)** a wall immediately to the right;
- **(C)** the target immediately to the left.

**Task:** for each position, choose a legal action from left, right, forward or backward, and explain your choice.

**Observation:** create a table with the columns State, Available actions, Chosen action and Reason.

**Reflection:** why would a rule such as "always move right" fail?

**Hint:** for each position, ask what is blocked and what is reachable.

#### Feedback

There is no single correct action that works in every state. One possible answer:

| State | Available actions | Chosen action | Reason |
|---|---|---|---|
| A: open path to the right | right, forward, backward, left | Right | The way is open, so moving right can make progress. |
| B: wall immediately to the right | forward, backward, left | Forward (or another open direction) | Right is blocked by the wall and would earn a penalty. |
| C: target immediately to the left | left, forward, backward, right | Left | Moving left reaches the target. |

The policy maps a state to an action. A rule such as "always move right" fails in states B and C.

### Extra Activity: Find the Mistake

This activity appears only in this Markdown file, not in the Study Guide.

A student describes Reinforcement Learning as follows:

> "The AI agent receives rewards and penalties, but it never changes its decisions. It always performs the same action."

1. What is the mistake in this explanation?
2. Explain how feedback helps the agent improve its behavior.

#### Feedback

**Answer 1.** The mistake is saying that the agent never changes its decisions. Reinforcement Learning lets an agent update its strategy based on the rewards and penalties it receives.

**Answer 2.** Feedback shows the agent which actions are useful and which should be avoided. By learning from experience, the agent can improve its future decisions and increase its expected cumulative reward.

## 9. Check Yourself

1. What is the agent in the maze example?
2. Why is a +5 immediate reward not necessarily the best decision?
3. What is the difference between exploration and exploitation?
4. Is moving left always a good action?
5. In Activity 7, why did the best route change when the Pit's reward changed from −10 to +10?

**Answers:**

1. The robot: the learner or decision-maker.
2. A later penalty or a missed goal may make the total reward lower. Decisions should consider cumulative outcomes.
3. Exploration tries unfamiliar actions to discover better choices. Exploitation uses actions already believed to work well.
4. No. Its usefulness depends on the current state, because there may be a wall or hazard to the left.
5. The policy depends on the rewards the agent receives. Once passing through the Pit gave a positive reward, a route through it earned a higher cumulative reward than the routes that avoided it.

## 10. Real-World Applications of Reinforcement Learning

Reinforcement Learning is used in different fields to help intelligent systems make better decisions through experience.

1. **Robotics:** robots can learn to walk, balance and perform tasks through repeated attempts. Example: a robot learns to walk without falling by receiving feedback about its movements and balance.
2. **Video games:** AI agents can learn strategies by playing games and receiving rewards for successful actions.
3. **Autonomous systems:** intelligent systems can improve decisions in changing environments. Example: a simulated self-driving vehicle learns to keep a safe distance from other vehicles. Real-world deployment requires rigorous safety engineering.
4. **Industrial automation:** machines can improve their operations by learning from feedback. Example: an industrial robot learns to perform a repetitive task more efficiently while reducing unnecessary movements.
5. **Resource management:** AI systems can learn how to distribute limited resources efficiently. Example: a data center system learns to allocate computing resources to reduce energy use while maintaining performance.

These are examples, not a claim that every robot, vehicle or industrial controller uses Reinforcement Learning. Real systems may use other AI methods or combinations of methods.

## 11. Conclusion

Behaviorist AI introduces the idea that intelligent behavior can improve through experience and feedback. Reinforcement Learning applies this idea by allowing agents to learn through rewards and penalties.

The agent observes its environment, takes actions, receives feedback and improves its strategy over time. An action's usefulness depends on the current state, and the best decision should consider both immediate and future rewards.

**Key takeaway:** an intelligent agent does not need to know the perfect action from the beginning. It can learn better decisions through experience, feedback and repeated interaction with its environment.

## 12. Supporting Files

| File | Use |
|---|---|
| `Robot_Maze_Activity.pdf` | Printable grid, run tables and answer key for Activity 7. |
| `Figure3_RL_Cycle.png` | Picture of the reinforcement-learning cycle from Section 3. |
| `Figure4_Robot_Maze_Grid.png` | Labelled 3×3 maze grid (A1 to C3) for Activity 7. |

See the project README for where these files are stored.

## 13. How This Topic Connects to the Other Missions

The robot-maze activity can run on a laptop (Mission 1) and be loaded through a network (Mission 2). See `connections.md` for the full connected scenario.

## 14. References

- Sutton, R. S., & Barto, A. G. (2018). *Reinforcement Learning: An Introduction* (2nd ed.). The MIT Press. http://incompleteideas.net/book/the-book-2nd.html
- Skinner, B. F. (1938). *The behavior of organisms: An experimental analysis.* Appleton-Century.
- Further reading (not needed for beginners): Sutton, R. S. (1988). Learning to predict by the methods of temporal differences. *Machine Learning, 3*, 9–44. https://doi.org/10.1007/BF00115009
