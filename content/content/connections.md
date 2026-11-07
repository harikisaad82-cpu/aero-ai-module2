# How Hardware, Networks and Behaviorist AI Connect

**Status:** Peer-reviewed (V2.0)

## Learning Outcomes

After this section, learners should be able to:

- Explain how hardware, networks and a learning agent work together in one everyday situation.
- Use terms from all three topics correctly in one explanation.

## One Connected Scenario

You open a learning website on a laptop and start an online robot-maze activity.

| Part of the story | Topic | What happens |
|---|---|---|
| The laptop runs the browser | Hardware | Input devices send your commands. The CPU runs the browser's instructions after they are loaded from storage into RAM. The GPU helps render graphics and the monitor displays the result. |
| The page arrives from the website | Networks | DNS helps find the website's IP address. Your laptop sends packets over Wi-Fi to the router and across the Internet. The server's response comes back and the browser displays it. |
| The robot learns a route | Behaviorist AI | The agent observes its state in the environment, chooses an action and receives a reward or penalty. After each attempt it updates its policy. |

Hardware makes the laptop work. Networks carry requests and responses between the laptop and the website. Inside the maze activity, an AI agent may learn a route from rewards and penalties. The three topics describe different layers of the same experience.

## Activity: Explain the Whole Story

**Task:** explain what happens when you open a browser, visit a website and start a robot-maze simulation. Include at least **two hardware components**, **two networking concepts** and **four reinforcement-learning terms**. You may answer in a paragraph or a labelled diagram.

Try it yourself first, then compare with the sample answer below.

## Sample Answer

When I open the browser, my keyboard and mouse (input devices) send commands to the CPU, which runs the browser's instructions after they are loaded from the SSD into RAM. When I type a website name, DNS translates it into an IP address, and my laptop sends packets over Wi-Fi to the router and across the Internet. The server's response comes back, and the monitor (output) displays the page, with the GPU helping to render graphics. When I start the robot-maze simulation, the agent observes its state in the environment, chooses an action and receives a reward or penalty. After each attempt it updates its policy, and over many runs it balances exploration and exploitation to increase its cumulative reward.

## Common Misunderstandings

- **Hardware and networks are different things:** the laptop (hardware) can run without a network, but it cannot load a website without one.
- **Wi-Fi is not the Internet:** Wi-Fi connects your laptop to a local network; the Internet connects networks around the world.
- **Reinforcement learning is a computational method, not the same as behaviorist psychology:** it borrows the idea of learning from consequences.

## Key Takeaway

Hardware provides the machine, networks connect machines, and a learning agent uses feedback to improve its decisions. Real systems combine all three.

## References

See [References](References.md).
