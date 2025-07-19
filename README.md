# LeanFlex-GKP
CVPR 2025  - LeanFlex-GKP: Flexible Group Count Enables Hassle-Free Structured Pruning, official repo.

## Abstract

Densely structured pruning methods — which generate pruned models in a fully dense format, allowing immediate compression benefits without additional demands — are evolving owing to their practical significance. Traditional techniques in this domain mainly revolve around coarser granularities, such as filter pruning, thereby limiting their performance due to restricted pruning freedom.

Recent advancements in Grouped Kernel Pruning (GKP) have enabled the utilization of finer granularity while maintaining the densely structured format. We observed that existing GKP methods often introduce dynamic operations to different aspects of their procedures, where many were done so at the cost of adding complications and/or imposing limitations — e.g., requiring an expensive mixture of clustering schemes; or having dynamic pruning rates and sizes among groups, which lead to reliance on custom architecture support for its pruned models.

In this work, we argue the best practice to introduce such dynamic operation to GKP is to make `Conv2d(groups)` (a.k.a. group count) flexible under an integral optimization, leveraging its ideal alignment with the infrastructure support of Grouped Convolution. Pursuing such direction, we present a one-shot, post-train, data-agnostic GKP method that is more performant, adaptive, and efficient than its predecessors; while simultaneously being a lot more user-friendly with little-to-no hyper‑parameter tuning or handcrafted criteria required.

---

## ✅ TODO List

### 📄 Documentation & Release
- [ ] Usage examples in `README.md`  
- [ ] Example configs and demo notebook  
- [ ] Package with `setup.py` and publish to PyPI  

### 🧩 Code & Pipeline
- [ ] Flexible‐group `Conv2d` implementation (GKP-Conv2d Module)
- [ ] k‑Means++ grouping & L₂‑norm + geometric‐median pruning modules
- [ ] One‑shot pruning script for a single Conv2d layer
- [ ] Full pruning pipeline

### 📊 Experiments & Baselines
- [ ] Benchmark script on CIFAR‑10, CIFAR‑100, Tiny-ImageNet subsets
- [ ] Implementation of prior arts of GKP (TMI-GKP, SR-GKP)
- [ ] Low‑resource and adversarial case studies  
