# DefenderAI

> Decentralized cyber-threat detection and operational triage subnet
> proposal for Bittensor.

## Overview

DefenderAI is a Bittensor subnet concept designed to create a
competitive, decentralized market for cyber-threat detection and
operational triage.

The subnet allows specialized miners to analyze sanitized security
artifacts and return structured threat intelligence. Validators
independently test and score miner outputs using hidden benchmark data,
hard negatives, adversarial variants, evidence checks, severity
calibration, and latency measurements.

Miner performance is converted into validator weight signals, allowing
Bittensor consensus and emissions to reward miners that consistently
provide useful, accurate, robust, and actionable security intelligence.

------------------------------------------------------------------------

## The Problem

Modern security teams face:

-   High volumes of security alerts
-   Constantly changing attack patterns
-   Fragmented detection systems
-   False positives that consume analyst time
-   Detection models that can become stale or overfit
-   Difficulty evaluating different detection approaches under
    consistent conditions

Traditional centralized systems can struggle to continuously adapt to
these changing conditions.

DefenderAI approaches the problem as a competitive intelligence market
where multiple independent detection systems can compete under the same
evaluation framework.

------------------------------------------------------------------------

## The Solution

DefenderAI creates a decentralized detection network where:

1.  Validators generate or select security challenges.
2.  Miners independently analyze the supplied security evidence.
3.  Miners return structured threat assessments.
4.  Validators evaluate responses against hidden benchmarks and
    adversarial tests.
5.  Miner performance is converted into weight signals.
6.  Bittensor consensus and emissions reward useful intelligence.
7.  The strongest detection systems receive greater economic incentives
    to continue improving.

------------------------------------------------------------------------

## What Miners Do

Miners act as independent cyber-threat detection systems.

They receive sanitized security artifacts such as:

-   URLs
-   Domains
-   Network-flow features
-   File metadata
-   Authentication anomalies
-   Threat reports

A miner returns a structured assessment containing:

-   Threat label
-   Confidence
-   Supporting evidence
-   Severity
-   Recommended response

Different miners can specialize in different security domains,
including:

-   Phishing detection
-   Malware detection
-   Network-threat detection
-   Identity-threat detection

This creates a competitive environment where specialized approaches can
be evaluated against the same validator-generated challenges.

------------------------------------------------------------------------

## What Validators Do

Validators are responsible for measuring the quality of miner
intelligence.

The validator evaluation engine follows:

**Sample → Blind → Query → Stress → Score → Weight**

Validators:

-   Sample security tasks
-   Keep evaluation information hidden from miners
-   Query multiple miners
-   Test hard negatives
-   Apply adversarial mutations
-   Compare outputs against hidden benchmark labels
-   Evaluate evidence quality
-   Measure severity calibration
-   Normalize latency
-   Generate miner weight signals

This prevents the network from rewarding simple pattern matching or
static benchmark memorization.

------------------------------------------------------------------------

## Evaluation Framework

DefenderAI evaluates miners using six core dimensions:

  Metric                     Weight
  ------------------------ --------
  Detection F1                  35%
  False-positive control        20%
  Robustness                    15%
  Evidence quality              15%
  Severity calibration          10%
  Latency                        5%

### Detection F1 --- 35%

Measures the miner's ability to correctly identify threats while
balancing precision and recall.

### False-positive Control --- 20%

Measures how effectively the miner avoids incorrectly flagging benign
security artifacts as threats.

### Robustness --- 15%

Tests whether the detector remains reliable when inputs are modified
through adversarial or difficult variations.

### Evidence Quality --- 15%

Evaluates whether the miner provides useful and relevant evidence
supporting its threat assessment.

### Severity Calibration --- 10%

Measures whether the assigned severity is appropriately aligned with the
underlying threat.

### Latency --- 5%

Rewards systems that provide useful detection intelligence within
practical response times.

------------------------------------------------------------------------

## Anti-Gaming Mechanisms

DefenderAI is designed to make benchmark gaming and superficial
optimization difficult.

The proposal uses:

-   **Rotating hidden sets** --- prevents miners from permanently
    optimizing against a known dataset.
-   **Hard-negative sampling** --- tests whether miners can distinguish
    real threats from difficult benign examples.
-   **Adversarial mutations** --- evaluates performance under modified
    or manipulated inputs.
-   **Cross-validator sampling** --- reduces dependence on a single
    validator's task distribution.
-   **Evidence checks** --- ensures that outputs contain meaningful
    supporting reasoning rather than unsupported labels.
-   **Latency normalization** --- prevents raw response speed from
    unfairly dominating detection quality.

