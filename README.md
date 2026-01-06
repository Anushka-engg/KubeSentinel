# KubeSentinel

[![GoDoc](https://godoc.org/k8s.io/test-infra?status.svg)](https://godoc.org/k8s.io/test-infra)
[![Build status](https://prow.k8s.io/badge.svg?jobs=ci-test-infra-continuous-test)](https://testgrid.k8s.io/sig-testing-misc#continuous)

This repository contains tools and configuration files for the testing and
automation needs of the Kubernetes project.

## 🚀 Key Features

- **Automated CI/CD Orchestration**  
  Manages pre-submit, post-submit, and periodic test jobs at scale.

- **Prow-Based Workflow Automation**  
  Handles PR validation, job triggering, status reporting, and merge automation.

- **Test Result Visualization & Analytics**  
  Provides dashboards and grids to track test health, failures, and trends.

- **Scalable Cloud Infrastructure**  
  Designed to run on Kubernetes with dynamic resource allocation.

- **Failure Detection & Triage**  
  Identifies flaky tests, clusters failures, and improves signal-to-noise ratio.

- **Highly Configurable**  
  YAML-based job definitions and modular tooling.


## ✨ Why KubeSentinel?

Because **manual testing doesn’t scale** — and broken releases aren’t an option.

KubeSentinel ensures:
- Every pull request is validated  
- Every test result is visible  
- Every failure is traceable  
- Every release is reliable  


## 🚀 What It Does

- 🔄 **Automated CI/CD Pipelines**  
  Runs pre-submit, post-submit, and scheduled tests automatically.

- 🤖 **Smart PR Validation**  
  Integrates with GitHub to trigger jobs, report statuses, and gate merges.

- 📊 **Powerful Test Dashboards**  
  Visualize test history, failures, and trends with clarity.

- ☁️ **Cloud-Native & Scalable**  
  Built on Kubernetes to dynamically scale with demand.

- 🧠 **Failure Analysis & Flake Detection**  
  Reduces noise by identifying flaky tests and clustering failures.

- ⚙️ **Config-Driven & Extensible**  
  YAML-based configurations and modular tooling for flexibility.



## 🧩 Core Building Blocks

| Component | Purpose |
|---------|--------|
| **Prow** | CI automation, job orchestration, GitHub integration |
| **TestGrid** | Test result dashboards & historical analysis |
| **Kubetest** | Kubernetes end-to-end test execution |
| **Boskos** | Cloud resource leasing & management |
| **GCS Tools** | Logs, artifacts, and result browsing |



## 🛠️ Technology Stack

- **Languages:** Go, Python, Bash  
- **Platform:** Kubernetes, Docker  
- **CI Engine:** Prow  
- **Configuration:** YAML  
- **Storage & Logs:** Cloud-native object storage



## 📂 Repository Layout

├── config/ # CI jobs & test definitions
├── prow/ # CI automation and plugins
├── testgrid/ # Test dashboards and configs
├── kubetest/ # Kubernetes test runners
├── tools/ # Utilities and helpers
└── docs/ # Documentation & guides

yaml
Copy code



## 🎯 Ideal Use Cases

- Kubernetes core & extension testing  
- Large-scale open-source CI systems  
- Cloud-native infrastructure validation  
- Distributed systems reliability assurance  

## Other Tools

- [`boskos`](https://github.com/kubernetes-sigs/boskos) manages pools of resources; our CI leases GCP projects from these pools
- [`experiment`](/experiment) is a catchall directory for one-shot tools or scripts
- [`gcsweb`](/gcsweb) is a UI we use to display test artifacts stored in public GCS buckets
- [`ghproxy`](https://github.com/kubernetes-sigs/prow/tree/main/cmd/ghproxy) is a GitHub-aware reverse proxy cache to help keep our GitHub API token usage within rate limits
- [`gopherage`](/gopherage) is a tool for manipulating Go coverage files
- [`label_sync`](/label_sync) creates, updates and migrates GitHub labels across orgs and repos based on `labels.yaml` file
- [`kettle`](/kettle) extracts test results from GCS and puts them into bigquery
- [`kubetest2`](https://github.com/kubernetes-sigs/kubetest2) is how our CI creates and e2e tests kubernetes clusters
- [`metrics`](/metrics) runs queries against bigquery to generate metrics based on test results
- [`robots/commenter`](/robots/commenter) is used by some of our jobs to comment on GitHub issues

## 🤝 Contributing

KubeSentinel thrives on community contributions.  
Follow Kubernetes contribution guidelines and ensure all CI checks pass before submitting changes.

---

## 📜 License

Apache License 2.0

---

## 🌍 Impact

KubeSentinel stands at the heart of Kubernetes development —  
