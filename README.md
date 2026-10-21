# Infrastructure Monitoring & Log Analysis

<p align="center">
  <img src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?auto=format&fit=crop&w=1600&q=80" alt="Infrastructure monitoring banner" width="100%" />
</p>

A hands-on lab focused on monitoring system health, reviewing logs, and identifying warning conditions across infrastructure and applications.

## Overview

This repository provides a practical foundation for infrastructure operations and incident investigation. It walks through the process of checking system health, reviewing logs, recognizing warning conditions, and documenting findings with clear corrective actions.

## Objectives

- Monitor CPU, memory, disk, network, and service health
- Review system and application logs for warnings, anomalies, and failures
- Correlate resource metrics with log events to identify likely root causes
- Document findings in a professional incident-report style
- Practice troubleshooting and corrective-action workflows

## Lab Tasks

### Task 1: Baseline the environment
- Check host health and uptime
- Review CPU, memory, and disk utilization
- Confirm service status and application availability

### Task 2: Monitor key system resources
- Inspect load averages, swap usage, and I/O wait
- Review filesystem capacity and inode pressure
- Validate network connectivity and latency

### Task 3: Analyze logs
- Review system logs for warnings and critical events
- Inspect application logs for exceptions, timeouts, and retries
- Search security logs for failed access attempts or blocked events

### Task 4: Correlate findings
- Link trends in resource use to log timestamps
- Determine whether the issue is a root cause or a downstream symptom
- Identify dependencies and likely failure points

### Task 5: Document the incident
- Record observations, logs, and metrics
- Summarize probable cause and impact
- Recommend corrective actions and follow-up validation

## Screenshot Gallery

The sections below are designed to showcase the sort of evidence collected during a monitoring and troubleshooting workflow.

### Monitoring dashboard view

![Resource monitor example](https://images.unsplash.com/photo-1558494949-ef010cbdcc31?auto=format&fit=crop&w=1200&q=80)

### Log review and event correlation

![Log analysis example](https://images.unsplash.com/photo-1555949963-aa79dcee981c?auto=format&fit=crop&w=1200&q=80)

### Incident response and documentation

![Incident report example](https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?auto=format&fit=crop&w=1200&q=80)

## Scope

- CPU usage and saturation
- Memory and swap pressure
- Disk capacity and I/O health
- Network reliability and latency
- Service uptime and dependency health
- Application and system logs
- Authentication and security events
- Incident documentation and remediation notes

## Workflow

1. Baseline the environment
2. Review resource data
3. Inspect logs for anomalies
4. Correlate evidence
5. Document findings
6. Recommend corrective actions

## Monitoring Checklist

See [docs/monitoring-checklist.md](docs/monitoring-checklist.md) for a structured checklist used during routine operations and troubleshooting.

## Log Analysis Guide

See [docs/log-analysis-guide.md](docs/log-analysis-guide.md) for guidance on reviewing log data and identifying operational patterns.

## Incident Report Template

See [docs/incident-report-template.md](docs/incident-report-template.md) for a formal template to document findings and remediation.

## Sample Findings

### 1. Disk pressure caused application slowdown
- High I/O wait and near-full storage
- Repeated timeout events in logs
- Root cause linked to stale logs and temporary files

### 2. Memory exhaustion triggered service restarts
- OOM warnings and repeated process restarts
- Elevated memory usage before the failure window
- Root cause likely related to workload spikes or a memory leak

### 3. Dependency failure caused HTTP 500s
- Backend errors and request timeouts
- Downstream service failure detected in logs
- Corrective action involved restoring dependency health and validating connectivity

## Final Presentation-Style Summary

This lab demonstrates how infrastructure monitoring and log analysis work together to detect, diagnose, and resolve operational issues. By reviewing system metrics and correlating them with log evidence, analysts can distinguish between symptoms and root causes, document incidents clearly, and recommend actionable remediation steps.

The overall objective is not only to identify failures, but to build a repeatable process for monitoring, investigation, and documentation. This makes the lab valuable for both technical troubleshooting and communication with stakeholders, especially when reporting service degradation, outages, or recurring infrastructure issues.

## Deliverables

- Monitoring notes
- Incident summary report
- Corrective action log
- Sample findings documentation
- Recommendations for preventive monitoring

## License

This project is intended for educational and lab use.
