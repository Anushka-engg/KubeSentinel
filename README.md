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

---

## 🧩 Core Components

- **Prow** – CI automation, GitHub integration, job orchestration  
- **TestGrid** – Test result dashboards and historical tracking  
- **Kubetest** – Kubernetes end-to-end test execution  
- **Boskos** – Cloud resource management for test environments  
- **GCS Web Tools** – Artifact and log browsing utilities

## 🛠️ Technology Stack

- **Languages:** Go, Python, Bash  
- **Infrastructure:** Kubernetes, Docker  
- **Configuration:** YAML  
- **CI/CD:** Prow  
- **Cloud Storage & Logging:** GCS-based tooling

---

## 📂 Repository Structure

├── config/ # CI job and test configurations
├── prow/ # Prow components and plugins
├── testgrid/ # Test dashboards and configurations
├── kubetest/ # Kubernetes test execution tools
├── tools/ # Supporting utilities and scripts
└── docs/ # Documentation and guides

yaml
Copy code

---

## 🎯 Use Cases

- Kubernetes core development testing  
- Large-scale open-source CI systems  
- Cloud-native infrastructure validation  
- Distributed systems quality assurance  

---

## 🤝 Contributing

Contributions are welcome from the community.  
Please follow Kubernetes contribution guidelines and ensure all changes pass required CI checks.

---

## 📜 License

Apache License 2.0

---

## 🌍 Community & Impact

KubeSentinel serves as a **critical backbone** of Kubernetes development, enabling reliable testing and delivery for one of the world’s most widely adopted cloud-native platforms.


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

