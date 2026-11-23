# Mission 1 — Computer Hardware

## Learning Outcomes

By the end of this mission, learners should be able to:

- Explain what computer hardware is.
- Identify the functions of the CPU, RAM, storage, GPU, input devices and output devices.
- Describe how hardware components work together.
- Distinguish temporary memory from long-term storage.
- Observe CPU, RAM and disk activity using Task Manager or Activity Monitor.

## 1.1 What Is Computer Hardware?

Computer hardware refers to the physical parts of a computer system.

Examples include the CPU, RAM, SSD, keyboard, mouse, monitor and GPU.

Each component has a different function, but they work together to process information and complete tasks.

## 1.2 Main Hardware Components

| Component | Function | Example |
|---|---|---|
| CPU | Executes instructions and performs calculations. | Processing game rules |
| RAM | Temporarily holds active data and instructions. It normally loses its contents without power. | Holding active game data |
| Storage | Keeps files and programs for long periods, including when power is off. | SSD or HDD |
| Input devices | Send commands or information into the computer. | Keyboard, mouse, microphone |
| Output devices | Present the computer's results. | Monitor, speakers, printer |
| GPU | Processes graphics and helps render images and video. | Rendering a 3D game scene |

### RAM vs Storage

RAM provides temporary working space for active programs.

Storage, such as an SSD or HDD, keeps saved files even after the computer is switched off.

A computer with a large SSD does not necessarily have a large amount of RAM.

## 1.3 How Hardware Components Work Together

When you open a photo:

1. The computer retrieves the file from storage.
2. The required data is loaded into RAM.
3. The CPU executes instructions to open and process the photo.
4. The GPU may help render the image.
5. The monitor displays the result.
6. The mouse can provide input when you interact with the photo.

### Simplified Hardware Diagram

```text
Input Devices
Keyboard / Mouse
       |
       v
      CPU <----> RAM
       |
       v
      GPU
       |
       v
Output Devices
    Monitor

Storage (SSD / HDD)
       |
       v
  Data loaded
    into RAM
```

This is a simplified diagram. Actual computers use multiple components and connections to transfer information.

## 1.4 Worked Example: Launching a Video Game

Imagine opening a video game on your computer.

1. **SSD:** Stores the installed game files.
2. **RAM:** Holds the game instructions and data currently being used.
3. **CPU:** Executes game rules, movement and other instructions.
4. **Keyboard:** Sends commands when the player presses a key.
5. **GPU:** Helps render the game's graphics.
6. **Monitor:** Displays the result.

| Component | Role |
|---|---|
| SSD | Stores the game files |
| RAM | Holds active game data |
| CPU | Executes instructions |
| Keyboard | Sends player commands |
| GPU | Helps render graphics |
| Monitor | Displays the game |

**Key takeaway:** Playing a game requires several hardware components to work together.

---

## Activity 1 — Power Cut! Predict What Survives

### Goal

Understand the difference between temporary memory and long-term storage.

### Scenario

Alex is writing an assignment on a laptop with 8 GB of RAM and a 256 GB SSD.

Alex writes two paragraphs without saving them. Suddenly, the laptop loses power.

### Instructions

Answer these questions before checking the explanations.

1. Will the unsaved paragraphs necessarily be available after restarting?
2. Which component retains saved files without power?
3. If Alex wants to keep many large videos, should Alex upgrade RAM or storage?

### Answers and Explanations

**1. Not necessarily.**

Unsaved information may be lost because RAM is volatile. Some applications provide automatic recovery, but this is not guaranteed.

**2. SSD storage.**

An SSD retains saved files when power is removed.

**3. Storage capacity.**

Large video files require permanent storage space. Additional RAM helps with active tasks but does not increase long-term file capacity.

### Reflection

Why do computers need both RAM and storage?

**Suggested answer:** RAM provides fast temporary working space for running applications, while storage preserves saved files and programs.

---

## Activity 2 — Label the Computer

### Goal

Identify hardware components and classify them by function.

### Instructions

Using the hardware definitions in Section 1.2, classify these eight items:

1. Microphone
2. SSD
3. RAM
4. Monitor
5. Keyboard
6. Processor
7. Printer
8. Speakers

Choose from:

- CPU
- Memory
- Storage
- Input
- Output

Then draw arrows showing how a computer records and saves a voice note.

### Answer Key

| Item | Classification |
|---|---|
| Microphone | Input |
| SSD | Storage |
| RAM | Memory |
| Monitor | Output |
| Keyboard | Input |
| Processor | CPU |
| Printer | Output |
| Speakers | Output |

