# Behavior Driven Development

# Table of Contents
1. [What is Behavior Driven Development](#bdd_overview)
2. [Benefits of BDD](#bdd_benefits)
3. [BDD Workflow and Gherkin Syntax](#bdd_workflow_and_gherkin_syntax)
4. [Example of BDD](#bdd_example)
5. [Tools for Behavior Driven Development](#bdd_tools)
6. [Overview of Behave](#overview_of_behave)
7. [Environment Setup](#environment_setup)
8. [Writing Feature Files](#writing_feature_files)
9. [Selenium](#selenium)
10. [Writing Step Files](#writing_step_files)
11. [Loading Test Data with Behave](#loading_test_data_with_behave)

---

<a id="bdd_overview"></a>
# What is Behavior Driven Development
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Behavior-Driven Development (BDD)

## Overview of BDD
- BDD focuses on the system’s external behavior, not internal workings.
- Suitable for integration testing, verifying components work together.
- It emphasizes an "outside-in" approach, prioritizing behaviors impacting business outcomes.
- BDD uses a single syntax for clarity and communication among team members.

## Difference Between BDD and TDD
- **TDD (Test-Driven Development):** Tests the internal functions of a system. Concerned with return codes, data formats, etc. Used for unit testing.
- **BDD (Behavior-Driven Development):** Higher-level testing from the user's perspective. Tests the system's behavior without concern for the internal API calls. It's applicable to integration, system, and acceptance testing levels.

## Example of BDD in Practice
- Virtual shopping cart behavior: Adding or removing items and ensuring the cart reflects these changes.

## Levels of Software Testing
1. **Unit Testing:** Testing individual components for correct functionality.
2. **Integration Testing:** Testing combined units to expose faults in interactions.
3. **System Testing:** End-to-end testing of the complete system against high-level requirements.
4. **User Acceptance Testing:** Users test the system for acceptability.

## BDD in the Software Testing Process
- Typically performed during integration, system, and acceptance testing stages.
- Allows for testing the behavior of a more complete running system.

## Key Takeaways
- BDD is ideal for ensuring the system behaves as users expect.
- BDD fits into higher-level testing phases where behavior observation is possible.

<!-- /MarkdownTOC -->
</details>

---

<a id="bdd_benefits"></a>
# Benefits of BDD
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Benefits of Behavior-Driven Development for Automated Testing

## Key Benefits of BDD
- **Unified Language:** BDD allows for describing behaviors in a single, accessible syntax that domain experts, testers, developers, and stakeholders can understand.
- **Improved Communication:** It facilitates clearer communication among all parties involved in the development process.
- **Natural Syntax:** BDD uses a natural language syntax, particularly given-when-then, which is easier to learn and approach than traditional TDD tools.
- **Gherkin Syntax:** The most common BDD syntax is Gherkin, named after the BDD tool Cucumber, enhancing readability and stakeholder engagement.

## Advantages of BDD Specifications
- **Behavior Description:** Specifies how a system should behave in different scenarios, providing clarity on expected functionality.
- **Documentation Generation:** BDD tools can automatically generate technical and user documentation from specifications, ensuring documentation is always up-to-date.
- **Test Generation:** Allows for automatic creation of tests from specifications, proving that the delivered behavior matches what stakeholders require.

<!-- /MarkdownTOC -->
</details>

---

<a id="bdd_workflow_and_gherkin_syntax"></a>
# BDD Workflow and Gherkin Syntax
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Behavior-Driven Development Workflow and Gherkin Syntax

## BDD Workflow
- Collaboratively explore the problem domain and create scenarios in Gherkin syntax.
- Use a BDD test runner like Behave to automate these scenarios as test cases.
- Behave will identify missing test steps needed to prove system behavior.
- Develop and refine these steps, receiving constant feedback on implementation.
- Maintain a living document that acts as both specification and tests, checked into source control and used in every test run.

## Gherkin Syntax Keywords
- **Given:** Defines preconditions to set up the system state before testing (e.g., "Given I have two items in my shopping cart").
- **When:** Describes an event or action taken (e.g., "When I remove an item from my cart").
- **Then:** Specifies the expected outcome to be verified (e.g., "Then I should only have one item in my shopping cart").
- **And:** Continues a series of similar steps for readability, taking the meaning of the previous Given, When, or Then (e.g., "Given this, And that").
- **But:** Introduces a contrasting step to what should not occur for readability (e.g., "But that is not observed").

<!-- /MarkdownTOC -->
</details>

---

<a id="bdd_example"></a>
# Example of BDD
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# BDD Specifications, Features, and Scenarios

## BDD Specification Components
- **Features**: Represent user stories. Can be multiple in a specification. Typically placed in individual specification files.
- **Scenarios**: Concrete examples describing single behaviors of a feature, written in Given, When, Then syntax to formulate complete test cases.

## Building a BDD Specification
- Start with a **Feature** keyword, followed by a title that clearly expresses the feature scope.
- Write a user story using agile user-story syntax: “As a [role], I want [functionality], so that [benefit].”
- Include multiple **Scenarios** within each feature to describe various behaviors.
- Scenarios are detailed with Gherkin syntax steps:
  - **Given**: Preconditions or initial state setup.
  - **When**: Event or action taken by the user.
  - **Then**: Expected outcome or behavior observed.

## Example BDD Specification
- **Feature**: "Returns go to stock" — handling item returns to stock.
- **Scenario 1**: "Refunded items should be returned to stock."
  - Given a customer previously bought a black sweater.
  - And I have three black sweaters in stock.
  - When they return the black sweater for a refund.
  - Then I should have four black sweaters in stock.

- **Scenario 2**: "Exchanged items should be returned to stock."
  - Given a customer previously bought a blue shirt.
  - And I have two blue shirts in stock.
  - And I have three black shirts in stock.
  - When they return a blue shirt for a replacement in black.
  - Then I should have three blue shirts in stock.
  - And I should have two black shirts in stock.

<!-- /MarkdownTOC -->
</details>

---

<a id="bdd_tools"></a>
# Tools for Behavior Driven Development
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Features of BDD Tools

BDD tools offer support for a variety of programming languages and have different features. When selecting a BDD tool, consider the programming language of your project and the specification syntax the tool supports.

## Common BDD Tools

### Cucumber
- One of the oldest BDD tools.
- Available in free open-source and paid versions.
- Supports Ruby, Java, .NET, and web applications in any language.
- Utilizes Gherkin syntax for specifications.
- Specifications written in plain text format for version control.

### Behave
- The tool used for Python projects.
- Recommended by Cucumber for Python BDD.
- Supports plain text feature files and Python-written steps.
- Offers environment setup and test fixtures for control over the test environment.

### JBehave
- The Java version of Behave, catering to Java framework projects.

### Concordion
- An open-source tool for Java.
- Specifications are written using natural language paragraphs.
- Ported to other languages like C#, Python, and Ruby.
- Does not use Gherkin syntax.

## Selection Criteria for a BDD Tool
- **Programming Language Compatibility**: Choose a tool that supports the language of your project.
- **Specification Syntax**: Prefer tools that support Gherkin for its ease of use and understandability by both stakeholders and developers.
- **Features**: Look for tools with powerful features that suit your project needs.

<!-- /MarkdownTOC -->
</details>

---

<a id="overview_of_behave"></a>
# Overview of Behave
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Running Behave with BDD

This section provides an overview of how the Behave tool operates, including the required file structure and execution of step functions.

## Required File Structure for Behave

- **Features Folder**: Behave requires a top-level folder named `features`.
  - Inside this folder, `.feature` files contain the scenarios and are processed by Behave.
  - Any naming convention works for these files.

- **Steps Subfolder**: 
  - Within the `features` folder, there's a subfolder called `steps` that contains Python files.
  - These Python files hold the steps that match the Gherkin statements in the `.feature` files.
  - The naming of these Python files is flexible, but using `_steps` in the name is common.

- **Generic Steps File**: 
  - A file named `web_steps.py` is recommended for generic steps that manipulate the web interface.
  - Additional Python files for steps can be stored in the steps folder.

- **No Direct Correlation**: 
  - The number of feature files does not need to match the number of steps files.
  - The Python steps should collectively cover all statements in the feature files.

## Running Behave

- Run the Behave tool from within the parent directory of the `features` folder.
- Behave reads each `.feature` file, finds matching Python steps in the `steps` files, and executes the functions.

## Sample Steps Files and Matching

- **Feature File**: Contains scenarios developed with stakeholders.
- **Steps File**: Contains Python statements that Behave matches to the feature file.
- **Function Names**: Behave ignores the names of the functions in the steps file, focusing instead on the decorators.
- **Process Flow**:
  - Behave scans the feature file for scenarios.
  - Matches each step's keyword and text string with a corresponding pair in the Python steps file.
  - Executes the matching function.
- The steps in the steps file do not need to be in any particular order.

```markdown
In this video, you learned that setting up the correct folder structure is crucial for Behave to function properly, and how Behave uses the code in `.feature` and steps files to execute tests.
```

<!-- /MarkdownTOC -->
</details>

---

<a id="environment_setup"></a>
# Environment Setup
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Test Fixtures in Behave

The section provides a detailed explanation of the test fixtures available in Behave and the process for setting up a testing environment using these fixtures.

## Behave Test Fixtures

Behave offers a range of test fixtures for setting up and tearing down the testing environment at various stages of test execution:

- `before_all` and `after_all`: Execute once before and after all features, ideal for setting up drivers like Selenium and establishing context for all steps.
- `before_feature` and `after_feature`: Run before and after each feature, useful for setting up a clean environment for every feature.
- `before_scenario` and `after_scenario`: Execute before and after each scenario, allowing granular control over the execution environment of each scenario.
- `before_step` and `after_step`: Run before and after every step, offering control at a very detailed level.
- `before_tag` and `after_tag`: Execute before and after a tagged section of the feature file, providing environment control based on tags.

## Setting Up the Behave Environment

- Behave requires an `environment.py` file where you declare your test fixtures.
- Global variables from the environment can be declared and used in test fixtures.
- The `context` object is passed to every step in the test suite, making it the carrier for shared data across steps.

### Example of `environment.py`

- Import necessary modules such as `getenv` from `os` and `WebDriver` from `selenium`.
- Declare global variables to be accessed by the test steps, like `wait_seconds` and `Base_URL`.
- Define `before_all` to set up the initial environment for running the BDD tests, which may include initializing the WebDriver and setting wait times.
- Define `after_all` to close down the web browser after all tests, ensuring resources are released properly.

### In summary, Behave's test fixtures are powerful tools for managing the testing environment throughout the BDD process. The `environment.py` file is the central place to declare and define these fixtures, ensuring a controlled environment for automated tests.

<!-- /MarkdownTOC -->
</details>

---

<a id="writing_feature_files"></a>
# Writing Feature Files
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Essential Tips for Writing Feature Files

The section covers practical tips for writing feature files in Gherkin syntax and explains how to use the Background keyword and data tables effectively.

## Writing Feature Files Tips

- **Strive for Consistency**: Avoid creating multiple Python steps for similar actions. Use consistent language like “I see” throughout the feature file.
  
- **Consider User Experience**: Use labels and terms in the feature files that users see on the interface, like “Customer ID” instead of `customer_id`.
  
- **Build In System Response Cues**: Include cues that signal system responses, such as status messages, to aid testing tools in detecting when an action has completed.

## Background Keyword

- Use `Background` to set a common initial testing state for all scenarios in a feature file.
- Typically used with `Given` statements but can accommodate any keyword.
- Background is run before each scenario, ensuring the same start state for each.

## Tables in Gherkin

- Indent tables to associate them with the corresponding Gherkin statement.
- Delimit columns with vertical bars (`|`) and use the first row for column names.
- The data in tables set in Background will reset before each scenario runs.

## Example Feature File

- Start with the `Feature` keyword and a title that captures the feature's essence.
- Include a user story following the "As a [role], I want [functionality], so that [benefit]" format.
- Use the `Background` keyword for common initial state setup followed by a data table.
- Write scenarios that describe the behavior with `Given`, `When`, `Then` steps.
- Include `And` for additional conditions or actions and `But` for negations.

### Overall, the section emphasizes the importance of clear, consistent language and the use of cues for successful feature file writing in BDD. The `Background` keyword and tables are powerful tools for setting up test conditions and expected data states.

<!-- /MarkdownTOC -->
</details>

---

<a id="selenium"></a>
# Selenium
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Selenium for BDD Testing

This video explains the role of Selenium in Behavior Driven Development (BDD) testing and provides a guide on how to initialize and use Selenium for automating web browser actions.

## What is Selenium?

Selenium is a suite of tools designed for automating web browser activity. It's essentially a WebDriver, which allows instructions to be executed across different browsers such as Chrome, Firefox, Safari, and Edge.

## Benefits of Selenium

- Perfect for integration testing of UIs in microservices architectures.
- Automates user actions like entering data, clicking links, and more.
- Saves time compared to manual testing.

## Initializing Selenium

1. Install the web browser you intend to test with on your system.
2. Instantiate the WebDriver corresponding to your browser.
   - For Chrome, set options such as headless mode and security features off for testing.
   - Create a Chrome driver with these options.

## Finding and Manipulating HTML Elements

- Selenium can find HTML elements by various selectors: class name, CSS selector, id, name, XPath, link text, partial link text, and tag name.
- The Python version of Selenium provides functions for each selector type.
- `find_element_by_id()` is a common and precise method used to interact with elements.

## Example of Using Selenium

```python
# Function to interact with an element by its ID
def find_and_assert_element_by_id(context, text_string):
    element = context.driver.find_element_by_id("customer_id")
    assert text_string in element.get_attribute('value')
```
- In the HTML, Selenium would find an element with the id="customer_id" to interact with.
- Once an element is found, it can be manipulated, such as clearing its content or typing into it using `send_keys()`.

## Handling Latency with WebDriverWait
- Web UI testing can involve latency, and WebDriverWait is used to handle such scenarios.
- It's a function that waits for an element to appear before proceeding with the test.

### Overall, Selenium is a powerful tool for automating and testing web UIs, offering real-user simulation for more effective BDD integration tests.

<!-- /MarkdownTOC -->
</details>

---

<a id="writing_step_files"></a>
# Writing Step Files
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Writing Step Files for Behave

This video provides an overview of how to create step files for Behave and outlines the workflow for writing steps that correspond to Gherkin statements in a feature file.

## What are Step Files?

Step files are Python files that contain functions matching the Gherkin statements from the feature file. Behave uses decorators to match the `Given`, `When`, and `Then` statements and executes corresponding Python functions.

## Workflow for Writing Steps

1. **Import Decorators**: Import the necessary decorators (`@given`, `@when`, `@then`) from Behave based on the Gherkin keywords used in your feature file.

2. **Match Gherkin Statements**: For each Gherkin statement in the feature file, use a decorator with a matching string to denote a corresponding step in the step file.

3. **Implement Step Functions**: Define a function called `step_impl` under each decorator, which Behave will execute when it finds a matching statement. Behave ignores the function names and solely relies on the text string in the decorators for matching.

4. **Use the Context Variable**: Utilize the `context` variable passed into each step to access shared data like web drivers or URLs.

5. **Perform Actions or Assertions**: Implement the necessary actions or assertions within each step function based on the behavior described by the Gherkin statement.

### Example:

- **Feature**: "The pet store catalog service"
- **Scenario**: "The website is up"

```gherkin
When I visit the 'Home Page'
Then I should see 'Welcome to the Pet Shop'
And I should not see '404 Not Found'
```
- Step File:
```python
from behave import when, then

@when('I visit the "Home Page"')
def step_impl(context):
    context.driver.get(context.base_url)

@then('I should see "Welcome to the Pet Shop"')
def step_impl(context):
    assert "Welcome to the Pet Shop" in context.driver.title

@then('I should not see "404 Not Found"')
def step_impl(context):
    element = context.driver.find_element_by_tag_name('body')
    assert "404 Not Found" not in element.text
```

## Summary
- Step files link the behavior described in Gherkin syntax with test code.
- Each Gherkin statement has a corresponding Python function annotated with a matching decorator.
- The context variable is essential for passing shared data through the steps.
- Steps include actions to set up test conditions and assertions to verify outcomes.

### Follow this workflow to ensure that each behavior outlined in your feature file is properly tested with corresponding Python code in Behave.

<!-- /MarkdownTOC -->
</details>

---

<a id="loading_test_data_with_behave"></a>
# Loading Test Data with Behave
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Loading Test Data in Behave

In Behave, test data can be specified in your feature file using the `Background` section, which is a powerful way to establish the initial state and data for testing. However, this data doesn't automatically populate itself—you must manually load it.

## How to Load Test Data

Behave stores the data in a variable within the `context` called `table`. This allows you to iterate over `context.table` to extract and load the necessary data for your tests.

### Example Feature: Search for Pets by Category

The feature file might include a `Background` section with a table format to list pets and their attributes:

```gherkin
Given the following pets
  | name | category | available |
  | Fido | dog      | true      |
  | ...  | ...      | ...       |
```
Each row in this table will be represented as a Python dictionary within context.table, making it accessible by the column names provided.

## Steps File Code to Load Data
1. **Start with a Decorator**: Use the `@given` decorator with the string "the following pets" to match the statement in the feature file.
```python
@given('the following pets')
```
2. **Define a Function**: Implement the step function, passing in the `context`.
```python
def step_impl(context):
    # Implementation details
```
3. **Iterate Over the Table**: Use a for loop to iterate over `context.table`, which gives you each row as a dictionary.
```python
for row in context.table:
    payload = {
        'name': row['name'],
        'category': row['category'],
        'available': row['available'].lower() in ['true', '1']
    }
```
4. **Create Payload**: Construct a payload dictionary with the data from the current row, converting strings to the appropriate data types (e.g., boolean).
5. **Make an HTTP Request**: Use the payload to make a POST request to the server’s REST API to create a pet.
```python
response = context.driver.post(context.base_url + '/pets', json=payload)
```
6. **Save Response and Assert**: Store the response in the context for other steps and assert the expected status code for creation.
```python
assert response.status_code == 201
```

## Summary
- The `Background` allows specifying test data in a tabular format.
- Behave assigns this data to `context.table`.
- Extract and load data by iterating over `context.table` with a for loop.
- Use the extracted data to create payloads and make HTTP requests to populate your test environment.

This process ensures that each scenario starts with a consistent and controlled dataset, allowing for reliable and repeatable test results.

<!-- /MarkdownTOC -->
</details>

---
