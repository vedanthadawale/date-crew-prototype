# Profile Pre-Filter & Rejection Classifier

A small prototype built for The Date Crew's product & tech assessment.

## What this is

Matchmakers at The Date Crew currently share profiles based on memory and
judgment of a client's preferences. About 35% of rejected profiles are
turned down for reasons the client already stated upfront (location, age
range, deal-breakers like smoking or not wanting children) — wasted
matchmaker time and wasted client attention.

This tool demonstrates two pieces of a fix:

1. **Preference Pre-Filter & Fit Score** — checks a candidate profile
   against a client's hard deal-breakers and soft preferences *before* it's
   shared. Hard violations are blocked with a plain-language reason;
   everything else is ranked by a fit score.
2. **Rejection Reason Classifier** — takes free-text rejection feedback and
   tags it into a structured category (location, habits, family
   expectations, personality, etc.) with a rough confidence score.

## Live demo

https://vedanthadawale.github.io/date-crew-prototype/

## Running it locally

No build step or dependencies. Clone the repo and open `index.html` in a
browser, or serve it with any static file server.

## Scope and limitations

- Uses mocked client and candidate data — no real database or backend.
- The rejection classifier runs on simple keyword matching so it works
  without an API key. In a production version, this step would call the
  Claude API instead, since real feedback is messier and often mixes
  multiple reasons in one sentence.
- Built as a demonstration of the core idea for a two-week, one-person
  build, not a finished product.
