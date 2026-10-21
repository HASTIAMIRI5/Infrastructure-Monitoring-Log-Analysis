# Monitoring Checklist

Use this checklist during routine infrastructure review and incident investigation.

## Environment Health
- [ ] Check system uptime
- [ ] Verify CPU usage and load average
- [ ] Verify memory usage and swap status
- [ ] Check disk usage and free space
- [ ] Review filesystem health and inode usage
- [ ] Review network connectivity and latency

## Services
- [ ] Confirm critical services are running
- [ ] Check listening ports and active connections
- [ ] Review restart counts and crash loops
- [ ] Validate dependencies and upstream connectivity
- [ ] Confirm certificate and TLS health where applicable

## Logs
- [ ] Review system logs for warnings and failures
- [ ] Review application logs for exceptions and timeouts
- [ ] Check authentication and authorization logs
- [ ] Search for repeated issues or recurrence windows

## Response Actions
- [ ] Record symptoms and affected systems
- [ ] Identify likely cause
- [ ] Note mitigation steps taken
- [ ] Validate system stability after action

## Notes
Document the exact timestamps, affected services, and evidence observed during the check.
