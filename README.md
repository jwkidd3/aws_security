# AWS Security Essentials

A 1-day, introductory-level, **lab-heavy** course on AWS cloud security fundamentals. Built around the AWS Shared Responsibility Model, it covers identity, data protection, network security, detective controls, DDoS mitigation, and incident response — with a capstone mini Well-Architected Security Review.

## Audience

Security and IT professionals interested in cloud-security practices — including security professionals with minimal to no prior AWS experience.

## Prerequisites

- Working knowledge of IT security practices and infrastructure concepts
- Familiarity with cloud-computing concepts

## Learning Objectives

By the end of the day participants will be able to:

1. Explain the security benefits and responsibilities of using the AWS Cloud
2. Describe AWS access-control and management features
3. Explain methods for encrypting data in transit and at rest in AWS
4. Describe how to secure network access to AWS resources
5. Identify AWS services for monitoring and incident response
6. Run a mini Well-Architected Security review and turn findings into a roadmap

## Format

- Six Reveal.js teaching decks (6–10 slides each)
- **Six Reveal.js lab decks** — paper-based analysis paired with short, read-only AWS Console navigation
- All material is single-file HTML — open in any browser, no build step
- About 50% of class time is hands-on

## Day Schedule

Class runs **09:00 – 16:00**. Instructor calls breaks as needed.

| Time          | Module / Lab                                          | Link                                                                             |
| ------------- | ----------------------------------------------------- | -------------------------------------------------------------------------------- |
| 09:00 – 09:30 | 1. Security on AWS                                    | [01-security-on-aws.html](presentations/01-security-on-aws.html)                 |
| 09:30 – 10:00 | **Lab 1 — Shared Responsibility Matrix**              | [lab1-shared-responsibility.html](labs/lab1-shared-responsibility.html)          |
| 10:00 – 10:20 | 2. Security OF the Cloud                              | [02-security-of-cloud.html](presentations/02-security-of-cloud.html)             |
| 10:20 – 10:50 | 3. Security IN the Cloud — Part 1 (Identity &amp; Data) | [03-security-in-cloud-part1.html](presentations/03-security-in-cloud-part1.html) |
| 10:50 – 11:25 | **Lab 2 — IAM Least Privilege Review**                | [lab2-iam-least-privilege.html](labs/lab2-iam-least-privilege.html)              |
| 11:25 – 11:55 | **Lab 3 — Data Protection &amp; KMS**                 | [lab3-data-protection.html](labs/lab3-data-protection.html)                      |
| 11:55 – 12:55 | *Lunch*                                               |                                                                                  |
| 12:55 – 13:25 | 4. Security IN the Cloud — Part 2 (Infra &amp; Detect) | [04-security-in-cloud-part2.html](presentations/04-security-in-cloud-part2.html) |
| 13:25 – 14:00 | **Lab 4 — Network Security Design**                   | [lab4-network-security.html](labs/lab4-network-security.html)                    |
| 14:00 – 14:30 | 5. Security IN the Cloud — Part 3 (DDoS &amp; IR)     | [05-security-in-cloud-part3.html](presentations/05-security-in-cloud-part3.html) |
| 14:30 – 15:00 | **Lab 5 — Incident Response Tabletop**                | [lab5-incident-response.html](labs/lab5-incident-response.html)                  |
| 15:00 – 15:20 | 6. Course Wrap-Up (WA tool, next steps)               | [06-wrap-up.html](presentations/06-wrap-up.html)                                 |
| 15:20 – 15:45 | **Lab 6 — Mini WA Security Review (Capstone)**        | [lab6-security-wa-review.html](labs/lab6-security-wa-review.html)                |
| 15:45 – 16:00 | Q&amp;A and close-out                                 |                                                                                  |

## Repository Layout

```
.
├── README.md
├── presentations/
│   ├── 01-security-on-aws.html
│   ├── 02-security-of-cloud.html
│   ├── 03-security-in-cloud-part1.html
│   ├── 04-security-in-cloud-part2.html
│   ├── 05-security-in-cloud-part3.html
│   └── 06-wrap-up.html
└── labs/
    ├── lab1-shared-responsibility.html
    ├── lab2-iam-least-privilege.html
    ├── lab3-data-protection.html
    ├── lab4-network-security.html
    ├── lab5-incident-response.html
    └── lab6-security-wa-review.html
```

## Running the Decks

Each presentation is a single self-contained HTML file using Reveal.js loaded from a CDN. Open it directly in a browser — no build step.

```
open presentations/01-security-on-aws.html
```

Navigation: arrow keys, `f` for fullscreen, `s` for speaker view, `?` for help.

## AWS Console Access

Students log into a shared class AWS account for navigation only — **no creates or edits**. Every lab includes an explicit read-only exploration section.
