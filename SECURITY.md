# Security policy

This covers every repository in the synapsereality organisation.

## Reporting a problem

Mail ben@synapsereality.io with "security" in the subject, or use the repo's
"Report a vulnerability" button (Security tab, private vulnerability reporting).
Please don't open a public issue for it.

Tell us the repo, the version or commit, what an attacker can do and how to
reproduce it. A proof of concept helps. We reply within 3 working days, and we
agree a disclosure date with you before anything is published.

## Supported versions

Only the latest release of each tool gets security fixes. The tools are young
and each has one supported line.

## What counts

These tools read files you give them and make HTTP requests to sites you name.
Some examples we would treat as security bugs:

- a credential from `--auth` or an API key variable sent to any host but its
  own, or written to a log or report
- a crafted sitemap, robots.txt, CSV or redirect response that makes a tool
  write outside its output path or run code
- a GitHub Action input that lets a pull request from a fork run commands

A site that blocks a crawler, or an AI engine that gives a wrong answer, is not
a vulnerability in these tools.
