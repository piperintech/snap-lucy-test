# Lucy Voice Bot — QA Test Harness

**A structured test program for an AI after-hours claims voice agent: 10 internal testers, 14 scripted claim scenarios, a post-call survey, and results collected automatically for analysis.**

[Live demo](https://piperintech.github.io/snap-lucy-test/) · Built for SNAP Insurance Service LLC

---

## The problem

SNAP was launching an AI voice agent ("Lucy", built by a vendor) to take first notice of loss calls after hours. Before real customers called it, we needed to know two things: **is the experience good**, and **does the data actually land correctly in the claims system?** Ad-hoc test calls couldn't answer either.

## How the test works

1. **Random assignment:** each tester selects their name and gets a scenario.
2. **A full character brief:** who they are, their role (insured, claimant, adjuster), their **mood** (frustrated, confused, rushed) and acting notes. This tests how the bot handles real behavior, not just perfect callers.
3. **Complete claim data:** policy, loss details, both vehicles and drivers, police and injury info, so every call can later be checked field by field.
4. **Post-call survey:** ease of call, bot rating, what went wrong.
5. **Automatic collection:** results post to a **Power Automate** flow, which writes them to a SharePoint list.
6. Each call is then compared against what was actually created in the claims system, to measure data accuracy.

The findings feed the [QA report dashboard](https://github.com/piperintech/lucy-test-dashboard).

## Stack

HTML, CSS, vanilla JavaScript · Power Automate HTTP trigger · SharePoint list · GitHub Pages

## Setup

Paste your own Power Automate trigger URL into `PA_URL` in `index.html` (see the setup comments above it).

> **All names, addresses, phone numbers, policy numbers, VINs and other claim details in this repo are fictional.** Tester names are anonymized.

---

Built by **Manuela Gonzalez Piper** · Product & AI · [GitHub](https://github.com/piperintech)