------------------------------------------------------------------------

## Why Bittensor

Bittensor provides the incentive layer required for a competitive
intelligence network.

Instead of relying on one centralized detection model, DefenderAI
enables multiple independent miners to compete on measurable security
tasks.

The network creates a feedback loop:

``` text
Miner Quality
      ↓
Validator Measurement
      ↓
Weight Signal
      ↓
Bittensor Consensus + Emissions
      ↓
Miner Incentives
      ↓
Improved Detection
```

This aligns economic incentives with useful cyber-threat intelligence.

------------------------------------------------------------------------

## Network Flow

``` text
┌──────────────────────────────┐
│  1. Sanitized Security Data  │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  2. Validator Challenge      │
│     Engine                   │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  3. Independent Miner Pool   │
│     Threat Detection         │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  4. Validator Scoring        │
│     Engine                   │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  5. Weight Signals           │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  6. Bittensor Consensus      │
│     + Emissions              │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│  7. Actionable Threat        │
│     Intelligence             │
└──────────────────────────────┘
```

------------------------------------------------------------------------

## Submission

This repository contains the interactive DefenderAI subnet proposal
submission.

The entire presentation is implemented as a standalone HTML experience.

### Main File

``` text
index.html
```

The `index.html` file contains the complete submission interface,
including:

-   Idea
-   Flowchart
-   Pitch Deck

No build system or external application setup is required to view the
submission.

------------------------------------------------------------------------

## Repository Structure

``` text
DefenderAI/
│
├── index.html
└── README.md
```

------------------------------------------------------------------------

## Running the Submission

Because the submission is a standalone HTML file, it can be opened
directly in a browser.

### Option 1 --- Open Directly

Open:

``` text
index.html
```

in any modern web browser.

### Option 2 --- Local Server

For a local development server, run:

``` bash
python -m http.server 8000
```

Then open:

``` text
http://localhost:8000
```

------------------------------------------------------------------------

## Submission Interface

The submission is organized into three primary sections.

### Idea

Explains the DefenderAI concept, problem, solution, miner and validator
roles, evaluation framework, and anti-gaming mechanisms.

### Flowchart

Visualizes the complete subnet loop from sanitized security evidence
through validator evaluation, weight signals, Bittensor consensus, and
actionable threat intelligence.

### Pitch Deck

Presents the proposal through an 8-slide narrative:

1.  DefenderAI
2.  Problem
3.  Solution
4.  Loop
5.  What Gets Rewarded
6.  Why Bittensor
7.  Execution Roadmap
8.  Thesis

------------------------------------------------------------------------

## Design

The submission uses a premium dark visual system focused on clarity and
presentation quality.

### Visual Direction

-   Dark interface
-   Violet and white primary palette
-   High-contrast typography
-   Minimal visual noise
-   Structured spacing
-   Responsive layout
-   Subtle motion
-   Interactive navigation
-   Presentation-oriented sections

The goal is to communicate a technical subnet proposal in a format that
feels closer to a polished product presentation than a conventional
documentation page.

------------------------------------------------------------------------

## Core Thesis

DefenderAI turns cyber-threat detection into a measurable decentralized
intelligence market.

Instead of asking one model to remain permanently correct, the network
creates an environment where multiple detection systems compete,
validators continuously test them against hidden and adversarial
conditions, and Bittensor incentives reward the systems that
consistently produce accurate and actionable security intelligence.

> **Better detection should earn stronger network incentives.**

------------------------------------------------------------------------

## Roadmap

### Phase 1 --- Prototype

-   Define subnet protocol
-   Establish miner response schema
-   Establish validator evaluation pipeline
-   Build initial benchmark and challenge sets

### Phase 2 --- Evaluation

-   Introduce hidden evaluation sets
-   Add hard negatives
-   Add adversarial mutations
-   Measure detection quality and calibration

### Phase 3 --- Incentive Loop

-   Convert validator measurements into miner weight signals
-   Integrate Bittensor consensus and emissions
-   Monitor miner performance over time

### Phase 4 --- Expansion

-   Add specialized detection categories
-   Expand security artifact types
-   Improve adversarial evaluation
-   Develop broader operational triage capabilities

------------------------------------------------------------------------

## Project Status

**Concept / Proposal**

This repository contains the DefenderAI subnet proposal and its
interactive presentation.

The implementation currently focuses on communicating the subnet
architecture, incentive mechanism, evaluation framework, and execution
thesis.

------------------------------------------------------------------------

## License

This repository contains a competition/proposal submission. Unless
otherwise specified by the repository owner, the contents should be
treated as proposal material rather than a production-ready security
product.
