# FinessePicks — Verified Record

Every pick made by [FinessePicks](https://finessepicks.com) is hashed (sha256) and committed to this repo.

## How verification works

1. When a pick is approved, we compute `sha256(JSON.stringify({id, team, odds, createdAt, sport, betType, line}))`
2. The hash + pick metadata are committed here as a JSON file
3. The commit timestamp proves the data existed at that time
4. Anyone can verify: check the hash against the pick data on our site

## How to verify a pick

1. Find the pick on [finessepicks.com/record](https://finessepicks.com/record)
2. Note the verification hash (first 8 chars shown on each pick)
3. Find the matching file in the `picks/` directory
4. The GitHub commit timestamp is your proof

## Timeline

- **Pre-April 2026**: All picks timestamped in our database before games started
- **April 16, 2026**: External verification launched. Existing graded picks backfilled
- **April 16, 2026+**: All new picks committed in real-time before tip-off

## Questions?

See [finessepicks.com/methodology](https://finessepicks.com/methodology)
