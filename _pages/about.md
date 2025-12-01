---
layout: about
title: home
permalink: /

profile:
  align: right
  image: working.jpg
  image_circular: false

news: true
selected_papers: false
social: false
---

Hi, I’m Zhaolun (Will) Su, a researcher specializing in large language models, vision-language systems, and post-training alignment. My work focuses on building scalable pipelines that enable models to self-improve, generate high-quality synthetic data, and learn robust reasoning behaviors without relying on stronger teacher models.

I’ve led major cross-team research efforts at [Meta MRS AI](https://ai.meta.com/research/), driving improvements in LLM reasoning, VLM post-training, and self-alignment, and previously worked across autonomous driving and mapping organizations at AutoX, Google, Waymo. My research interests center on reinforcement learning for LLMs, self-training, synthetic data generation, and alignment methods that make large models more adaptive, reliable, and aligned with human preferences.

I’m passionate about bridging advanced research with practical, production-ready systems—designing models and pipelines that scale, generalize, and deliver measurable impact in real-world applications such as recommendation and agentic systems.

<div style="margin-top: 2rem;">
  <p><strong>Contact:</strong> <a href="mailto:zhsu@umich.edu">zhsu@umich.edu</a> <em></em></p>
</div>

---

<h2 style="text-align: center; margin-top: 3rem; margin-bottom: 2.5rem; font-size: 2rem; font-weight: 300; color: #2c3e50;">Publications & Projects</h2>

<div style="background-color: #f7f8fa; padding: 0.9rem 1.5rem; margin-top: 2rem; margin-bottom: 1.2rem; border-left: 4px solid #6b7c8f; border-radius: 6px; box-shadow: 0 1px 3px rgba(0,0,0,0.04); transition: all 0.3s ease;">
  <h3 style="margin: 0; color: #2c3e50; font-size: 1.2rem; font-weight: 600; letter-spacing: 0.2px;">Improving LLM Reasoning Ability</h3>
</div>

**RESTRAIN: From Spurious Votes to Signals — Self-Driven RL with Self-Penalization**  
Zhaoning Yu†, <u>Will Su†</u>,, Leitian Tao, Haozhu Wang, Aashu Singh, Hanchao Yu, Jianyu Wang, Hongyang Gao, Weizhe Yuan, Jason Weston, Ping Yu‡, Jing Xu‡.  († Equal contribution)

*2025* [[PDF](https://arxiv.org/pdf/2510.02172)]

RESTRAIN (2025) proposes a label-free reinforcement-learning method that lets LLMs self-improve on reasoning tasks without any human-provided answers. Instead of trusting majority-vote pseudo-labels—which are often wrong on hard problems—RESTRAIN uses the full distribution of sampled answers, weighting each candidate answer by its vote frequency, and penalizes prompts where the model shows low self-consistency (i.e., no answer is reliable). It further downweights inherently uncertain prompts using a frozen reference model, preventing the RL loop from amplifying spurious confidence. Combined with GRPO-style policy optimization, this yields strong empirical gains: on multiple benchmarks, RESTRAIN outperforms prior unsupervised RL baselines and often matches or even exceeds gold-label supervised RL—despite using zero human labels. The result is a robust and scalable approach for self-training LLMs on reasoning tasks using only unlabeled data.

---

**SVR-R1: Bootstrapping Multi-modal Reasoning with Self-verification in Reinforcement Learning**  
Mingyuan Wu, Jingcheng Yang, Shengyi Qian, Xudong Wang, Jize Jiang, Qifan Wang, Aashu Singh, Khoi Pham, Claire Liu, <u>Will Su</u>, Zhuokai Zhao, Klara Nahrstedt, Jianyu Wang, Hanchao Yu.  
*2025* 

Self-Verified Reasoner (SVR-R1), a novel reinforcement learning (RL) framework designed to enhance multimodal reasoning in vision-language models (VLMs). SVR-R1 leverages a model’s own self-verification as a learning signal: for each query, the model proposes an answer and then uses its own weights to verify the answer with a binary verdict (Yes/No). If the verdict is "No," the model is prompted to rethink and regenerate its answer; if "Yes," or after a set number of turns, the answer is finalized for reward computation. SVR-R1 is implemented using Group Relative Policy Optimization (GRPO) and an asynchronous multi-turn rollout framework, requiring no external supervision or auxiliary critics. Experiments on challenging vision–language reasoning benchmarks show that SVR-R1 significantly improves accuracy over strong GRPO baselines, with models gradually relying less on verification rounds as they internalize self-correction. This approach bridges the gap between inference-time self-refinement and RL training for VLMs, offering a simple yet effective method for bootstrapping multimodal reasoning and paving the way for future research in self-improving VLMs.

---

<div style="background-color: #f7f8fa; padding: 0.9rem 1.5rem; margin-top: 2rem; margin-bottom: 1.2rem; border-left: 4px solid #6b7c8f; border-radius: 6px; box-shadow: 0 1px 3px rgba(0,0,0,0.04); transition: all 0.3s ease;">
  <h3 style="margin: 0; color: #2c3e50; font-size: 1.2rem; font-weight: 600; letter-spacing: 0.2px;">Autonomous Driving & HD Map</h3>
</div>

**Google Geo HD Map**  
Semantic Surfel Based Traffic Control Items Curation Designed and implemented semantic classification models for street view surfels, which are used to curate traffic control items including lane markers, flow-lines, lane connectivity, merges, and splits. Implemented pipelines to scale model deployment at Google scale, and metrics to monitor long-term model performance(Accuracy, Latency, etc). Tech: Vision Transformer, Multiple View Geometry, Map Reduce, etc

---

**Waymo Perception**  
Multimodal FOD Perception - LiDAR/Camera/HD Map Designed, implemented, and deployed ML ML-based real-time lane surface model, that performs geometry mapping guided by onboard attention. The module simultaneously produces the elevation, norm and incline angle of lane surfaces over ROI. Built pipelines to supervise the model’s long-term performance as the fleet adapts to different operation domains. Improved model latency with optimized mathematical models including CNN, RANSAC, PCA and ICP matching.

---

<div style="background-color: #f7f8fa; padding: 0.9rem 1.5rem; margin-top: 2rem; margin-bottom: 1.2rem; border-left: 4px solid #6b7c8f; border-radius: 6px; box-shadow: 0 1px 3px rgba(0,0,0,0.04); transition: all 0.3s ease;">
  <h3 style="margin: 0; color: #2c3e50; font-size: 1.2rem; font-weight: 600; letter-spacing: 0.2px;">Surgical Robotics</h3>
</div>

**Integration of Autopatching with Automated Pipette and Cell Detection in Vitro**  
Qiuyu Wu, Ilya Kolb, Brendan M Callahan, <u>Zhaolun Su</u>, William Stoy, Suhasa B Kodandaramaiah, Rachael Neve, Hongkui Zeng, Edward S Boyden, Craig R Forest, Alexander A Chubykin.  
*2016* [[PDF](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=nzkurd4AAAAJ&citation_for_view=nzkurd4AAAAJ:d1gkVwhDpl0C)] 

<div style="text-align: center;">
<iframe width="560" height="315" src="https://www.youtube.com/embed/V9QZI-y7LVo?si=FXG83RKvRYGm0Fh-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

We introduces an automated, computer-vision-guided patch-clamp system that integrates real-time pipette tip tracking with robust, label-free cell detection in acute brain slices, enabling a fully automated approach to in-vitro whole-cell electrophysiology. The system uses image-based algorithms to locate and continuously track the pipette in 3-D, identify candidate neurons from DIC/IR-DIC imagery, and dynamically guide the pipette toward the cell membrane with closed-loop visual feedback. By automating critical manual steps—pipette approach, membrane contact detection, seal formation, and break-in—the method achieves reliable whole-cell recordings without human intervention. This computer-vision-driven pipeline demonstrates that high-quality patch-clamp experiments can be achieved through precise image-based control, significantly improving throughput, standardization, and reproducibility relative to manual electrophysiology.

---

**US Patent: Systems and methods for automated image-guided patch-clamp electrophysiology in vitro**  
Alexander A Chubykin, <u>Zhaolun Su</u>, Qiuyu Wu 
*2016* [[Patent](https://patents.google.com/patent/US10324080B2/en)] 

This patent (US 10324080B2) introduces a fully automated, image-guided patch-clamp system that uses real-time computer vision and robotic micromanipulation to perform whole-cell electrophysiology in vitro without human intervention. The invention automatically detects cells from label-free microscope images, tracks the pipette tip in 3-D, and precisely guides the pipette to each target neuron while controlling pressure and seal formation through a closed-loop feedback process. By automating all major steps of the traditional manual patch-clamp workflow, the system delivers high-quality, reproducible recordings at significantly higher throughput, lowering the skill barrier and enabling large-scale, systematic electrophysiological studies.

---


<div style="text-align: center; font-size: 2.5rem; margin-top: 3rem; margin-bottom: 2rem;">
  <a href="https://www.linkedin.com/in/zhaolun-will-su/" title="LinkedIn" target="_blank" style="margin: 0 1rem;"><i class="fab fa-linkedin"></i></a>
   <a href="https://scholar.google.com/citations?user=nzkurd4AAAAJ" title="Google Scholar" target="_blank" style="margin: 0 1rem;"><i class="ai ai-google-scholar"></i></a>
  <a href="https://github.com/zhsu-private" title="GitHub" target="_blank" style="margin: 0 1rem;"><i class="fab fa-github"></i></a>
</div>