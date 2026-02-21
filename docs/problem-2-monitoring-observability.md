# Problem 2: Improving Monitoring & Observability in Production Systems

## 1. Business Context

During production operations, the engineering team experienced multiple incidents where system degradation was detected by customers before internal teams were aware.

High latency, elevated error rates, and infrastructure saturation were impacting user experience and revenue, particularly during peak traffic periods.

Monitoring existed, but it was fragmented, inconsistent, and lacked proactive alerting thresholds.

This reactive model increased downtime and reduced customer trust.

---

## 2. Problem Statement

The organization relied heavily on reactive monitoring. Engineers were responding to incidents only after:

- Customer complaints
- Social media reports
- Revenue anomalies
- Support ticket spikes

There was no centralized observability strategy, no defined Service Level Objectives (SLOs), and no structured incident severity model.

This created:

- Increased Mean Time To Detect (MTTD)
- Increased Mean Time To Recover (MTTR)
- Operational stress
- Revenue exposure during outages

---

## 3. Root Cause Analysis

After internal review, the primary gaps identified were:

- No unified monitoring dashboard
- Alert thresholds not aligned to business SLAs
- Lack of defined critical service metrics
- No structured incident classification
- Limited traceability across distributed services

Monitoring tools existed, but visibility was incomplete and not business-aligned.

---

## 4. Engineering Strategy & Implementation

To address the issue, the team implemented a proactive monitoring framework.

### A. Defined Service Level Indicators (SLIs)

Key SLIs were identified:

- API latency
- Error rate (5xx responses)
- Infrastructure utilization (CPU, memory)
- Request throughput
- Payment success rate

These metrics connected technical performance to business impact.

---

### B. Established Service Level Objectives (SLOs)

Clear performance targets were defined:

- 99.9% API availability
- Error rate below 1%
- Latency under defined SLA thresholds

This allowed measurable reliability tracking.

---

### C. Centralized Observability Platform

All infrastructure and application logs were consolidated into a centralized dashboard using:

- AWS CloudWatch
- Prometheus & Grafana
- Structured logging pipelines

This eliminated fragmented visibility.

---

### D. Automated Alerting Framework

Alert thresholds were implemented:

- CPU utilization > 80%
- Error rate spike above baseline
- Latency exceeding SLA
- Dependency service failures

Alerts were configured to notify engineers before customer impact.

---

### E. Incident Severity Classification

A structured model was introduced:

- SEV-1: Full production outage
- SEV-2: Major degradation
- SEV-3: Minor issue

This standardized response procedures.

---

## 5. Operational Improvements

After implementation:

- Mean Time To Detect (MTTD) decreased significantly
- Incident response became structured and repeatable
- Customer-reported outages declined
- Engineering stress during incidents reduced
- Reliability metrics became measurable and trackable

Monitoring shifted from reactive firefighting to proactive reliability engineering.

---

## 6. Key Takeaways

- Monitoring must align with business impact
- Observability requires metrics, logs, and traces
- SLIs and SLOs provide measurable reliability targets
- Automated alerting reduces downtime exposure
- Structured incident response improves operational maturity

This initiative strengthened system resilience and improved production reliability.