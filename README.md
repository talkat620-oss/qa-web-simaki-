# Simaki Website — Performance Testing

**Author:** Tal Katriel  
**Project:** 5 Stars Software Testing Course — Gal Matalon  
**Tool:** Apache JMeter 5.6.3

## Overview

Basic performance testing of selected public pages of the Simaki restaurant ordering website. The objective was to evaluate HTTP response times, response consistency and successful HTTP responses under controlled, low-volume conditions.

## Test Configuration

| Parameter | Configuration |
|---|---|
| Tool | Apache JMeter 5.6.3 |
| Protocol | HTTPS |
| Request method | HTTP GET |
| Environment | Live production website |
| Traffic model | Single-user / low-volume |
| Request delay | Controlled, where appropriate |

## Testing Scope

- Homepage and menu HTTP response times
- Response consistency across sequential GET requests
- HTTP response code validation
- Latency, elapsed time and response size (identified metrics)
- Homepage response time comparison across four supported languages

## Language Performance Results

Ten sequential requests per language were reported in the System Test Report (STR).

| Language | Samples | Average (ms) | Minimum (ms) | Maximum (ms) | Error rate |
|---|---:|---:|---:|---:|---:|
| Hebrew | 10 | 1,726 | 588 | 4,275 | 0.00% |
| English | 10 | 1,436 | 530 | 2,515 | 0.00% |
| French | 10 | 1,512 | 549 | 3,714 | 0.00% |
| Russian | 10 | 1,327 | 605 | 2,155 | 0.00% |
| **Overall** | **40** | **1,500** | **530** | **4,275** | **0.00%** |

## Key Findings

- All 40 requests in the language comparison completed without reported errors.
- Overall average HTTP response time was approximately 1.5 seconds.
- Russian had the lowest observed average response time (1,327 ms).
- Hebrew had the highest observed average (1,726 ms) and maximum (4,275 ms).

## Conclusion and Limitations

The results provide a basic HTTP performance baseline under the reported test conditions. They do not represent full browser rendering times or establish production capacity under concurrent traffic. No performance acceptance threshold is documented for the language comparison.

The STR describes load and stress testing as excluded. However, test case T76 is marked Passed and refers to 50 concurrent users. This discrepancy requires verification against the original JMeter test plan and execution logs; no concurrency or capacity conclusions are drawn here.

## Supporting Evidence

The results above are transcribed from the STR, sections 4.1–4.5 (pages 8–9). Original JMeter artifacts are not included in this README and should be added when available:

- JMeter test plan (`.jmx`)
- Raw execution results (`.jtl` or `.csv`)
- Summary Report and Aggregate Report exports
- Sanitized screenshots of test configuration and results

## Project Context

This is an educational QA portfolio project, not an official performance certification of the Simaki website. Any further testing against the live website should be authorized and avoid disrupting normal operations.
