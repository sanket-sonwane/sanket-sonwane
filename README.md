# Sanket Sonwane

```
Engineer  |  AI/ML · Systems · Software · Security · Embedded/IoT
```

Final-year Computer Engineering student, building and experimenting across
artificial intelligence, systems software, computer networks, security, and
connected devices.

Most of my work sits at the seams between layers — an application or model on
top, and the operating system, network, infrastructure, or physical device
underneath it. I'm drawn to problems where the interesting part is the wiring
between those layers rather than any single component. I'm still working across
domains and building the depth to specialize in one of them.

---

## What I Work On

| Area | What it covers |
| --- | --- |
| 🤖 **Intelligent Systems** | AI/ML, LLMs, RAG, model integration, agentic systems, computer vision |
| ⚙️ **Systems & Software** | Python, backend services, Linux, operating systems, databases, APIs |
| 🔐 **Security & Networks** | Cybersecurity, SDN, network security, MEC security, traffic analysis |
| 🔌 **Embedded & IoT** | Microcontrollers, sensors, Arduino, hardware/software integration |
| 👁️ **Vision & Automation** | Photogrammetry, image processing, camera control, industrial automation |
| ☁️ **Infrastructure** | Docker, PostgreSQL, MongoDB, vector databases, cloud fundamentals |

---

## Engineering Philosophy

**Understand it end to end.** Framework knowledge has a short half-life;
fundamentals compound. I care more about knowing what sits underneath — how a
request moves through an application, a syscall, a network, and a device.

**Build the working thing, not the demo path.** Tutorials stop at the happy
path. I want the version that fails on bad input, loses the network, runs out
of disk, and gets restarted. Reliability is where engineering actually lives.

**Measure it.** Running isn't the same as working. Before claiming an
improvement, I try to define what "better" means — scheduling overhead,
detection precision and recall, inference latency — and get an actual number.

**Learn by shipping.** Most of what I understand came from building something
that didn't work, reading the source, and debugging at 2 AM. Projects are my
primary study material.

---

## Featured Projects

A curated set rather than a complete list — these cover the widest range of
what I've built so far.

### Learning to Defer — Context-Aware CPU Scheduling

*Research · Linux · Operating Systems · Machine Learning · Systems*

**Problem.** Stock schedulers decide what runs next from queue position and run
state, with very little insight into what a process is actually doing.

**What I built.** A scheduling experiment that treats *when not to run
something* as the interesting decision. Lightweight context signals — process
behaviour, memory and I/O profile, recent execution history — feed a small
model or rule set that decides whether a process should be deferred. Evaluated
against a baseline on throughput, latency, and decision overhead, because a
smarter scheduler that costs more than it saves isn't worth anything.

`[Project Link]` · `[Paper]`

### Lightweight Trust-Based Rogue Node Detection in MEC

*SDN · Network Security · Python*

**Problem.** Multi-access Edge Computing assumes the edge is cooperative. One
rogue node can misreport, hijack traffic, or quietly degrade service for
everyone behind it.

**What I built.** A Ryu-based controller that profiles edge host behaviour and
assigns trust scores from observed flow records, flagging nodes that deviate
from their established baseline. State is persisted to MongoDB so behaviour is
tracked over time rather than judged from a single snapshot.

`Python` · `Ryu` · `OpenFlow` · `Mininet` · `Open vSwitch` · `MongoDB`
`[Project Link]`

### AI-Powered Network Attack Detection

*SDN · Network Security · LLMs · Python*

**Problem.** Raw network alerts are noisy, and a rule engine on its own hands an
operator a list with no explanation attached.

**What I built.** A pipeline that pulls telemetry from the SDN layer, extracts
flow and topology features, and uses an LLM reasoning layer (Nemotron) to
correlate alerts into a small number of plausible incidents with reasoning
attached. The model interprets and explains — it isn't the only detector, and
keeping that separation deliberate is what makes the system trustworthy.

`SDN` · `Nemotron` · `Python` · `Network Security`
`[Project Link]` · `[Paper]`

### VisionMitra — Assistive Navigation

*Geospatial · Algorithms · Python*

**Problem.** Navigation assistance that still works when you have no signal.

**What I built.** Routing and stop lookup built entirely from offline
OpenStreetMap and GTFS data. KD-trees handle nearest-neighbour queries over the
map graph, A* handles routing. No API keys, no per-request cost, no dead zones.

`Python` · `OSM` · `GTFS` · `KDTree` · `A*`
`[Project Link]` · `[Demo]`

### Photogrammetry Automation

*Computer Vision · Automation · Embedded*

