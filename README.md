# GitHub Actions Lab – Nickolaos Tassos

This repository contains three GitHub Actions workflows demonstrating CI concepts such as job dependencies, environment variables, secrets, multi-platform automation, and pull-request workflows.

---

## Workflow 1 – Dependent Jobs (build → test → deploy)

**Purpose:**  
To demonstrate job dependency sequencing using `needs`. This ensures that the build stage completes successfully before executing tests, and the tests complete before deployment.

**Key Concepts Demonstrated:**  
- `on: push` event  
- `needs` keyword to control execution order  
- `runs-on` to specify the runtime environment  

**What It Proves:**  
Successful execution of all three jobs in order: **build → test → deploy**.

---

## Workflow 2 – Environment Variables and Secrets

**Purpose:**  
To demonstrate GitHub Secrets, workflow-level environment variables, job-level variables, and step-level variables. Also shows how secrets are masked in logs.

**Key Concepts Demonstrated:**  
- `workflow_dispatch` (manual trigger)  
- `env` at workflow, job, and step scope  
- `secrets` for secure values (AWS keys)  

**What It Proves:**  
Secrets stay masked (`***`), and variables are passed correctly through each execution level.

---

## Workflow 3 – Multi-Platform Workflow (Ubuntu, Windows, macOS)

**Purpose:**  
To demonstrate running parallel CI jobs across different operating systems triggered by a pull request.

**Key Concepts Demonstrated:**  
- `pull_request` trigger  
- `runs-on` with multiple operating systems  
- Parallel job execution  

**What It Proves:**  
All three jobs run simultaneously on **Ubuntu**, **Windows**, and **macOS**.

---

## Challenges and Resolutions

| Challenge | Resolution |
|-----------|------------|
| Pull request workflow did not trigger at first | Triggered correctly after creating a feature branch and PR |
| Secrets could not be displayed | Verified behavior by checking masked output (`***`) in logs |
| Ensuring proper YAML indentation | Followed 2-space indentation to avoid syntax errors |

---

- Each workflow’s YAML content
- Actio
