# Bioinformatics Workflow Bootcamp

**Free · Virtual · 3 Days · Hosted on GitHub Codespaces**

Build reproducible, portable, and scalable bioinformatics workflows from scratch — no prior computational experience required.

> **GitHub Repository:** [github.com/hossainlab/bioinfo_workflow](https://github.com/hossainlab/bioinfo_workflow)

---

## What Is This Bootcamp?

Bioinformatics Workflow Bootcamp is a free, hands-on virtual training for scientists who want to take control of their computational workflows. Over three focused sessions, you will learn the three tools that define modern bioinformatics infrastructure — and exactly how they fit together.

Whether you are a wet-lab scientist stepping into computation, a researcher exhausted by broken environments and unreproducible results, or simply someone who wants a cleaner way to work — this bootcamp is built for you.

**No prior bioinformatics experience required.**

---

## The Three-Day Journey

```
Day 1 — Pixi          Day 2 — Docker         Day 3 — Nextflow + nf-core
─────────────────     ─────────────────────   ──────────────────────────
Manage your tools     Package your tools      Orchestrate everything into
cleanly on any        into containers that    scalable, resumable,
machine. Lock exact   run identically on      community-tested pipelines.
versions. Build a     any OS, HPC, or
mini pipeline.        cloud platform.
```

| Day | Topic | Core Question Answered |
|-----|-------|------------------------|
| 1 | [Pixi — Reproducible Environments](docs/day1_pixi_tutorial.md) | How do I manage tools without breaking my system? |
| 2 | [Docker — Portable Containers](docs/day2_docker_tutorial.md) | How do I make my analysis run anywhere? |
| 3 | [Nextflow + nf-core — Workflow Orchestration](docs/day3_nextflow_tutorial.md) | How do I scale and automate a real pipeline? |

---

## What You Will Learn

### Day 1 · Pixi — Simplify Your Bioinformatics Workflow

- Why package management matters and where Conda falls short
- Install and configure Pixi with bioconda channels
- Create a project, add tools, and lock exact versions with `pixi.lock`
- Define a pipeline as named tasks in `pixi.toml` — no shell scripts needed
- Run FastQC + MultiQC on real public FASTQ data
- Share a fully reproducible environment with collaborators via Git

### Day 2 · Docker — Build Once, Run Anywhere

- Understand containers vs virtual machines and why containers win for bioinformatics
- Install Docker and pull pre-built bioinformatics images from BioContainers
- Write a Dockerfile to package BWA and Samtools with a custom alignment script
- Mount data volumes and run containerized pipelines on your own files
- Push your image to Docker Hub so anyone can reproduce your work

### Day 3 · Nextflow + nf-core — Workflow Management for Everyone

- Why shell scripts fail at scale — and what workflow managers fix
- Install Nextflow and the nf-core CLI via Pixi
- Browse 50+ community-curated nf-core pipelines
- Run `nf-core/fetchngs` to download public SRA data automatically
- Run `nf-core/rnaseq` end-to-end with a single command
- Use `-resume` to recover from failures without restarting everything
- Read MultiQC reports and copy software versions straight into your methods section
- Understand how Pixi + Docker + Nextflow form one unified stack

---

## Getting Started

### Step 1 — Star and Fork the Repository

Visit the workshop repository and click **Star** to bookmark it. You will return here for tutorials and updates throughout the bootcamp.

> **[github.com/hossainlab/bioinfo_workflow](https://github.com/hossainlab/bioinfo_workflow)**

### Step 2 — Open the Workshop Codespace

Your entire environment is pre-configured and ready in the cloud — **no installation needed on your computer.**

Click the button below to launch the workshop environment instantly in your browser:

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://opulent-pancake-6r4p4qjr9xxhrw9w.github.dev/)

> Or go to: **[opulent-pancake-6r4p4qjr9xxhrw9w.github.dev](https://opulent-pancake-6r4p4qjr9xxhrw9w.github.dev/)**

You will see VS Code open in your browser with a Linux terminal at the bottom — that is your workspace for all three days.

**First launch takes 2–3 minutes** while GitHub builds your container. After that, it opens in seconds.

### Step 3 — Verify Your Environment

Once the Codespace opens, run these checks in the terminal:

```bash
pixi --version     # Pixi package manager
docker --version   # Docker container runtime
java -version      # Java (required by Nextflow)
```

If all three return version numbers, you are fully ready. Your instructor will guide you from here.

### Step 4 — Stop Your Codespace After Each Session

A running Codespace uses your free GitHub hours. **Always stop it when you are done for the day** — your files are saved automatically.

Go to [github.com/codespaces](https://github.com/codespaces) → find your Codespace → click **Stop**.

> Stopping preserves all your work. Deleting removes everything permanently. When in doubt, stop — never delete.

### Need a GitHub Account?

Go to [github.com](https://github.com) and sign up for free — no payment details required.

> GitHub gives every free account **120 core-hours per month**. The full 3-day workshop uses roughly 6 core-hours — well within the free limit.

### Prefer a Local Setup?

Codespaces is strongly recommended for this workshop, but local options are fully supported:

| Platform | What to do |
|----------|------------|
| Linux (Ubuntu / Debian / Fedora) | Open a terminal — you are ready |
| macOS | Applications → Utilities → Terminal |
| Windows 10 / 11 | Follow the WSL2 setup guide in [Day 1](docs/day1_pixi_tutorial.md) |

---

## Repository Structure

```
bioinfo_workflow/
├── docs/
│   ├── day1_pixi_tutorial.md       Day 1 full tutorial — Pixi
│   ├── day2_docker_tutorial.md     Day 2 full tutorial — Docker
│   └── day3_nextflow_tutorial.md   Day 3 full tutorial — Nextflow + nf-core
├── .devcontainer/
│   └── devcontainer.json           Pre-configured Codespace environment
├── LICENSE
└── README.md
```

---

## Tools Covered

| Tool | What It Does | Why It Matters |
|------|-------------|----------------|
| [Pixi](https://pixi.sh) | Fast, project-based package manager | Replaces messy Conda environments with locked, portable projects |
| [Docker](https://www.docker.com) | Container runtime | Packages tools + OS into images that run identically everywhere |
| [Nextflow](https://nextflow.io) | Workflow orchestration language | Runs parallel, resumable pipelines on any compute platform |
| [nf-core](https://nf-co.re) | Community pipeline framework | 50+ publication-ready pipelines (rnaseq, sarek, chipseq, and more) |
| [BioContainers](https://biocontainers.pro) | Docker image registry for bio tools | Every BioConda tool as a ready-to-pull Docker image |

---

## Schedule at a Glance

All sessions run **9:00 PM – 11:00 PM** (2 hours per day).

### Day 1 · 21:00 – 23:00 · Pixi

| Time | Session |
|------|---------|
| 21:00 – 21:10 | Welcome, introductions, and environment check |
| 21:10 – 21:20 | GitHub Codespaces setup (recommended) |
| 21:10 – 21:25 | WSL2 setup on Windows (local alternative) |
| 21:25 – 21:40 | Basic Linux commands for everyone |
| 21:40 – 21:45 | Break |
| 21:45 – 21:55 | Why package management matters — Conda vs Pixi |
| 21:55 – 22:05 | Installing and configuring Pixi |
| 22:05 – 22:20 | Pixi core concepts — toml, lock, tasks |
| 22:20 – 22:45 | Lab: build a FastQC + MultiQC pipeline |
| 22:45 – 22:55 | Reproducibility, Git workflow, and sharing |
| 22:55 – 23:00 | Q&A and Day 1 recap |

### Day 2 · 21:00 – 23:00 · Docker

| Time | Session |
|------|---------|
| 21:00 – 21:05 | Day 1 recap |
| 21:05 – 21:25 | Containers vs VMs — Docker architecture |
| 21:25 – 21:40 | Installing Docker and running hello-world |
| 21:40 – 21:45 | Break |
| 21:45 – 22:05 | Image layers, volumes, and essential commands |
| 22:05 – 22:30 | Lab: write a Dockerfile for NGS alignment |
| 22:30 – 22:50 | Lab: pull and run pre-built BioContainers |
| 22:50 – 23:00 | Q&A and Day 2 recap |

### Day 3 · 21:00 – 23:00 · Nextflow + nf-core

| Time | Session |
|------|---------|
| 21:00 – 21:05 | Days 1–2 recap |
| 21:05 – 21:20 | Workflow management — the problem Nextflow solves |
| 21:20 – 21:35 | Installing Nextflow and nf-core via Pixi |
| 21:35 – 21:40 | Break |
| 21:40 – 21:50 | Browsing nf-core pipelines |
| 21:50 – 22:25 | Lab: run nf-core/fetchngs and nf-core/rnaseq |
| 22:25 – 22:40 | Understanding outputs and MultiQC reports |
| 22:40 – 22:50 | The Pixi + Docker + Nextflow stack explained |
| 22:50 – 23:00 | Resources, next steps, and Q&A |

---

## By the End of This Bootcamp You Will Have

- A working Pixi project with locked, reproducible tool environments
- A custom Docker image containing bioinformatics tools you built yourself
- A complete nf-core pipeline run with real data and a publication-ready MultiQC report
- A clear mental model of how Pixi, Docker, and Nextflow each solve a distinct problem
- The confidence to troubleshoot, extend, and apply these tools to your own research

---

## Community Resources

| Resource | Purpose |
|----------|---------|
| [Workshop Repository](https://github.com/hossainlab/bioinfo_workflow) | Tutorials, code, and all workshop materials |
| [nf-core website](https://nf-co.re) | Pipeline documentation and tutorials |
| [nf-core Slack](https://nf-co.re/join) | Ask questions — one of the most welcoming communities in bioinformatics |
| [Nextflow documentation](https://nextflow.io/docs) | Full language and executor reference |
| [Seqera Platform](https://seqera.io) | Monitor and manage pipeline runs at scale |
| [BioContainers](https://biocontainers.pro) | Browse Docker images for thousands of bio tools |
| [Pixi documentation](https://pixi.sh) | Pixi command reference and guides |

---

## License

This workshop material is released under the [MIT License](LICENSE). You are free to use, adapt, and redistribute it with attribution.

---

*Seats are free. Your workflow transformation is priceless.*
