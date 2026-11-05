# Greater Accra daily discovery

This small Node.js program runs around 08:17 UTC daily on a standard GitHub-hosted runner. It does not use an AI model, Codex, paid runners, paid search services or private social accounts. GitHub may delay scheduled runs.

Every run includes an all-business map search plus four rotating categories across Greater Accra. Five small region tiles are checked, with at most two new companies per search and ten in total. Company identity and original map-object checks prevent duplicate entries. Published website links are checked; missing map links never establish website absence. Public business contacts, linked social profiles, establishment evidence and rule-based proposals are prepared where sources permit. Source failures are recorded. No outreach is sent.

Only collector code and AES-256-GCM encrypted state/results are public. The encryption key is held in a repository Actions secret and the private app's runtime secrets. Private app notes, edited messages and owner contact lists are never read by the runner. Logs contain aggregate counts only.

The private app imports and validates encrypted results when opened. No visitor session or private app credential is stored here. The encrypted feed index retains 90 daily batches for offline catch-up. Pause or resume the schedule under Actions → this workflow → menu. Disable the workflow to stop collection.

A manual dispatch on an already completed GMT day does not repeat source queries. Workflows never run on pull requests and third-party actions are pinned to commit SHAs. The built-in GitHub job token can write encrypted results only within this repository and expires after the run.
