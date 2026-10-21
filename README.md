# Infrastructure Monitoring & Log Analysis

## Overview

This lab focuses on monitoring system health, reviewing logs, and identifying warning conditions or service anomalies. The goal is to practice basic operational troubleshooting, correlate metrics with logs, and document findings with clear corrective actions.

## Objectives

- Monitor key system resources and services
- Review both system and application logs
- Identify warnings, anomalies, and recurring failure patterns
- Correlate events across services and infrastructure layers
- Document findings and recommended corrective actions

## Scope

- CPU usage
- Memory and swap usage
- Disk usage and inode pressure
- Network reliability and latency
- Service status and uptime
- Application logs
- System logs
- Authentication and security events
- Error and warning patterns

## Lab Workflow

1. Baseline the environment
   - Check system uptime and health
   - Review CPU, memory, disk, and network status
   - Confirm services are running as expected

2. Review monitoring data
   - Identify spikes or sustained resource pressure
   - Look for unusual process activity or failed services
   - Check for abnormal network traffic, packet loss, or latency

3. Analyze logs
   - Review system logs for warnings, crashes, failed services, and kernel errors
   - Review application logs for exceptions, timeouts, or dependency failures
   - Search for repeated patterns and error bursts

4. Correlate findings
   - Connect metrics with log events
   - Identify likely root causes rather than symptoms
   - Look for dependencies that may be failing

5. Document findings
   - Record observed anomalies
   - Explain probable cause
   - Recommend corrective actions
   - Note follow-up validation steps

## Common Monitoring Checks

### System resources
- CPU load and saturation
- Memory usage and swap activity
- Disk space and filesystem health
- I/O wait and file contention
- Network throughput and connection errors

### Services
- Process status
- Port listening status
- Service restarts / crash loops
- Dependency service health
- TLS or certificate validation issues

### Applications
- HTTP 4xx / 5xx errors
- Slow requests
- Database connection errors
- Timeouts
- Queue backlog or job failures

## Log Review Checklist

### System logs
- Kernel errors
- Memory pressure warnings
- Disk full alerts
- Service failures
- Authentication failures
- Scheduled job failures

### Application logs
- Stack traces
- Retry loops
- Failed database calls
- Timeout exceptions
- Dependency errors

### Security logs
- Failed login attempts
- Privilege escalation events
- Port scanning or unauthorized access
- Blocks or firewall denials

## Sample Log Commands

Linux / Unix examples:

```bash
top

df -h
free -m
vmstat 1
iostat
ss -tulpn
journalctl -xe
tail -f /var/log/syslog
grep -Ei "error|warn|fail|critical" /var/log/*.log
```

Application example:

```bash
tail -f /path/to/app.log
grep -Ei "ERROR|WARN|Exception|Timeout" /path/to/app.log
```

## Sample Incident Investigation Template

### Title
- Example: Web app performance degradation after midnight

### Summary
- Brief description of the issue and business impact

### Timeline
- Time when symptoms began
- Time when alerts were triggered
- Time when corrective action was taken

### Observed Symptoms
- High CPU usage
- Increased error rate
- Database latency
- Service restarts

### Evidence
- Log excerpts
- Monitoring screenshots or metrics
- Relevant alerts

### Probable Cause
- Example: disk usage exceeded 90%, causing slow writes and delayed responses

### Impact
- User-facing slowdowns
- Failed requests
- Increased support tickets

### Corrective Actions
- Increased disk capacity
- Cleaned stale logs
- Restarted dependent service
- Optimized database queries

### Validation
- Confirm normal resource use
- Recheck logs for recurrence
- Verify service metrics returned to baseline

## Sample Findings

### 1. Disk pressure caused application slowdown
- Symptoms: high latency, failed writes, growing queued jobs
- Evidence: disk usage above 95%, repeated I/O timeout events in logs
- Root cause: logs and temporary files consumed storage
- Fix: rotate logs, clear stale files, expand disk capacity if needed

### 2. Memory exhaustion triggered service restarts
- Symptoms: app crashes, process exits, elevated restart count
- Evidence: memory alarms, kernel OOM killer logs
- Root cause: memory leak or oversized workload
- Fix: investigate heap usage, optimize memory consumption, scale resources

### 3. Dependency failure caused widespread HTTP 500s
- Symptoms: user-facing errors, elevated backend latency
- Evidence: application logs show timeout to database or upstream API
- Root cause: downstream dependency unavailable
- Fix: restart dependency, check connection pool, validate network access

## Deliverables

- Monitoring notes
- Incident report
- Corrective action log
- Sample findings summary
- Recommendations for preventive monitoring

## Assessment Criteria

- Quality of system and service checks
- Accuracy of log analysis
- Ability to identify warning patterns
- Correlation between metrics and log evidence
- Clarity of incident documentation
- Practicality of corrective actions

## Suggested Final Deliverable Format

- Short summary of the environment
- List of monitored resources
- Key warning conditions identified
- Log findings and correlation notes
- Root cause analysis
- Remediation steps and follow-up recommendations

## License

This project is intended for educational and lab use.
