---
layout: default
---

&nbsp;

[Proceedings 2019 - Part 1](/schedule/images/Proceedings2019_Part1.pdf) &emsp;&emsp;&emsp;   [Proceedings 2019 - Part 2](/schedule/images/Proceedings2019_Part2.pdf)

[Proceedings 2020 - Part 1](/schedule/images/Proceedings2020_Part1.pdf) &emsp;&emsp;&emsp;   [Proceedings 2020 - Part 2](/schedule/images/Proceedings2020_Part2.pdf)

[Proceedings 2021 - Part 1](/schedule/images/Proceedings2021_Part1.pdf) &emsp;&emsp;&emsp;   [Proceedings 2021 - Part 2](/schedule/images/Proceedings2021_Part2.pdf)

[Proceedings 2023 - Part 1](/schedule/images/Proceedings2023_Part1.pdf) &emsp;&emsp;&emsp;   [Proceedings 2023 - Part 2](/schedule/images/Proceedings2023_Part2.pdf)

&nbsp;

The course project can be categorized as a literature review, original research, or a literature review that leads to original research.

- **Literature Review:** An in-depth review and analysis of **a collection of papers** around a topic. The review must provide a critical summary, exposition, and discussion of the topic, which will often require reading related work for context. **This option will be sparsely selected by the tutor; it is easy to throw a bunch of papers into ChatGPT/Gemini and get your work done. The literature review should be on an interesting collection of papers that they do not seem connected but they are.**

- **Original Research:** You are strongly encouraged to align the project with your current research interests. Otherwise, the instructor can provide ideas. Projects can be theoretical (e.g., proving a convergence guarantee) or experimental (e.g., implementing and benchmarking an algorithm). **This will be the default option for projects.**

You are encouraged to team up. Optimal size for a team is 3 students: deviations from this number will be considered given the circumstances (either there is no one to team up, or you have your own research you want to push forward, or the project is difficult and allows more team-members).

### Milestones

- **Project Selection:** Choose a project topic ASAP. **Deadline: October 3rd.**

- **Project Proposal:** Submit a one-page description of your project. Outline the core problem, why it is interesting, and a list of key papers to read. For research projects, provide a clear plan of the steps you will take. **Deadline: October 10th.**

- **In-Class Presentation:** Towards the end of the semester, you will give a short spotlight talk (5-10 minutes) on your project. Focus on high-level ideas and key results.

- **Final Report:** A written report of at least six pages (excluding references) in a standard conference format (e.g., ICML/NeurIPS LaTeX template). **Deadline: End of the semester.** Note that exceptional projects can be continued beyond the semester with the goal of publication.

---

### Suggested List of Projects & Papers

Below is a list of potential project ideas. You are welcome to propose your own, subject to instructor approval.

---

#### **Topic 1: Efficient Model Adaptation and Low-Rank Training**
The rise of massive foundation models has made full fine-tuning computationally prohibitive. This area explores parameter-efficient techniques that modify only a small fraction of a model's weights.

**Project Focus:** This project is heavily **implementation-focused**. The goal is to implement and compare two or more recent LoRA-like methods. A successful project would involve fine-tuning a small-to-medium language model (e.g., GPT-2, Llama-2-7B) on a downstream task and benchmarking the methods on both task performance (e.g., accuracy) and computational efficiency (memory usage, training time).

