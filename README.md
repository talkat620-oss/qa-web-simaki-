# Simaki Website — QA Testing Project

**Author:** Tal Katriel  
**Project type:** Educational manual QA portfolio  
**Course:** 5 Stars Software Testing Course by Gal Matalon

## Project Overview

This project evaluates the functionality, usability and reliability of Simaki, a web-based restaurant ordering system supporting delivery and self-pickup. The testing process included exploratory testing, test design, structured execution, defect reporting and a release-readiness assessment.

## Tools

| Tool | Purpose |
| --- | --- |
| TestRail | Test case management, execution and traceability |
| Jira | Defect reporting and tracking |
| Apache JMeter | Basic HTTP performance checks |
| Chrome, Firefox, Edge, Brave | Browser compatibility testing |

## Testing Scope

- Registration and login
- Self-pickup and delivery workflows
- Menu navigation and product customization
- Shopping cart, pricing and checkout up to order submission
- Localization (Hebrew, English, French and Russian)
- Accessibility, usability and GUI testing
- Browser compatibility and responsive layout checks
- Basic HTTP performance testing

## Test Execution Results

| Status | Test cases | Percentage |
| --- | ---: | ---: |
| Passed | 71 | 55.0% |
| Failed | 20 | 15.5% |
| Blocked | 2 | 1.6% |
| Untested | 36 | 27.9% |
| **Total** | **129** | **100%** |

93 of 129 cases received an execution outcome, including blocked cases (72.1%).

## Defect Analysis

24 unique defects were recorded in Jira. The STR summary reports the following severity distribution:

| Severity | Count |
| --- | ---: |
| S2 — Critical | 1 |
| S3 — Major | 11 |
| S4 — Minor | 9 |
| Unclassified | 3 |
| **Total** | **24** |

Reported findings included localization inconsistencies, contradictory product customization options, accessibility issues and checkout usability problems.

## Performance Testing

The STR reports 40 sequential HTTP requests across four website languages, with an average response time of approximately 1.5 seconds and a 0% request error rate. These results describe HTTP response times, not browser rendering times or system capacity.

## Project Documentation

The System Test Report (STR) contains the testing methodology, functionality maps, business flows, TestRail execution results, Jira defect records, performance results and QA recommendations.

Additional supporting artifacts may be added as they become available.

## QA Conclusion

**Educational release-readiness recommendation: NO-GO.**

The report identifies unresolved quality concerns, incomplete test coverage and a lack of verified defect closure. Recommended next steps include defect resolution, completion of release-critical tests and regression testing.

## Limitations

Testing was conducted for educational purposes on a live website. Real payments, actual order submission, backend testing and penetration testing were outside the scope. The reported language performance comparison used low-volume requests; it does not establish load or stress capacity. The release-readiness recommendation is an educational assessment, not an operational decision by Simaki.
