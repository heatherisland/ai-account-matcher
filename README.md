# AI Account Matcher

A design case study for an AI-assisted account matching and entity-resolution tool. It reconciles records that describe the same real-world account across messy, inconsistent data sources.

> Generalized overview of a tool I designed and built. It names no employer, client, or data. Happy to talk through the approach.

## The problem

Account and customer records arrive from multiple systems with no shared key: different spellings, formats, and partial fields. Matching them by hand is slow and error-prone.

## The approach

- A similarity engine scores candidate record pairs across multiple fields instead of relying on exact matches.
- AI-assisted enrichment fills gaps and raises match confidence, with results cached so repeat runs stay fast.
- A reviewer-facing UI surfaces suggested matches with their scores, so a person confirms or rejects rather than trusting the machine blindly.
- Optional templated output (for example, generated outreach copy) from confirmed matches.

## Stack

Python, a Streamlit review interface, a custom similarity and scoring engine, and LLM-assisted enrichment.
