# AWS Security Essentials

A 1-day, introductory-level, **lab-heavy** course on AWS cloud security fundamentals. Built around the AWS Shared Responsibility Model, it covers identity, data protection, network security, detective controls, DDoS mitigation, and incident response — closing with a mini Well-Architected Security Review lab.

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

- Six Reveal.js teaching decks (short — lecture is about 30% of class time)
- **Seven Reveal.js lab decks** — hands-on work in the AWS web console, with analysis tasks and answer keys
- All material is single-file HTML — open in any browser, no build step
- About 70% of class time is hands-on (70/30 lab-to-lecture split); every lab is individual work

## Day Schedule

Class runs **09:00 – 16:00** (360 instructional minutes plus a 60-minute lunch). Breaks are taken inside the longer lab blocks.

| Time          | Module / Lab                                             | Min | Link |
| ------------- | -------------------------------------------------------- | --- | ---- |
| 09:00 – 09:15 | 1. Security on AWS | 15 | [01-security-on-aws.html](presentations/01-security-on-aws.html) |
| 09:15 – 09:45 | **Lab 1 — Shared Responsibility Matrix** | 30 | [lab1-shared-responsibility.html](labs/lab1-shared-responsibility.html) |
| 09:45 – 10:00 | 2. Security OF the Cloud | 15 | [02-security-of-cloud.html](presentations/02-security-of-cloud.html) |
| 10:00 – 10:25 | **Lab 2 — Compliance Evidence &amp; Guardrails** | 25 | [lab2-compliance-guardrails.html](labs/lab2-compliance-guardrails.html) |
| 10:25 – 10:40 | 3. Security IN the Cloud — Part 1a (Identity &amp; Access) | 15 | [03-security-in-cloud-part1.html](presentations/03-security-in-cloud-part1.html) |
| 10:40 – 11:20 | **Lab 3 — IAM Least Privilege Review** | 40 | [lab3-iam-least-privilege.html](labs/lab3-iam-least-privilege.html) |
| 11:20 – 11:35 | 3. Security IN the Cloud — Part 1b (Data Protection) | 15 | [03-security-in-cloud-part1.html](presentations/03-security-in-cloud-part1.html) |
| 11:35 – 12:10 | **Lab 4 — Data Protection &amp; KMS** | 35 | [lab4-data-protection.html](labs/lab4-data-protection.html) |
| 12:10 – 13:10 | *Lunch* |  |  |
| 13:10 – 13:30 | 4. Security IN the Cloud — Part 2 (Infra &amp; Detect) | 20 | [04-security-in-cloud-part2.html](presentations/04-security-in-cloud-part2.html) |
| 13:30 – 14:15 | **Lab 5 — Network Security Design** | 45 | [lab5-network-security.html](labs/lab5-network-security.html) |
| 14:15 – 14:30 | 5. Security IN the Cloud — Part 3 (DDoS &amp; IR) | 15 | [05-security-in-cloud-part3.html](presentations/05-security-in-cloud-part3.html) |
| 14:30 – 15:15 | **Lab 6 — Incident Response Tabletop** | 45 | [lab6-incident-response.html](labs/lab6-incident-response.html) |
| 15:15 – 15:25 | 6. Course Wrap-Up (WA tool, next steps) | 10 | [06-wrap-up.html](presentations/06-wrap-up.html) |
| 15:25 – 15:55 | **Lab 7 — Mini WA Security Review** | 30 | [lab7-security-wa-review.html](labs/lab7-security-wa-review.html) |
| 15:55 – 16:00 | Q&amp;A and close-out | 5 |  |

**Time split:** labs 250 min (69%) · lecture 105 min + Q&amp;A 5 min = 110 min (31%).

## Repository Layout

```
.
├── README.md
├── AWS AWS Security Essentials.docx   (source course outline)
├── presentations/
│   ├── 01-security-on-aws.html
│   ├── 02-security-of-cloud.html
│   ├── 03-security-in-cloud-part1.html
│   ├── 04-security-in-cloud-part2.html
│   ├── 05-security-in-cloud-part3.html
│   └── 06-wrap-up.html
└── labs/
    ├── lab1-shared-responsibility.html
    ├── lab2-compliance-guardrails.html
    ├── lab3-iam-least-privilege.html
    ├── lab4-data-protection.html
    ├── lab5-network-security.html
    ├── lab6-incident-response.html
    └── lab7-security-wa-review.html
```

## Running the Decks

Each presentation is a single self-contained HTML file using Reveal.js loaded from a CDN. Open it directly in a browser — no build step.

```
open presentations/01-security-on-aws.html
```

Navigation: arrow keys, `f` for fullscreen, `s` for speaker view, `?` for help.

## AWS Console Access

Every lab is performed hands-on in the **AWS web console**. All students share **one class AWS account** with administrator access, working in **us-east-1 (N. Virginia)**.

- **Naming:** the instructor assigns each student a unique ID (`stu01`, `stu02`, …). Every resource a student creates starts with that ID, and S3 bucket names also end with the account ID. Students only open, change, or delete resources that start with their own ID.
- Each lab creates what it needs and ends with a **Cleanup** slide.
- Labs avoid billable heavyweights (no EC2 instances, RDS databases, load balancers, or NAT gateways). Small charges are possible for KMS keys and Secrets Manager secrets until cleanup.

### Instructor Setup (before class)

1. **Student identities** — one sign-in per student in the class account with administrator access, plus a student-ID list (`stu01`…).
2. **Service quotas in us-east-1** — each student holds one VPC, one internet gateway, and one S3 gateway endpoint at a time (Labs 5 and 6). Make sure each quota is at least *class size + 2*:
   - *VPCs per Region* (default 5)
   - *Internet gateways per Region* (default 5)
   - *Gateway VPC endpoints per Region* (default 20)
3. **GuardDuty (Lab 6)** — GuardDuty is a single account-wide setting. Before Lab 6, in us-east-1 open GuardDuty, choose *Enable all GuardDuty features* → *Get started* → *Enable GuardDuty*, then *Settings* → *Sample findings* → *Generate sample findings* once (about 445 findings, one per type). After class, choose *Settings* → in the *Suspend GuardDuty* section choose *Disable GuardDuty* → confirm. All features, including the protection plans, are covered by the 30-day free trial; billing starts after that.
4. **Organizations** — the class account is the organization's management account. SCPs never apply to a management account, so Lab 2 has students write and validate SCPs only; they never create or attach them.
5. **No default VPC** — Labs 1 and 6 assume us-east-1 has no default VPC (the class account's was removed). If one exists, delete it before class or add 1 to the VPC and internet-gateway quotas above.

### After Class

Search each service for leftover `stu` resources. KMS keys from Lab 4 stay in *Pending deletion* for 7 days, which is expected.
