# Operations & Troubleshooting Runbook

## Automated Rolling Upgrades
Whenever the Backend pipeline finishes pushing container builds, instances swap gracefully. If health tests throw a non-200 check, the runner issues an immediate emergency rollback step.

## Troubleshooting Pipeline Faults
1. **Pipeline Fails on Security Audit:** Check `npm audit` or Docker image scanner logs to clean up outdated dependencies before force-pushing patches.
2. **ASG Capacity Starvation:** Refer to `monitoring/alarm-definitions.json` to monitor scale-out activities during spikes.