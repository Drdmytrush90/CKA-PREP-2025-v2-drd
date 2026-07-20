# CKA Practice (Exam Order Edition)

Straightforward CKA practice labs derived from the CKA-PREP playlist, renumbered to match my exam prep notes. Every question lives in its own folder with three bash files:

- `LabSetUp.bash` — copy/paste into Killercoda (or any Kubernetes cluster) to prep the environment.
- `Questions.bash` — the scenario text plus the YouTube link for the walkthrough.
- `SolutionNotes.bash` — a step-by-step solution when you need a hint.

## How to Use

1. Launch the CKA Killercoda playground: https://killercoda.com/playgrounds/scenario/cka
2. Clone this repo inside the environment:
   ```bash
   git clone https://github.com/Drdmytrush90/CKA-PREP-2025-v2-drd.git
   cd CKA-PREP-2025-v2-drd
   chmod +x scripts/run-question.sh
   ```
3. Pick a folder under `Question-*` and run:
   ```bash
   ./scripts/run-question.sh "Question-13 Network-Policy"
   ```
   to apply the setup and print the question text, or run `bash "Question-1 HPA/LabSetUp.bash"` manually.
4. Work through the task, then consult `SolutionNotes.bash` if you need help.

## Available Questions

| Question | Topic |
|----------|-------|
| Question-1 HPA | HorizontalPodAutoscaler with scale-down stabilization window |
| Question-2 Ingress | Ingress exposing echoserver-service on example.org/echo |
| Question-3 Cri-Dockerd | Install cri-dockerd .deb + sysctl params for kubeadm |
| Question-4 Resource-Allocation | Fair CPU/memory requests across WordPress replicas |
| Question-5 Sidecar | Co-located logging container with shared /var/log volume |
| Question-6 CNI & Network Policy | Install Calico (tigera-operator) as the cluster CNI |
| Question-7 Storage-Class | local-path StorageClass, WaitForFirstConsumer, default SC |
| Question-8 NodePort | Expose front-end Deployment port 80 via NodePort Service |
| Question-9 PriorityClass | high-priority class one less than highest user-defined |
| Question-10 ArgoCD | Argo CD via Helm template + install, --skip-crds |
| Question-11 MariaDB-Persistent volume | Restore Deployment with PVC bound to existing PV |
| Question-12 Gateway-API | Migrate Ingress to Gateway + HTTPRoute with TLS |
| Question-13 Network-Policy | Pick the least-permissive NetworkPolicy from samples |
| Question-14 Etcd-Fix | Repair kubeadm cluster: etcd endpoint + scheduler config |
| Question-15 CRDs | cert-manager CRD list + kubectl explain certificate.spec.subject |
| Question-16 TLS-Config | nginx ConfigMap: allow TLSv1.3 only |
| Question-17 Taints-Tolerations | Extra practice: taints and tolerations |

Each `Questions.bash` includes a YouTube link with the walkthrough.
