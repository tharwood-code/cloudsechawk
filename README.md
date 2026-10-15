# cloudsechawk

Practical, runnable code for cloud and Kubernetes security engineers and the platform teams
they work with. Everything here was built and exercised in a private lab first; nothing is
published until it has run end to end.

The focus: supply-chain controls (mirror, scan, sign, admit), Kubernetes hardening you can
measure (CIS, policy, audit), and AWS posture checks that run on a schedule with the least
privilege they need — each as a self-contained module with its own README and a cost note.

## Modules

| Module | What it gives you | Status |
|---|---|---|
| `argo-tool-sync/` | Argo Workflows template that mirrors a catalog of tools into your registry (JFrog Container Registry), scans each with Trivy, publishes SARIF/SBOM, and gates on severity | planned |
| `kind-registry-wiring/` | kind on podman talking to a private HTTP registry by name, with the CoreDNS/containerd pieces explained | planned |
| `jcr-least-privilege/` | Repos, permission targets, service users and a smoke test for JFrog Container Registry via REST | planned |
| `kyverno-mirror-only/` | Admission policy pack: only images from your mirror, only if cosign-signed | planned |
| `kube-bench-kind-hardening/` | Before/after CIS runs on a kind control plane with the kubeadm patches that fix each ID | planned |
| `prowler-argo-weekly/` | Prowler against an AWS account from a CronWorkflow, with the exact IAM policy it needs | planned |

## Principles

- **Runs from scratch.** Every module states its prerequisites and a start-to-finish command sequence.
- **Least privilege is the default**, not an exercise left to the reader.
- **Costs are stated.** If a module needs a VM or cloud resources, the README says roughly what it costs per month and how to tear it down.
- **No secrets, ever.** CI runs gitleaks on every push; placeholders use RFC 5737 addresses and `change-me`.

## Contributing

See `CONTRIBUTING.md`. Issues and PRs are welcome; tool/module requests have a template.

## License

Apache License 2.0. See `LICENSE` and `NOTICE`.
