# Introduction to Testing

# Table of Contents
1. [The Importance of Testing](#importance_of_testing)
2. [Why Developers Don't Test](#why_dev_dont_test)
3. [Testing Levels and Release Cycle](#testing_levels_release_cycle)
4. [TDD and BDD](#tdd_and_bdd)
5. [Testing Case Study](#testing_case_study)

---

<a id="importance_of_testing"></a>
# The Importance of Testing
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Summary of Video on the Importance of Testing in Software Development

## Importance of Testing
- **Quote by Scott Ambler:** "If it's worth building, it's worth testing. If it's not worth testing, why are you wasting your time working on it?"
- Testing verifies functionality and is essential to the development process.

## Automated Testing in DevOps
- Automated testing is critical for building continuous integration and deployment pipelines.
- Emphasis on client experience, requirements, and expectations before coding begins.

## Margaret Hamilton and Software Engineering
- Margaret Hamilton, an American computer scientist, led the development of NASA Apollo program's onboard guidance software.
- Credited with coining and popularizing "software engineering."
- Introduced foundational software engineering principles in the 1960s.

## Design Principles from Apollo Guidance System
1. **Use High-Level Language:** Eases calculation and reduces errors.
2. **Divide into Jobs:** Constrained by limited memory, they broke down tasks into smaller jobs.
3. **Restart on Failure:** Rather than diagnosing, restart the job.
4. **Checkpoint Good State:** Save progress at successful points for efficiency.
5. **Hardware Monitors Software:** Prevents a single job from hanging the system.
6. **Send Telemetry:** Enables real-time monitoring and problem-solving during operations.

## Relevance to Test Driven Development (TDD)
- Even with solid design principles, testing is needed to cover unforeseeable scenarios.
- The famous 1202 Program Restart alarm during Apollo 11's mission illustrates the need for thorough testing.

## Concluding Thoughts
- Testing ensures that the software functions correctly and can handle unexpected events.
- A robust system evolves through continuous testing and understanding of complex system interactions.

<!-- /MarkdownTOC -->
</details>

---

<a id="why_dev_dont_test"></a>
# Why Developers Don't Test
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Video Summary: The Importance of Testing in Software Development

## Key Problems When Developers Don't Test Code
- **Assumption of Functionality:** Developers often assume the code works without testing, leading to future complications.
- **Lack of Future-Proofing:** Without tests, future changes or contributions to the codebase can break existing functionality.
- **Underestimating System Changes:** System updates, library upgrades, and patching vulnerabilities can affect code stability.

## The Consequences of Not Testing
- **Repository Code Issues:** Without initial tests, it's challenging to identify whether new changes cause problems or if they existed before.
- **Legacy Code Uncertainty:** Returning to code after a period requires testing to understand its current state.
- **Security Vulnerabilities:** Unpatched libraries can lead to security breaches, as seen in the Equifax incident.
- **Time Mismanagement:** The time saved upfront by not writing tests is lost in extended debugging sessions later.

## Importance of Testing
- **Maintaining Code Integrity:** Tests ensure that as libraries update, the code remains functional.
- **Facilitating Refactoring:** Test cases allow for confident code refactoring and feature additions.
- **Assuring Compatibility:** Tested code is more likely to behave as expected, crucial for open-source projects and shared packages.

## Conclusion
- Testing is an essential practice for robust, resilient, and future-compatible software development. It ultimately saves time and ensures that the code behaves as expected in various scenarios and uses.

<!-- /MarkdownTOC -->
</details>

---

<a id="testing_levels_release_cycle"></a>
# Testing Levels and Release Cycle
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="tdd_and_bdd"></a>
# TDD and BDD
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---

<a id="testing_case_study"></a>
# Testing Case Study
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->


<!-- /MarkdownTOC -->
</details>

---