- **Core Papers:**
  - [LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685)
  - [LoST: Low-Rank and Sparse Training for Deep Neural Networks](https://arxiv.org/abs/2402.06202)
  - [SLTrain: A Sparse Backpropagation-Free and LoRA-like Finetuning Approach](https://arxiv.org/abs/2404.09345)
  - [GaLore: Memory-Efficient LLM Training by Gradient Low-Rank Projection](https://arxiv.org/abs/2403.03507)

---

#### **Topic 2: Mixture-of-Experts (MoEs) and Learning to Specialize**
MoE models activate only a fraction of their parameters for any given input, enabling massive model scale with constant computational cost. This topic explores the optimization and design of these architectures.

**Project Focus:** A blend of **literature review and implementation**. Review the evolution of routing algorithms in MoEs. The implementation could involve building a simple MoE layer on top of a standard transformer block and experimenting with different routing strategies. The report should discuss the trend towards parameter-efficient and dynamic routing.

- **Core Papers:**
  - [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://arxiv.org/abs/1701.06538)
  - [DD-oME: A Differentiable and Dynamic Offloading-based Mixture-of-Experts Framework](https://arxiv.org/abs/2405.17646)
  - [Parameter-Efficient Routed Fine-Tuning for Large Language Models](https://arxiv.org/abs/2405.07119)
  - [Soft-MoE: Scaling Mixture-of-Experts to Billions of Experts for Dynamic Model Training](https://arxiv.org/abs/2308.00951)

---

#### **Topic 3: The Quest for the Optimal Learning Rate**
The learning rate is arguably the most critical hyperparameter in deep learning. This project area explores the frontier of adaptive and "learning-rate-free" optimization algorithms that aim to automate this choice.

**Project Focus:** A mix of **theoretical review and implementation**. The student should compare the theoretical assumptions and guarantees behind 2-3 of the listed methods. The implementation component would involve benchmarking these adaptive methods against standard SGD with momentum and Adam on a well-known vision or language task, analyzing their convergence speed and final performance.

- **Core Papers:**
  - [Stochastic Polyak Step-size for SGD: An Adaptive Learning Rate for Fast Convergence](https://arxiv.org/pdf/2002.10542.pdf)
  - [Learning-Rate-Free Learning by D-Adaptation](https://arxiv.org/pdf/2301.07733.pdf)
  - [Automatic Gradient Descent: Deep Learning without Hyperparameters](https://arxiv.org/pdf/2304.05187.pdf)
  - [Adaptive Proximal Algorithms for Convex Optimization under Local Lipschitz Continuity of the Gradient](https://arxiv.org/pdf/2301.04431.pdf)
  
---

#### **Topic 4: Optimization for Distributed, Federated, and Asynchronous Systems**
How do you train a model when data is decentralized and workers are unreliable? This area studies optimization algorithms that are robust to communication delays, client drift, non-IID data, and asynchronicity.

**Project Focus:** A mix of **review and optional implementation**. Review the core challenges in federated/distributed optimization. Implement a simple simulation of Federated Averaging (FedAvg) and introduce artificial delays to observe their effect. The report should analyze recent theoretical advances that provide convergence guarantees under these challenging, realistic conditions.

- **Core Papers:**
  - [Communication-Efficient Learning of Deep Networks from Decentralized Data](https://arxiv.org/abs/1602.05629) (FedAvg)
  - [Asynchronous Stochastic Optimization Robust to Arbitrary Delays](https://proceedings.neurips.cc/paper/2021/file/4b85256c4881edb6c0776df5d81f6236-Paper.pdf)
  - [Asynchronous SGD Beats Minibatch SGD Under Arbitrary Delays](https://arxiv.org/pdf/2206.07638.pdf)
  - [Sharper Convergence Guarantees for Asynchronous SGD for Distributed and Federated Learning](https://arxiv.org/pdf/2206.08307.pdf)
  - [Learning Under Delayed Feedback: Implicitly Adapting to Gradient Delays](https://arxiv.org/pdf/2106.12261.pdf)

---

#### **Topic 5: Scalable Training via Model Decomposition (IST)**
Instead of training a monolithic network, what if we could break it into smaller parts that can be trained semi-independently? This topic explores various strategies for model decomposition to enable efficient, distributed training.

**Project Focus:** A **literature review** project. Compare and contrast different decomposition strategies, such as Independent Subnetwork Training (IST), vertical decomposition, and layer-wise approaches like in `Resist`. A strong report will synthesize these ideas and discuss their respective trade-offs in terms of communication cost, scalability, and model performance.

- **Core Papers:**
  - [Distributed Learning of Fully Connected Neural Networks Using Independent Subnet Training](https://par.nsf.gov/servlets/purl/10404274)
  - [GIST: Distributed Training for Large-Scale Graph Convolutional Networks](https://link.springer.com/article/10.1007/s41468-023-00127-8)
  - [Resist: Layer-wise Decomposition of ResNets for Distributed Training](https://proceedings.mlr.press/v180/dun22a/dun22a.pdf)
  - [Federated Learning Over Images: Vertical Decompositions and Pre-Trained Backbones Are Difficult to Beat](https://openaccess.thecvf.com/content/ICCV2023/papers/Hu_Federated_Learning_Over_Images_Vertical_Decompositions_and_Pre-Trained_Backbones_Are_ICCV_2023_paper.pdf)

---

#### **Topic 6: AI for Scientific Discovery & Material Science**
Optimization is at the heart of modern scientific discovery, powering generative models for molecules and crystals, and driving the "active learning" loop in autonomous labs that decide the next experiment to run.

**Project Focus:** This is a **literature review** project focusing on problem formulation. The student should select one sub-area (e.g., crystal generation) and deeply analyze how the scientific goal is translated into a tractable optimization problem. What are the objective functions? What are the constraints (e.g., chemical validity)? What specific algorithms (e.g., diffusion models, VAEs) are used to solve them?

- **Core Papers:**
  - [Crystal Diffusion Variational Autoencoder for Periodic Material Generation](https://arxiv.org/pdf/2110.06197)
  - [An Autonomous Laboratory for the Accelerated Synthesis of Novel Materials](https://www.nature.com/articles/s41586-023-06734-w.pdf)
  - [Scaling Deep Learning for Materials Discovery](https://www.nature.com/articles/s41586-023-06735-9.pdf)
  - [Can LLMs Generate Diverse Molecules?](https://arxiv.org/pdf/2410.03138)

---

#### **Topic 7: Second-Order Optimization in Deep Learning**
While first-order methods like SGD and Adam dominate, second-order methods, which use curvature (Hessian) information, promise faster convergence. The challenge lies in making them scalable.

**Project Focus:** This is a **theory and literature review** project. Compare and contrast how different methods (like K-FAC and Shampoo) approximate the Hessian to make computation feasible. A deep dive into the trade-offs between per-iteration cost, memory, and convergence rate would make for a strong report.

- **Core Papers:**
  - [Optimizing Neural Networks with Kronecker-factored Approximate Curvature](https://arxiv.org/abs/1503.05671) (K-FAC)
  - [Shampoo: Preconditioned Stochastic Tensor Optimization](https://arxiv.org/abs/1802.09568)
  - [Deep Learning via Hessian-free Optimization](http://www.cs.toronto.edu/~jmartens/docs/Deep_HessianFree.pdf)
  - [Large-Scale Distributed Second-Order Optimization Using Kronecker-Factored Approximate Curvature](https://arxiv.org/pdf/1811.12019.pdf)

---

#### **Topic 8: Optimization in Quantum Machine Learning**
Training quantum circuits as machine learning models presents unique optimization challenges not found in classical settings, such as the barren plateau phenomenon.

**Project Focus:** A **literature review** focused on the translation of classical optimization concepts to the quantum realm. Students should explore the challenges of gradient estimation on quantum hardware and review algorithms designed to navigate the complex loss landscapes of variational quantum algorithms.

- **Core Papers:**
  - [Barren plateaus in quantum neural network training landscapes](https://arxiv.org/abs/1803.11173)
  - [Quantum Natural Gradient](https://arxiv.org/abs/1909.02108)
  - [Parameter Setting in Quantum Approximate Optimization of Weighted Problems](https://arxiv.org/pdf/2305.15201)
  - [A variational perspective on the quantum approximate optimization algorithm](https://arxiv.org/abs/2009.10095)

---

#### **Topic 9: Embedding Solvers as Differentiable Neural Network Layers**
What if a layer in your network was an optimization solver? This paradigm allows for embedding constrained optimization, combinatorial solvers, or even physics simulations directly into end-to-end trainable models.

**Project Focus:** **Review-heavy with a potential implementation component.** The core task is to review the role of the Implicit Function Theorem in enabling backpropagation through a solver. A more advanced project could involve implementing a simple differentiable QP layer using a library like `cvxpylayers`.

- **Core Papers:**
  - [OptNet: Differentiable Optimization as a Layer in Neural Networks](https://arxiv.org/abs/1703.00443)
  - [Differentiable Convex Optimization Layers](https://arxiv.org/abs/1910.12430)
  - [SATNet: Bridging deep learning and logical reasoning using a differentiable satisfiability solver](https://arxiv.org/abs/1905.12149)

---

#### **Topic 10: The Interplay of Energy-Based Models and Optimization**
Energy-Based Models (EBMs) offer a flexible framework for generative modeling but are notoriously difficult to train. This project explores the unique optimization challenges they present.

**Project Focus:** A **theoretical review**. What are the connections between the properties of the energy function and the optimization landscape? Review the role of MCMC-based methods for gradient estimation (like contrastive divergence) and discuss how these sampling methods interact with the optimizer's convergence. What is the "twist"? The twist is to connect EBM training to the broader class of saddle-point optimization problems.

- **Core Papers:**
  - [Implicit Generation and Generalization in Energy-Based Models](https://arxiv.org/abs/2006.14233)
  - [How to Train Your Energy-Based Models](https://arxiv.org/abs/2101.03288)
  - [Energy-Based Models for Continual Learning](https://arxiv.org/abs/2011.13264)

&nbsp;
&nbsp;
