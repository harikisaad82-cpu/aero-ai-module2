# Module Outline: Hardware, Networks & Behaviorist AI

**Team:** Aero AI
**Version:** Final Version 3.0 (Stage 3)

## Module Overview

This module introduces three connected ideas. Hardware is the physical machine. Networks let machines exchange data. Behaviorist AI shows how a software agent can learn from rewards and penalties. Learners start with a computer, see how it communicates, and finish by seeing how an AI agent improves its decisions from feedback.

## Intended Learners

Beginners in an introductory Computer Science and AI course.

## Prerequisite Knowledge

Everyday use of computers and the internet. No programming, networking or AI background is assumed. Each topic defines its own vocabulary before using it.

## Learning Outcomes

After using this material, a beginner should be able to:

1. Identify the main hardware components and explain what each does.
2. Explain the difference between memory (RAM) and storage.
3. Explain how devices exchange data over a network using IP addresses, packets, protocols, switches and routers.
4. Trace how a website loads and find the mistake in a simple network problem.
5. Explain how an agent learns from rewards and penalties, and calculate a cumulative reward.
6. Explain exploration versus exploitation and why the current state matters.
7. Combine ideas from all three topics to explain one everyday scenario.

## Learning Sequence

The topics are meant to be read in this order, because each one builds on the one before it.

| # | Section | Main ideas | Examples and activities | File | Status |
|---|---|---|---|---|---|
| 1 | Hardware | CPU, RAM, storage, input, output, GPU | Opening a photo; launching a video game; power-cut activity with answers | `content/hardware.md` | Final |
| 2 | Networks | Network types, devices, IP addresses, protocols, DNS, bandwidth, latency | How a website loads; find-the-mistake printing activity; bandwidth vs latency check | `content/networks.md` | Final |
| 3 | Behaviorist AI | Agent, environment, state, action, reward, policy, exploration vs exploitation, cumulative reward | Robot maze with rewards; predict the next action; find the mistake; immediate or cumulative; explore or exploit | `content/behaviorist-ai.md` | Final |
| 4 | How the topics connect | One scenario that combines hardware, networks and a learning agent | "Explain the Whole Story" activity with a sample answer | `content/connections.md` | Final |
| 5 | Test Bank | True/False, multiple choice and open-ended questions, each with an answer and explanation | Covers sections 1 to 4 | `activities/test-bank.md` | Final |
| 6 | References | Sources and attribution for all sections | None | `content/References.md` | Final |

## Scope

All three core topics, the section that connects them and the Test Bank are complete. The Study Guide contains additional optional hands-on labs (Task Manager, ping and traceroute, Little Man Computer, Cisco Packet Tracer) that go beyond the activities in these Markdown files. These labs are not required for the learning outcomes above.

## Resource Mapping

This table shows where each Markdown topic is used in the other resources. The Markdown is the source. The Study Guide supports independent learning, the slides support classroom teaching, and the videos explain and demonstrate.

| Markdown file | Study Guide | Test Bank | Slides | Video Tutorials |
|---|---|---|---|---|
| `hardware.md` | Mission 1 (Activities 1 to 3, optional Little Man Computer) | Hardware questions | Hardware slides with component diagram; power-cut activity | Hardware explained in the Video Tutorials submission |
| `networks.md` | Mission 2 (Activities 4 to 6, optional Packet Tracer) | Networks questions | Networks slides with home network diagram; find-the-mistake and bandwidth vs latency activities | Networks explained in the Video Tutorials submission |
| `behaviorist-ai.md` | Mission 3 (Activities 7 to 11) | Behaviorist AI questions | Behaviorist AI slides with learning cycle diagram; robot maze activity | Behaviorist AI explained in the Video Tutorials submission |
| `connections.md` | Final Review | Questions that combine topics | Summary slides | Not selected for a separate video |
| `activities/test-bank.md` | Test Bank (Word version) | Source of questions | Next-steps slide | Not selected for video |

### Activity mapping

| Markdown activity | Study Guide activity |
|---|---|
| Hardware: power-cut activity | Activity 1: Power cut, predict what survives |
| Networks: find the mistake (printer) | Activity 4: Find the network mistake |
| Networks: bandwidth vs latency check | Activity 5: Bandwidth or latency? |
| Behaviorist AI: A, predict the next action | Activity 8: Predict the robot's next action |
| Behaviorist AI: C, immediate or cumulative | Activity 9: Immediate or cumulative? |
| Behaviorist AI: D, explore or exploit | Activity 10: Explore or exploit? |

The Study Guide also contains activities that appear only there: Activity 2 (label the computer), Activity 3 (live lab), Activity 6 (network detective), Activity 7 (play the robot on a 3x3 grid) and Activity 11 (draw a state-dependent policy).

## Key Facts Shared Across All Resources

These values and definitions are the same in the Markdown, Study Guide, Test Bank, slides and videos.

- RAM is volatile working memory. SSD and HDD are non-volatile storage. The GPU renders graphics.
- A router connects networks, a switch connects devices within a LAN, and an access point provides Wi-Fi. Wi-Fi is not the Internet.
- Ping measures latency. Traceroute lists the hops a packet takes. nslookup shows DNS information.
- Reinforcement learning is related to behaviorist psychology but is not the same thing. It is a computational method that learns from consequences.
- In the 3x3 robot maze, a route may not visit the same square twice in one run. This rule keeps the best score well defined.
