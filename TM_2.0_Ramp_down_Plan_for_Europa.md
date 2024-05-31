

TM 2.0 Ramp down Plan for Europa
================================

For reference, see the [Europa Simultaneous Release](/Europa_Simultaneous_Release "Europa Simultaneous Release"), in particular the [Milestones and Release Candidates](/Europa_Simultaneous_Release#Milestones_and_Release_Candidates "Europa Simultaneous Release").

Contents
--------

*   [1 Project Plan](#Project-Plan)
*   [2 Ramp down for Europa](#Ramp-down-for-Europa)
    *   [2.1 TM 2.0 Dates](#TM-2.0-Dates)
*   [3 Ramp down for Europa SR1 (28-Sep-2007)](#Ramp-down-for-Europa-SR1-.2828-Sep-2007.29)
*   [4 Ramp down for Europa SR2 (29-Feb-2007)](#Ramp-down-for-Europa-SR2-.2829-Feb-2007.29)

Project Plan
------------

This plan is about the detailed timing and planning of the last release candidates for DSDP Target Management 2.0 ([TM 2.0 Project Plan](https://www.eclipse.org/dsdp/tm/development/tm_project_plan_2_0.html)).

Ramp down for Europa
--------------------

Typically the last week of a Milestone is for testing, and fixing only regressions and P1 or blocking defects. For milestones, the component lead (or delegate) is enough to review and approve a bug.

For M6, we plan to be functionally and API complete and the remaining Release Candidates are for (only) fixing bugs, or fixing release required items (such as version numbers, licensing, etc.).

From M6 to M7/RC0 on May 18th, we expect each component lead (or delegate) to review and verify their teams' bugs.

After the first RC is produced, other RCs will be produced, if needed, every week.

After the first RC is produced, the time for general functional improvements is long past. The following describes the types of bugs that would be appropriate:

*   A regression
*   A P1 or P2 bug, one that is blocking or critical, and some cases of major severities.
*   Documentation and PII files are exceptions to the normal PMC required review, since there is little chance of that breaking anything, though it is still expected to be complete by M6, and remaining work to be only documentation fixes (that is, no refactoring of plugins, build changes, etc, without PMC review and approval).
*   In addition to a bug meeting the above priority/severity conditions, there should be a simple, safe, well understood fix that is well isolated from effecting other components, that doesn't affect API or adopters, that has been well reviewed and well tested.
*   As each Release Candidate passes, the criteria for weighing the benefit-to-risk ratio criteria gets higher and higher, and as such requires a larger number of committers and PMC members to review.

### TM 2.0 Dates

*   May 18th, M7/RC0 produced

After the 18th, besides the normal component team review, at least 1 additional committer should also review and vote +1 on bugzilla after reviewing the bug for appropriateness and risk. Until RC1 this is optional.

*   May 25th, RC1 produced

After the 25th, besides the normal component team review, at least 1 additional committer must also review and vote +1 on bugzilla after reviewing the bug for appropriateness and risk.

*   June 5th, RC2 produced

After June 5, besides the normal component team review, at least 1 PMC member and 1 additional committer must also review and vote +1 after reviewing the bug for appropriateness and risk.

*   June 14th, RC3 produced

After the 14th, besides the normal component team review, all available committers must also review and agree in a vote after reviewing the bug for appropriateness and risk.

*   June 22

Do zip, update, site preparations

*   June 29

Release

Ramp down for Europa SR1 (28-Sep-2007)
--------------------------------------

Since we expect to see only bug fixes without functional change in the TM 2.0.1 Service Release, the testing and ramp down procedure is shortened compared to the full release. Because of that, we will also not have milestones for the Service Release, but produce weekly I-builds or M-builds every Thursday. Quality of these builds is expected to be the same or better than any milestone.

The last few weeks before the TM 2.0.1 release are reserved for testing and raising the bar for bug fixes, with appropriateness of a bug fix considered similar to the full release described above:

*   Aug 30th, RC1 produced

After Aug 30th, we'll have an intensive [TM 2.0.1 Testing](/TM_2.0.1_Testing "TM 2.0.1 Testing") pass and fork off a mainenance branch for 2.0.1. For futher fixes, besides the normal component team review, at least 1 additional committer **should** also review and vote +1 on bugzilla after reviewing the bug for appropriateness and risk. **Every fix after RC1 needs to be verified.**

*   Sep 6th, RC2 produced

After Sep 6th, besides the normal component team review, at least 1 additional committer **must** also review and vote +1 on bugzilla after reviewing the bug for appropriateness and risk. With RC2, we will **fork off the R2\_0\_maintenance branch** for further 2.0.1 work. Fixes after RC2 need to be applied to both the MAIN trunk and the R2\_0\_maintenance branch.

*   Sep 13th, RC3 produced

After Sep 13th, we do not really want to put any more bug fixes into 2.0.1 unless an emergency turns up. Time is reserved for our [DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007](/DSDP/TM/Face-to-face_Meeting_Toronto_17-Sep-2007 "DSDP/TM/Face-to-face Meeting Toronto 17-Sep-2007"), and release preparations. After Sep 13th, besides the normal component team review, at least 1 PMC member and 1 additional committer must also review and vote +1 after reviewing the bug for appropriateness and risk.

Ramp down for Europa SR2 (29-Feb-2007)
--------------------------------------

*   Feb 25th, Release bits ready for Europa (according to [Europa\_Simultaneous\_Release#Proposal 1: Schedule Change](/Europa_Simultaneous_Release#Proposal_1:_Schedule_Change "Europa Simultaneous Release"))
*   The TM release to be shipped with Europa SR2 will likely be TM 2.0.3


(Migrated from [https://wiki.eclipse.org/TM_2.0_Ramp_down_Plan_for_Europa](https://wiki.eclipse.org/TM_2.0_Ramp_down_Plan_for_Europa))