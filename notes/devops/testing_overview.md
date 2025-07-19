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

# Importance of Testing in Software Development

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

# The Importance of Testing in Software Development

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

# Levels of Software Testing and Release Cycle Phases

## Levels of Software Testing
- **Unit Testing:** Tests individual components for correct behavior ("happy" and "sad" paths).
- **Integration Testing:** Tests combined units to expose flaws in their interactions.
- **System Testing:** Tests the complete, integrated system against specific requirements.
- **User Acceptance Testing (UAT):** Validates the system against business requirements and for end-user acceptability.

## Phases of the Traditional Release Cycle
- **Development Environment:** Where unit testing occurs and code is stored in SCM like Git.
- **Build Environment:** For compiling code artifacts and additional unit testing.
- **Package Repository:** Storage for build artifacts such as Java jars, Python wheels, or Docker images.

### Testing Environments
- **Test Environment:** For integration testing and performance/compliance testing.
- **Staging/Pre-Production Environment:** A replica of production for system testing.
- **Production Environment:** Where acceptance testing is finalized before delivery.

## Conclusion
- Testing is a structured process with different levels, each with a specific focus.
- The release cycle moves from development to production, with testing's complexity increasing as it progresses.

<!-- /MarkdownTOC -->
</details>

---

<a id="tdd_and_bdd"></a>
# TDD and BDD
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# TDD vs BDD

## Test Driven Development (TDD)
- **Internal Focus:** TDD is concerned with the internal functioning of the system.
- **Test-First Approach:** Tests are written before the code is developed.
- **Design-Driven Tests:** Tests describe the desired behavior of code, driving its design and development.
- **Unit Testing:** TDD is primarily used for unit testing at a lower level.

## Behavior Driven Development (BDD)
- **External Focus:** BDD focuses on the system's behavior from an external viewpoint.
- **Business-Outcome Oriented:** Implements behaviors that directly contribute to business outcomes.
- **Common Syntax:** Uses a syntax understandable by all stakeholders, improving communication.
- **Integration and Acceptance Testing:** BDD is used for higher-level testing to ensure components work together correctly.

## Complementary Nature of TDD and BDD
- **Cyclic Development:** Developers cycle between TDD and BDD to cover all aspects of testing.
- **Building the Right Thing:** BDD ensures the system has the right set of capabilities and behaviors.
- **Building the Thing Right:** TDD confirms that each feature performs its intended task.

<!-- /MarkdownTOC -->
</details>

---

<a id="testing_case_study"></a>
# Testing Case Study
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# The Purpose of Test Cases and the Dangers of Untested Code

## The Purpose of Test Cases
- **Definition:** A test case is a code piece that validates the expected output for a given input.
- **Usage:** Ensures code works correctly by testing with different data types.
- **Importance:** Identifies bugs, such as incorrect handling of negative numbers, Booleans, or strings.
- **Example:** Demonstrated with a Python function `area_of_a_triangle` where test cases expose multiple bugs.

## Defensive Programming
- **Robust Code:** Requires type hinting, docstrings, and explicit checks for correct data types and value ranges.
- **Exceptions:** Raises `TypeError` and `ValueError` to handle incorrect input types and non-positive numbers, respectively.
- **Production-Ready:** The final code includes validation checks before the calculation, making it robust for production use.

## Untested Code Is Untrustworthy
- **Uncertainty:** Untested code may appear to work but can fail with unexpected inputs.
- **Best Practices:** Always write test cases for potential failures and handle them gracefully.
- **Trustworthiness:** Code is only reliable if it has been thoroughly tested and proven to work with test cases.

<!-- /MarkdownTOC -->
</details>

---
