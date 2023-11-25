# Continuous Integration (CI)

# Table of Contents
1. [What is Continuous Integration(CI)?](#what_is_ci)
2. [Benefits of Continuous Integration(CI)](#benefits_of_ci)
3. [Social Coding](#social_coding)
4. [Git Feature Branch Workflow: Working in Branches](#ci_git_working_in_branch)
5. [Git Feature Branch Workflow: Making a Pull Request](#ci_git_making_pull_request)
6. [Tools of Continuous Integration (CI)](#tools_of_ci)
7. [Introduction to GitHub Actions](#intro_to_github_actions)
8. [Deeper Dive into GitHub Actions: Part 1](#github_action_p1)
9. [Deeper Dive into GitHub Actions: Part 2](#github_action_p2)

---

<a id="what_is_ci"></a>
# What is Continuous Integration(CI)?
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# What Is Continuous Integration (CI) Summary

## Definition of CI
- **Continuous Integration (CI)**: Automation process for regularly integrating code changes into the main codebase.

## Key Features of CI
- **Short-Lived Branches**: Developers work on small features in brief feature branches.
- **Frequent Pull Requests**: Regular merging back into the main or master branch.
- **Automated CI Tools**: Use of tools to automate testing and integration processes.

## Differences from Traditional Development
- **Traditional Approach**: Developers work on large features in long-lived branches, leading to drift from the main branch.
- **CI Approach**: Focuses on small, incremental changes with continuous testing and integration.

## Benefits of CI
- **Reduces Code Drift**: Frequent integration minimizes divergence between branches.
- **Quick Integration of Fixes**: Fast implementation and testing of critical fixes.
- **Enhanced Collaboration**: Through regular code reviews and discussions on pull requests.
- **Predictability and Reduced Risk**: Better visibility of project progress and timely delivery.
- **Streamlined Development Process**: Automated tools simplify testing and integration.

## CI in Practice
- **Collaborative Development**: Encourages developer collaboration and sharing of ideas.
- **Automated Workflows**: CI tools automate workflows like application building and reporting on build success or failure.

## Conclusion
- CI facilitates more efficient, collaborative, and predictable software development.
- Integrates automated tools to streamline development and testing processes.

<!-- /MarkdownTOC -->
</details>

---

<a id="benefits_of_ci"></a>
# Benefits of Continuous Integration(CI)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Benefits of Continuous Integration (CI) Summary

## Key Benefits
- **Faster Reaction to Code Changes**: Automated testing and building ensure immediate feedback on code changes.
- **Reduced Code Integration Risk**: Frequent integration of smaller code changes minimizes the risk of major issues.
- **Higher Code Quality**: Continuous review and testing during CI processes improve overall code quality.
- **Code Review Efficiency**: Pull requests facilitate efficient and regular code reviews, even for small changes.
- **Reliable Version Control**: Ensures the code in repositories like Git is always functional and ready for deployment.

## Best Practices
- **Continuous Testing**: Every code change undergoes automated tests to identify issues early.
- **Collaborative Code Reviews**: Developers review each other’s pull requests, enhancing quality and knowledge sharing.
- **Monitoring Code Coverage**: Regular checks on code coverage during pull requests to maintain high standards.
- **Idempotent Deployment**: Confidence in deploying code knowing that it has been thoroughly tested and reviewed.

## Conclusion
- CI/CD leads to more efficient, reliable, and high-quality software development.
- Emphasizes the importance of team collaboration and monitoring in the development process.

<!-- /MarkdownTOC -->
</details>

---

<a id="social_coding"></a>
# Social Coding
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Social Coding Summary

## Source Code Management (SCM)
- **Definition**: Tracking versions of source code during development.
- **Tools**: SCM tools or Version Control Systems (VCSs) are used to manage source code.
- **Types**: Centralized (code in a central repository) and Distributed (local clones of code repository).

## Social Coding
- **Concept**: "Open source for inner source," adopting open-source practices within enterprises.
- **Traditional vs. Social Coding**: Previously, private repositories with limited access were common. Social coding makes repositories public for collaboration.
- **Benefits**: Promotes code reuse, prevents redundant development, fosters collaboration.

## Social Coding in Practice
1. **Issue Creation and Assignment**: Open an issue and assign it to yourself to signal you are working on it.
2. **Discussion and Agreement**: Collaborate with the repository owner on the feature development.
3. **Forking and Development**: Fork the repository, create a branch, and make changes.
4. **Pull Request and Review**: Issue a pull request for review. Repository owners have full control over the contributions.

## Key Takeaways
- **Controlled Collaboration**: Repository owners maintain control, yet collaboration is encouraged.
- **Win-Win Situation**: Leveraging existing code saves resources and adds features.
- **Enterprise Adoption**: Applying open-source methodologies internally leads to efficient and collaborative development.

## Conclusion
- Social coding enhances code quality, increases collaboration, and streamlines the development process.

<!-- /MarkdownTOC -->
</details>

---

<a id="ci_git_working_in_branch"></a>
# Git Feature Branch Workflow: Working in Branches
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Git Feature Branch Workflow Summary

## Introduction to Git
- **What is Git**: A distributed source code management tool, widely used for version control.
- **Importance in DevOps**: Facilitates collaborative development and handles projects of all sizes.

## Git Workflow
- **Local Changes**: Use `git add` to stage changes and `git commit` to commit them locally.
- **Remote Changes**: `git push` to send changes to the remote repository.
- **Fetching Changes**: `git fetch` for metadata and `git pull` for actual code changes.
- **Branch Management**: `git checkout` to switch between branches.
- **Undoing Changes**: `git reset --soft` for undoing commits while keeping changes in staging.

## Git Feature Branch Workflow
- **Creating Branches**: Each new feature should have its own branch.
- **Committing Changes**: Regular commits to save progress.
- **Pushing to Remote Branch**: Frequent updates to a remote branch for backup and collaboration.
- **Pull Requests**: For code review and discussions.
- **Merging to Main Branch**: After successful review and testing, merge code into the main branch.

## Best Practices
- **Start with Latest Code**: Always pull the latest changes from the main branch.
- **Descriptive Commit Messages**: Ensure clarity on changes made.
- **Use `.gitignore`**: To avoid unwanted files in the repository.
- **Remote Tracking**: Set up remote branch tracking for easy collaboration.

## Conclusion
- Git and its feature branch workflow are integral to modern software development, enhancing code quality and facilitating efficient collaboration.

<!-- /MarkdownTOC -->
</details>

---

<a id="ci_git_making_pull_request"></a>
# Git Feature Branch Workflow: Making a Pull Request
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Git Feature Branch Workflow: Making Pull Requests Summary

## Overview of Pull Requests in Git Feature Branch Workflow
- **Workflow Steps**: The final steps involve issuing a pull request and merging the code.
- **Start with Main Branch**: Begin by updating your local main branch with the latest changes.
- **Merge Main into Feature Branch**: Ensure your feature branch includes the latest main branch changes.
- **Resolve Conflicts**: Handle any merge conflicts that arise during this process.

## Preparing for Pull Request
- **Update Main Branch Locally**: Switch to the main branch and run `git pull`.
- **Merge Updated Main into Feature Branch**: Apply the latest changes from the main to your feature branch.
- **Push Updated Branch**: After resolving conflicts and updating, push the branch to the remote repository.

## Post-Merge Actions
- **Switch to Main Branch**: After merging the pull request, switch back to the main branch.
- **Pull Latest Changes**: Update the main branch with the newly merged changes.
- **Delete Old Feature Branch**: Remove the feature branch used, as it's now merged with the main branch.
- **Create New Feature Branch**: For new development work, start with a fresh feature branch.

## Key Practices
- **Regular Updates**: Keep both the main and feature branches updated with the latest changes.
- **Clean Workflow**: Maintain a streamlined process by deleting old branches and starting new ones for each feature.
- **Pull Request Review**: Ensure pull requests are thoroughly reviewed before merging.

## Conclusion
- The Git Feature Branch workflow with pull requests is essential for organized and efficient code integration, ensuring up-to-date and conflict-free merging into the main branch.

<!-- /MarkdownTOC -->
</details>

---

<a id="tools_of_ci"></a>
# Tools of Continuous Integration (CI)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Tools of Continuous Integration Summary

## Jenkins
- **Type**: Both Continuous Integration and Continuous Delivery.
- **Features**: 
  - Open-source with a large ecosystem of plugins.
  - Utilizes ‘Groovy’ language in a Jenkinsfile for CI/CD pipelines.
- **Workflow**: Set up project on Jenkins server, create Jenkinsfile in the project repository, specify CI instructions.
- **Build Environment**: Supports builds in VM or Docker container.
- **Downsides**: Requires managing plugins and manual configuration on Jenkins website.

## CircleCI
- **Type**: CI/CD service, not open-source.
- **Features**: 
  - Uses YAML file for CI process.
  - Natively supports various languages and databases.
  - Docker compatible.
- **Workflow**: Set up project on CircleCI website, create config file in the repository, specify CI instructions.
- **Build Environment**: Supports builds in VM or Docker container.
- **Downside**: Manual setup on CircleCI website.

## Travis CI
- **Type**: CI/CD hosted service.
- **Features**: 
  - Supports numerous languages, databases, and Docker.
  - Utilizes YAML file (.travis.yml) for CI processes.
  - Available as a service or enterprise license.
- **Workflow**: Set up project on Travis CI website, create .travis.yml in the repository, specify CI instructions.
- **Build Environment**: Builds in VM or Docker container.
- **Downside**: Requires manual setup on Travis CI admin UI.

## Common Characteristics
- **Pipeline as Code**: All tools support CI pipeline definitions as code, enhancing automation and repeatability.
- **Build Environments**: Support both native and Docker builds.
- **Service Model**: CircleCI and Travis CI are offered as services, reducing management overhead.

## GitHub Actions (Mentioned)
- Integrated into GitHub, allows CI/CD pipelines to be managed as YAML files.

## Conclusion
- These CI tools each have unique attributes but share common goals of enabling efficient and automated Continuous Integration.

<!-- /MarkdownTOC -->
</details>

---

# Table of Contents
1. [Introduction to GitHub Actions](#intro_to_github_actions)

<a id="intro_to_github_actions"></a>
# Introduction to GitHub Actions
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Introduction to GitHub Actions

## Overview: Basic Understanding of GitHub Actions

- **GitHub Actions**: A CI/CD tool integrated into every GitHub repository.
- **Availability**: Accessible as a built-in service in GitHub, requiring no extra sign-up or add-ons.
- **Pipeline as Code**: Treats CI pipeline as code using `.yaml` files.
</details>

## GitHub Actions Features
- **Workflow Definition**: Defined in `.yaml` files stored in `.github/workflows` folder.
- **Event-Driven Execution**: Workflows are triggered based on specified events.
- **Marketplace Integration**: Offers a variety of pre-built actions for numerous languages and tasks.
- **Simplicity and Reproducibility**: No external website or manual setup required, ensuring reproducible workflows.
- **Starter Code**: Functional workflow templates available for customization.

## Workflow Components
- **Workflow**: Automated procedures composed of jobs and steps.
- **Events**: Triggers for workflows, like push, pull request, or release creation.
- **Runners**: Execute jobs, either built-in or self-hosted.
- **Jobs**: Group specific tasks, e.g., build, publish, or deploy.
- **Steps**: Constituent of jobs, performing tasks like code checkout, compilation, linting, and testing.
- **Actions**: Basic units within steps, executing single tasks like code checkout or dependency installation.

## Key Takeaways
- **CI/CD Integration**: Available in every GitHub repository.
- **Rich Marketplace**: Extensive collection of actions for diverse needs.
- **Ease of Setup**: Starter code and template-based approach for quick setup.
- **Workflow Structure**: Organized into jobs, steps, and actions for efficient process management.

<!-- /MarkdownTOC -->
</details>

---

<a id="github_action_p1"></a>
# Deeper Dive into GitHub Actions: Part 1
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Deeper Dive into GitHub Actions – Part One

## Introduction
This video provides a comprehensive understanding of GitHub Actions, including its setup, components, and functionality.

## Setting Up GitHub Actions
- **Create a Folder Structure**: Begin by creating a `.github/workflows` folder in your project's root directory.
- **YAML Workflow Files**: Place one or more .yaml files in the `workflows` folder. These files contain workflow statements.

## Workflow Execution
- **Triggering Workflows**: Workflows are executed based on specified events (e.g., pushing to master branch, pull request).
- **Isolated Environment**: Jobs within a workflow run in an isolated environment, either on a virtual machine or in a Docker container.

## Configuring GitHub Actions
1. **Create `.github` Folder**: If not existing, create this folder at the root of your project.
2. **Add `workflows` Folder**: Under `.github`, create a `workflows` folder.
3. **Place .yaml Files**: Add your workflow .yaml files to the `workflows` folder.

## Components of a Workflow
- **Events**: Triggers for workflow execution (e.g., code commits, pull requests).
- **Jobs**: Comprise steps performed on the same runner, executed in parallel by default but can be set to run serially.
- **Runners**: Servers that perform jobs on specific platforms or operating systems.
- **Steps**: Individual tasks within a job, such as checking out code or building a Docker container.
- **Actions**: Predefined procedures executed within a step, available through GitHub Actions Marketplace.

## Detailed Components
- **Events**: Various events (35 types) can trigger workflows, like issue modifications or code pushes.
  - **Examples**: Pull request on master branch, push to main branch, release publishing.
- **Jobs**: A set of steps using the same runner.
  - **Dependencies**: Use `needs` keyword to create job dependencies.
  - **Components**: Include a runner, optional services, and steps.

## Key Takeaways
- **Configuration**: GitHub Actions is configured through .yaml files in a `.github/workflows` folder.
- **Workflow Components**: Include events, jobs, runners, steps, and actions.
- **Events and Jobs**:
  - An event triggers a workflow.
  - A job is a series of steps using the same runner.

<!-- /MarkdownTOC -->
</details>

---

<a id="github_action_p2"></a>
# Deeper Dive into GitHub Actions: Part 2
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

# Deeper Dive into GitHub Actions – Part Two

## Key Concepts

### 1. Components of a Job in GitHub Actions Workflow
- **Runners**: Servers that perform jobs on specific platforms or operating systems.
  - Supported OS: Various flavors of Ubuntu, macOS, and Windows Server.
  - Runner definition uses `runs-on:` keyword.
  - Examples: 
    - `build` job runs on the latest Ubuntu version.
    - Specified Ubuntu 22.04 for consistent environment.
    - Python 3.9-slim Docker container on Ubuntu for container-based development.

### 2. Services in a Workflow
- Defined as Docker containers.
- Can be any public Docker image, including custom ones.
- Used to create databases, message queues, etc.
- Example: Postgres database service for unit tests, accessible via DNS name `postgres`.

### 3. Steps in a Workflow
- The core of GitHub Actions where the work is executed.
- Comprises shell commands or actions.
- Optional features:
  - `name:` for descriptive identification in reports.
  - `id:` for referencing in other steps.
- Defined using `uses:` for actions or `run:` for shell commands.
- Supports multiple commands and environment variables (`env:`).

### 4. Actions
- Executable procedures within steps.
- Defined with `uses:` followed by the action name.
- Configurable with arguments (`with:`) or `args:`.
- GitHub Actions Marketplace: A resource for finding and utilizing prebuilt actions.

## Example Workflow
- **Workflow Name**: `CI Build`
- **Trigger**: Pull request to the master branch.
- **Job**: `build` running on Python 3.9 container and Ubuntu.
- **Service**: Redis database from Redis 6-Alpine Docker image.
- **Steps**:
  - Checkout code using a GitHub action.
  - Upgrade pip and wheel, install packages from `requirements.txt`.
  - Run unit tests with `nosetests`.
  - Set `DATABASE_URI` environment variable for Redis service.
  - Upload code coverage data to Codecov using a specific version of codecov uploader.

## Summary
- Jobs in a GitHub Actions workflow consist of runners, services, steps, and actions.
- Runners perform jobs on designated operating systems.
- Services are Docker containers that support the workflow.
- Steps are tasks comprising shell commands or actions.
- Actions are executable procedures within steps.
- The GitHub Actions Marketplace is a key resource for finding prebuilt actions.

<!-- /MarkdownTOC -->
</details>

---

<a id="--"></a>
# --
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---

<a id="--"></a>
# --
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->



<!-- /MarkdownTOC -->
</details>

---
