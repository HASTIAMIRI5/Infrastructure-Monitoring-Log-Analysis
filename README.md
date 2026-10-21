# Infrastructure Monitoring & Log Analysis

<p align="center">
  <img src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?auto=format&fit=crop&w=1600&q=80" alt="Infrastructure monitoring banner" width="100%" />
</p>

<div align="center">
  <img alt="Status" src="https://img.shields.io/badge/Status-Portfolio%20Project-blue" />
  <img alt="Focus" src="https://img.shields.io/badge/Focus-Infrastructure%20Monitoring%20%26%20Log%20Analysis-0A66C2" />
  <img alt="Type" src="https://img.shields.io/badge/Type-IT%20Operations%20%26%20Troubleshooting-4B8BBE" />
</div>

A formal IT operations portfolio project focused on monitoring system health, reviewing logs, and diagnosing infrastructure and application issues.

## Project Overview

This repository documents a practical monitoring and troubleshooting lab for IT administrators and support engineers. It demonstrates how to review system performance, identify anomalies, correlate resource metrics with application and system logs, and communicate findings in a structured incident report.

## Objectives

- Monitor CPU, memory, disk, and network health
- Validate the status of services and application dependencies
- Inspect system and application logs for errors, warnings, and recurring failures
- Correlate monitoring data with log evidence to determine likely root causes
- Produce professional incident documentation and remediation notes

## Core Focus Areas

- Infrastructure health monitoring
- Log review and anomaly detection
- Service and dependency validation
- Root-cause analysis and troubleshooting
- Operational documentation and reporting

## Deliverables

- Monitoring checklist
- Log analysis guide
- Incident report template
- Sample findings and corrective actions
- Portfolio-ready summary for presentations and interviews

## Documentation

- [Monitoring Checklist](docs/monitoring-checklist.md)
- [Log Analysis Guide](docs/log-analysis-guide.md)
- [Incident Report Template](docs/incident-report-template.md)
- [Lab Tasks and Objectives](docs/lab-tasks.md)
- [Final Presentation Summary](docs/final-presentation-summary.md)

## Lab Workflow

1. Baseline the environment
2. Review resource utilization
3. Inspect logs for warnings and failures
4. Correlate events across services and systems
5. Document incident evidence and recommended action
6. Validate the resolution and present findings clearly

## Example Findings

### Disk pressure and performance degradation
- High I/O wait and nearly full file systems
- Log entries indicate timeouts, failed writes, and delayed processing
- Root cause linked to storage exhaustion and stale log accumulation

### Memory exhaustion and service instability
- Repeated restarts and OOM alerts
- Elevated memory usage observed before the failure window
- Likely root cause: workload spike or inefficient memory use

### Dependency failure affecting application availability
- HTTP 500s, timeouts, and backend queue buildup
- Logs confirm downstream service or database unavailability
- Corrective actions include dependency validation and service recovery

## Final Demo Summary

This project reflects a realistic infrastructure troubleshooting workflow used in IT operations. It shows how monitoring tools and logs are combined to identify service degradation, understand the timeline of events, and document root causes in a professional and repeatable way.

The value of this lab is not only technical troubleshooting, but also clear communication: a strong monitoring and log analysis process improves uptime, reduces recovery time, and supports better operational decisions across the environment.

## Portfolio Value

This project demonstrates:
- practical troubleshooting ability
- operational awareness of system health
- monitoring and log-analysis fundamentals
- structured incident documentation skills
- readiness for IT support, systems administration, and infrastructure roles

## License

Educational and portfolio use.
