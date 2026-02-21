# secure-repo-before-release
# Secure Repo Before Release – DevSecOps Demo

## 📌 Overview
This repository demonstrates how DevSecOps practices can be used to secure a codebase before release by integrating automated security checks into a CI pipeline.

## 🔐 Problem Statement
A teammate accidentally committed an API key into the repository. The goal is to ensure that secrets and vulnerable dependencies are detected automatically and blocked during CI.

## 🛠 Tools Used
- GitHub Actions (CI pipeline)
- Gitleaks (Secret scanning)
- npm audit (Dependency vulnerability scanning)

## 🚦 CI Security Checks
The CI pipeline performs the following checks on every push:
1. Scans the repository for hardcoded secrets using Gitleaks
2. Scans dependencies for known vulnerabilities using npm audit

## ❌ Fail Scenario
- An API key was intentionally committed to simulate a security mistake
- A vulnerable dependency version was used
- The pipeline failed, blocking the release

## 🔧 Fix Applied
- Removed secrets from the repository
- Added `.gitignore` to prevent future secret commits
- Updated vulnerable dependencies to secure versions

## ✅ Pass Scenario
After applying fixes, the pipeline passed successfully, ensuring the repository is secure for release.

## 📚 DevSecOps Learning Outcome
This project demonstrates secure SDLC practices by shifting security left and enforcing automated security gates before production deployment.