### Voice Note Example

```text
Microphone (Input)
        |
        v
CPU + RAM (Processing
and temporary data)
        |
        v
SSD (Saved recording)
        |
        v
Speakers / Monitor
      (Output)
```

The microphone captures sound. The CPU processes the information while RAM temporarily holds active data. The recording can then be saved to the SSD.

### Reflection

Can one device have more than one role?

**Answer:** Yes. A touchscreen acts as an output device when displaying information and as an input device when detecting touch.

---

## Activity 3 — Live Lab: Watch Your Computer Work

### Goal

Observe how CPU, RAM and storage activity changes when an application opens and closes.

### Preparation

Use your own laptop or desktop computer.

**Windows:**

1. Press `Ctrl + Shift + Esc`.
2. Open Task Manager.
3. Select the Performance tab.

**macOS:**

1. Open Applications.
2. Select Utilities.
3. Open Activity Monitor.
4. Inspect the CPU, Memory and Disk tabs.

No additional software is required.

### Instructions

**Step 1 — Before**

With only the monitoring tool open, record:

- CPU usage (%)
- RAM currently in use
- Disk activity

**Step 2 — Prediction**

Predict which measurement will change the most when you open a large application or play a video.

**Step 3 — During**

Open the application or video.

Wait approximately 20 seconds.

Record CPU usage, RAM usage and disk activity again.

Take a screenshot of the readings.

**Step 4 — After**

Close the application and record the same three measurements.

### Observation Table

Copy this table into your worksheet and enter your actual measurements.

| Moment | CPU % | RAM used | Disk activity |
|---|---|---|---|
| Before | Record measurement | Record measurement | Record measurement |
| During | Record measurement | Record measurement | Record measurement |
| After | Record measurement | Record measurement | Record measurement |

### Questions

1. Which measurement changed the most?
2. Why does RAM usage usually increase when an application opens?
3. Why do saved files remain on the SSD after the application closes?
4. Why might the readings differ between computers?

### Expected Results and Explanations

**CPU:** Usage may increase when the computer processes instructions.

**RAM:** Usage normally increases when an application loads instructions and active data into memory.

**Disk:** Activity may increase briefly when the application loads files from storage.

**After closing:** RAM usage often decreases, but it may not return to the exact starting value because the operating system can retain cached data.

Measurements vary because of background applications, operating-system activity and the computer's specifications.

### Reflection

CPU, RAM and storage perform different tasks, but their activity is connected. Opening an application can affect all three components.

---

## 1.5 Optional Investigation: Little Man Computer

Little Man Computer (LMC) is a simplified educational model that demonstrates instruction execution and memory.

**Simulator:** https://peterhigginson.co.uk/lmc/

### Instructions

1. Open the simulator.
2. Locate the program area, memory and input/output sections.
3. Enter the following instructions:

```text
INP
OUT
HLT
```

4. Run the program using the input `7`.
5. Repeat using the input `12`.
6. Record both outputs.

### Expected Results

| Input | Expected output |
|---|---|
| 7 | 7 |
| 12 | 12 |

`INP` reads a number, `OUT` displays it, and `HLT` stops execution.

### Fallback

If the simulator cannot be accessed, trace the three instructions on paper.

The output should match the input.

### Reflection

LMC helps learners understand basic instruction processing, but it does not represent every feature of a modern CPU.

---

## 1.6 Check Yourself

**Question 1:** A laptop has a 1 TB SSD. Does that tell you how much RAM it has?

**Answer:** No. SSD capacity and RAM capacity are separate.

**Question 2:** Is a keyboard an input or output device?

**Answer:** Input. It sends commands into the computer.

**Question 3:** Why might unsaved work disappear after a power cut?

**Answer:** Unsaved information may be held in volatile RAM, which normally loses its contents without power.

**Question 4:** What does the GPU do?

**Answer:** It processes graphics and helps render images and video.

## Key Takeaway

Hardware components cooperate to perform computing tasks.

Input devices send commands, the CPU processes instructions, RAM holds active data, storage retains files, the GPU helps render graphics, and output devices present results.

## Learning Resources

- Aero AI Academy Study Guide V1.0, Mission 1, pages 5–8.
- [Little Man Computer Simulator](https://peterhigginson.co.uk/lmc/)

## Related Worksheet

Mission 1 activities are supported by `Hardware_Worksheet.pdf`. Use the worksheet to record the component labels, voice-note diagram and Task Manager observations.
