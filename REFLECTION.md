# Reflection – CYA 01: Jamf MDM Implementation

## Activity Description

My department at WSU IT manages a mixed fleet of Windows and Apple devices.
Windows devices had mature, automated management through existing tooling, but
Apple devices lacked equivalent MDM coverage and were not fully compliant with
Washington State IT security requirements. I was assigned to close that gap by
implementing Jamf Pro as the Apple MDM solution — building enrollment profiles,
configuration profiles, and scoping logic from scratch.

---

## Technical and Professional Decisions

The most significant decision was determining **profile scope and granularity**.
I had to choose between broad profiles applied to all Apple devices versus
granular profiles scoped to device groups by role or location. I chose a
tiered approach: a baseline security profile for all devices (screen lock,
encryption, password policy) with additional profiles scoped to specific groups.
This mirrors how our Windows GPOs are structured and makes future maintenance
more intuitive for colleagues.

A second decision was **documentation depth**. Because I am not the only IT
staff member who may need to modify these configurations, I wrote the Confluence
article to be comprehensive enough for someone unfamiliar with Jamf — including
rationale for each profile setting, not just the steps. This added time upfront
but reduces support burden later.

---

## Contributions

I worked individually on this project. My supervisor provided the initial
requirements (compliance targets, device scope, and timeline) and reviewed
the final configuration, but the research, design, implementation, and
documentation were entirely my own work. I referenced Jamf's official
documentation, Apple Business Manager guides, and Washington State's published
IT security standards to inform every configuration decision.

---

## Quality Assessment

The core deliverable — compliant, enrolled, managed Apple devices — is
complete and functioning. Devices are actively managed in Jamf. However, I assess the current state as about 70% of the final
target. The remaining gap is **deployment automation for Splunk and Cortex XDR**.
Windows devices have this automated; Apple devices currently require additional
manual steps. If I repeated this experience, I would allocate more time earlier
to scripting and policy automation within Jamf rather than treating it as a
follow-on task — the manual steps create inconsistency risk every time a new
device is enrolled.

---

## Career Alignment

This experience directly supports both of my career goals. In the short term,
it gives me a concrete, enterprise-relevant infrastructure project to discuss
in TPM and consulting interviews, complementing my current work as a TPM Intern
at SYW.ai. In the long term, it deepened my understanding of how large
organizations enforce security policy at scale through MDM, which is foundational
knowledge for any enterprise IT or consulting career. The documentation work
also reinforced professional communication skills relevant to client-facing
technical roles.
