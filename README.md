# TrendScout — README (for Reddit review)

## Purpose
TrendScout is a read-only monitoring tool that helps moderators and product teams find requests and problem reports in public Reddit communities so they can respond faster.

## What we fetch
- Endpoints: /r/{subreddit}/new.json, comment endpoints, item endpoints.
- Only public, open subreddits.

## Data minimisation & retention
- Stored fields: post_id, subreddit, timestamp, short text snippet, link.
- Deleted posts are removed from our storage within 48 hours.
- No usernames retained in analytics exports.
- Data stored for <X days> (we will set to a short window; e.g., 30 days).

## Security
- API secrets in secrets manager.
- HTTPS for all network traffic.
- Access controlled via RBAC; logs retained and auditable.

## Behaviour
- Read-only: no posting / voting / messaging.
- Rate-limited polling; we will adhere to Reddit rate limits and implement backoff.

## Contact
- Owner: u/rajigle358
- Email: rajigle358@gmail.com
- Repo / prototype: https://github.com/harshalkharabe/trendscout-reddit-monitor (private until approval; access on request)
