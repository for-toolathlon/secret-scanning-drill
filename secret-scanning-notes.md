# Secret Scanning Notes

## What secret scanning does
GitHub's secret scanning automatically scans the code in public and private repositories for leaked credentials (secret scanning for private repositories). When a secret is detected, it is alerted to repository administrators and security teams. The workflow detects credentials in commits, branches, and pull requests, and it works on open-source as well as proprietary code. Detections are reported as secret scanning alerts in the repository security tab.

## How alerts are surfaced and resolved
When secret scanning finds a credential, it creates a secret scanning alert in the repository. Each alert links to the specific file and line of code where the secret was found and shows details about the secret type. Alerts can be resolved by editing the code to remove the secret or by configuring a bypass request (delegated bypass) for specific patterns or categories. Alerts are visible in the repository's security alerts and can be tracked among issues.

## Example secret types it detects
- AWS access keys (e.g., `AKIA...`, access keys for AWS IAM users)
- GitHub personal access tokens (PATs) and GitHub OAuth tokens
- Docker registry credentials and tokens
- Kubernetes secrets and tokens
- NuGet API tokens and packages credentials
- npm/internal registry API tokens
- PostgreSQL, MySQL, and other database credentials
- Google Cloud Platform service account keys

## Documentation references
- Secret scanning overview: https://docs.github.com/en/code-security/secret-scanning
- Secret types reference: https://docs.github.com_files/en/code-security/secret-scanning/secret-types
- Secret scanning alerts: https://docs.github.com/en/code-code-security/secret-scanning/secret-scanning-alerts