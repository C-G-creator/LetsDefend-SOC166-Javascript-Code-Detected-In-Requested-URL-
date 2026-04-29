# LetsDefend SOC166 - Javascript Code Detected In Requested URL
This repository is a case study based on my investigation of a LetsDefend alert involving JavaScript code detected in a requested URL. I put it together to show the workflow I followed from triage to final assessment, with evidence, notes, and a clean write-up that is easy to review.

## Overview

On February 26, 2022, LetsDefend generated an alert for JavaScript code detected in a requested URL against `WebServer1002` (`172.16.17.17`). I reviewed the request pattern, source reputation, and related logs to determine whether the activity was malicious and whether it succeeded.

## What this repo shows

- Alert triage.
- Source IP reputation review.
- Log review and timeline building.
- Attack classification.
- Escalation decision-making.

## Files

- `writeup/SOC166-Javascript-Code-Detected-In-Requested-URL.md` — full case study.
- `screenshots/` — evidence images used in the write-up.
- `artifacts/` — notes and supporting files.

## Main finding

The traffic was consistent with a reflected XSS attempt. The request sequence showed probing behavior, the source IP had poor reputation, and the repeated `302` responses with `0-byte` bodies suggested the payload did not execute successfully.

## How to use this repo

Open the write-up first, then review the screenshots in the order they appear in the case study. The markdown file is written so it can stand on its own inside GitHub without needing extra context.

## Notes

This repo is intentionally straightforward and written in a natural style. It is meant to read like an actual analyst project rather than a template dump.