**Problem.** Dimensional inspection is still largely manual, and manual
measurement doesn't scale or repeat.

**What I built.** An automated capture-to-measurement pipeline: remote camera
control on a Canon EOS body, an Arduino-driven rotary stage for consistent
angles, scripted capture sequencing, then image processing to extract
dimensions. The real problem is calibration and repeatability — making the
numbers trustworthy, not just computable.

`Python` · `Computer Vision` · `Canon EOS` · `Arduino` · `Automation`
`[Project Link]`

### ClassNode — Student Management Platform

*Backend · Full-Stack · Databases*

**Problem.** Attendance, quizzes, and results end up scattered across
spreadsheets and inconsistent records.

**What I built.** A Django + React/TypeScript platform covering authentication
and role-based access, attendance, quizzes, and dashboards over PostgreSQL,
with Supabase providing auth and managed Postgres.

`Django` · `React` · `TypeScript` · `PostgreSQL` · `Supabase`
`[Project Link]` · `[Demo]`

### Autonomous Commerce Agent

*Agents · LLMs · Payment Systems · APIs*

**Problem.** Agentic systems fail unpredictably when they're also handling
money.

**What I built.** Separate buyer and merchant agents negotiating over a shared
API, with a deterministic policy layer underneath enforcing the rules — the
model proposes, the service layer decides. Inventory reservation is
concurrency-safe and releases correctly on failure, and Razorpay handles the
payment leg. Keeping probabilistic output away from irreversible state changes
was the central design decision, not an afterthought.

`LLMs` · `Agents` · `APIs` · `Razorpay` · `Payment Systems`
`[Project Link]`

### Smart Food Stall

*IoT · Computer Vision · Mobile · Backend*

**Problem.** Small vendors track sales and stock by hand, and lose money to both
bad records and spoilage.

**What I built.** A Flutter app backed by Node.js that records transactions and
tracks stock close to real time. YOLO handles vision-based item recognition,
and Bluetooth links the software side to on-site hardware — a full loop from
camera to backend to the owner's phone.

`Flutter` · `Node.js` · `YOLO` · `Bluetooth` · `IoT`
`[Project Link]`

---

## Technology Stack

Grouped by role rather than listed flat, because context makes a tool list
actually readable.

**Languages** — Python · C/C++ · JavaScript · TypeScript · SQL

**AI/ML** — PyTorch · scikit-learn · Transformers · LLMs · RAG · Computer Vision

**Backend** — Django · Node.js · REST APIs

**Systems** — Linux · Operating Systems · Networking · Docker

**Security** — Ryu · OpenFlow · Mininet · Network Security

**Embedded / IoT** — Arduino · Sensors · Hardware Interfaces

**Databases / Infrastructure** — PostgreSQL · SQLite · MongoDB · Vector
Databases · Docker

---

## Research & Engineering Interests

Areas I'm actively exploring. Not claims of expertise — just where my curiosity
is currently pointed.

- **Intelligent systems** — how much decision-making a system can delegate to a
  model before it stops being predictable or debuggable.
- **AI for systems** — putting learned models inside OS and network decision
  loops without giving up determinism.
- **Operating systems & systems engineering** — scheduling, memory behaviour,
  and reading kernel source to find out why something is actually fast.
- **Cybersecurity & network security** — trust, anomaly detection, and moving
  from dashboards toward enforcement.
- **Agentic systems** — where LLM agents genuinely belong, and where they
  emphatically do not, especially around irreversible actions.
- **Embedded & IoT** — reconciling constrained devices with software that
  assumes a reliable network.
- **Computer vision** — going past classification into measurement.
- **Human-centered intelligent systems** — assistive technology, and honestly
  evaluating whether the system helps the person using it.

---

## Currently Learning

Active gaps, currently in progress:

- **Linux internals & kernel development** — reading and writing real code
  against the kernel, not just running commands.
- **Data structures & algorithms** — closing the fundamentals gap properly.
- **Systems programming** — C/C++ and memory management past the coursework
  version.
- **AWS & cloud engineering** — deploying and operating what I've built instead
  of only running it locally.
- **Docker & deployment** — reproducible environments, CI, and actually shipping.
- **Open-source development** — reading and contributing to codebases I didn't
  write.

---

## Connect

Happy to talk about a project, a role, or anything on this page that looks worth
discussing.

- **GitHub** — [@sanket-sonwane](https://github.com/sanket-sonwane)
- **LinkedIn** — [in/sanket--sonwane](#)
- **Email** — [sanketsonwane512@gmail.com](#)
- **Portfolio** — [https://sanket--sonwane.verce.app](#)
- **Research / Publications** — [](#)
