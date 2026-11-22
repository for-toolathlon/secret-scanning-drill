# Secret Scanning Training Notes

## What secret scanning does
Secret scanning automatically scans code and other repository content for leaked credentials and secret patterns. It works on every push and on pull requests, analyzing files in tracked languages. When it finds something that matches a known secret format (like an API key, token, password, or private key), it creates an alert in the repository's security tab (e.g., GitHub's security overview). The alerts are linked to an advisory, labeled, and can be resolved by the repository owner or team member.

## How alerts are surfaced and resolved
Alerts are surfaced as "secret scanning alerts" on the security tab of the repository. Each alert is a single line indicating a matched pattern, its likely location, and how to remediate. Alerts can be resolved. By default, resolved alerts with high confidence from trusted sources can be auto-dismissed, and they can also be manually dismissed by a site admin. Review and resolve alerts individually, or request delegated dismissal for teams.

## Example secret types scanned
- API keys (e.g., GitHub tokens, personal access tokens)
- SSH keys (including private keys)
- Database credentials (passwords, connection strings)
- AWS credentials (access keys, secret keys)
- Other keys and tokens (e.g., Slack, Google API keys)

Reference: GitHub documentation — Secret scanning (https://docs.github.com/en/code-security/secret-scanning) and Supported secret scanning patterns (https://docs.github.com/en/code-security/secret-scanning/secret-scanning-patterns)
