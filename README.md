# Infrastructure Monitoring & Log Analysis

A practical lab focused on monitoring system health, reviewing logs, and identifying anomalies across infrastructure and applications.

## Overview

This repository is designed for hands-on practice in infrastructure monitoring and log analysis. It demonstrates how to baseline system health, identify warning conditions, review service and application logs, and document findings with corrective actions.

## Objectives

- Monitor key system resources and services
- Review system and application logs
- Detect warnings, anomalies, and failure patterns
- Correlate monitoring data with log evidence
- Document findings and recommended actions

## Lab Scope

- CPU, memory, and disk utilization
- I/O bottlenecks and resource saturation
- Network latency, packet loss, and connection issues
- Service uptime and dependency health
- Application and system event logs
- Security and authentication events
- Incident documentation and remediation

## Monitoring Checklist

### System Resources
- CPU usage and load averages
- Memory utilization and swap activity
- Disk usage and inode pressure
- I/O wait and read/write contention
- Network throughput and errors

### Services and Applications
- Process state and crash loops
- Port availability and listening services
- Restart counts and uptime
- Dependency service health
- Application error rates and failed requests

## Log Analysis Workflow

1. Baseline the environment
   - Confirm the system is healthy and services are running
   - Review resource utilization trends
   - Identify any recent changes or unusual activity

2. Review logs for warning patterns
   - Search for errors, warnings, and critical events
   - Check service restarts, failed jobs, and repeated exceptions
   - Look for authentication failures or denied access attempts

3. Correlate events
   - Connect spikes in CPU, memory, or disk usage with log timestamps
   - Match application errors to dependency failures or network issues
   - Determine whether the issue is a symptom or root cause

4. Document findings
   - Note the evidence and impact
   - Explain the likely cause
   - Record corrective actions and validation steps

## Sample Log Commands

```bash
top
free -m
df -h
vmstat 1
iostat
ss -tulpn
journalctl -xe
tail -f /var/log/syslog
grep -Ei "error|warn|fail|critical" /var/log/*.log
```

Application log review:

```bash
tail -f /path/to/app.log
grep -Ei "ERROR|WARN|Exception|Timeout" /path/to/app.log
```

## Example Incident Template

### Title
Example: Database latency caused elevated HTTP 500 errors

### Summary
A brief explanation of the issue, scope, and impact.

### Timeline
- Start time
- Alert trigger time
- Mitigation time
- Resolution time

### Symptoms
- High CPU or memory usage
- Slow requests
- Queue backlog
- Service restarts

### Evidence
- Log snippets
- Monitoring screenshots
- Alerts and timestamps

### Probable Cause
Example: Disk pressure and slow database queries caused request timeouts.

### Corrective Actions
- Restarted the affected service
- Cleared stale logs
- Increased capacity
- Tuned database query performance

### Validation
- Confirm resource metrics returned to baseline
- Recheck error rate and logs
- Verify application uptime and user impact

## Sample Findings

### 1. Disk Pressure Caused Slow Application Response
- Signs: high I/O wait, filesystem near capacity, growing queued jobs
- Evidence: log entries show I/O timeout and failed writes
- Root cause: stale logs and temporary files depleted available storage
- Fix: rotate logs, clean temporary files, expand storage if required

### 2. Memory Exhaustion Triggered Service Restarts
- Signs: elevated memory usage, OOM messages, crash loops
- Evidence: kernel logs indicate out-of-memory events
- Root cause: memory leak or workload spikes
- Fix: investigate memory growth, monitor service limits, scale resources

### 3. Dependency Failure Caused Widespread HTTP 500s
- Signs: application errors, backend latency, failed upstream calls
- Evidence: application logs show timeout to database or API dependency
- Root cause: dependent service unavailable or overloaded
- Fix: validate dependency health, restart service if needed, review connection limits

## Deliverables

- Monitoring notes
- Incident summary
- Corrective action log
- Sample findings report
- Recommendations for preventive monitoring

## Documentation

- [Monitoring Checklist](docs/monitoring-checklist.md)
- [Log Analysis Guide](docs/log-analysis-guide.md)
- [Incident Report Template](docs/incident-report-template.md)

## License

This project is intended for educational and lab use.
