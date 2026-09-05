<div align="center">

# Awesome-VLM-Streaming-Video 🎬
<img src="https://img.shields.io/github/stars/ydyhello/Awesome-VLM-Streaming-Video.svg?style=social">
<img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg">
<a href="https://github.com/ydyhello/Awesome-VLM-Streaming-Video/pulls"><img src="https://img.shields.io/badge/PRs-Welcome-red"></a>
<a href="https://github.com/ydyhello/Awesome-VLM-Streaming-Video/commits/main"><img src="https://img.shields.io/github/last-commit/ydyhello/Awesome-VLM-Streaming-Video?color=blue"></a>
</div>

## 📒 Introduction

📚 A curated collection of papers and open-source code repositories dedicated to the application of Vision-Language Models (VLMs) for streaming video.

## 📖 Contents
- [Awesome-VLM-Streaming-Video 🎬](#awesome-vlm-streaming-video-)
  - [📒 Introduction](#-introduction)
  - [📖 Contents](#-contents)
  - [🛠️ Project](#️-project)
  - [📋 Technical Report](#-technical-report)
  - [💬 Proactive Interaction](#-proactive-interaction)
    - [Auxiliary Response Head](#auxiliary-response-head)
    - [Generative Token-based Trigger](#generative-token-based-trigger)
    - [RL-optimized Proactive Response](#rl-optimized-proactive-response)
    - [Training-free / Feature-based Trigger](#training-free--feature-based-trigger)
    - [Hybrid Trigger Framework](#hybrid-trigger-framework)
    - [Learned Response Timing](#learned-response-timing)
  - [🧠 Long-term Memory Management](#-long-term-memory-management)
    - [Hierarchical Multi-level Memory](#hierarchical-multi-level-memory)
    - [Sliding-window / Eviction](#sliding-window--eviction)
    - [Token Compression / Pruning](#token-compression--pruning)
    - [KV-Cache Compression / Retrieval / Reuse](#kv-cache-compression--retrieval--reuse)
    - [Retrieval-augmented Memory](#retrieval-augmented-memory)
    - [Semantic/Textual Abstraction](#semantictextual-abstraction)
    - [Event-centric Structured Memory](#event-centric-structured-memory)
    - [Spatial / 3D Memory](#spatial--3d-memory)
    - [Parametric / Fast-weight Memory](#parametric--fast-weight-memory)
  - [⚡ Real-time Inference](#-real-time-inference)
    - [Encoding-Decoding Parallelism](#encoding-decoding-parallelism)
    - [Selective Model Invocation](#selective-model-invocation)
    - [Visual Token Reduction](#visual-token-reduction)
    - [KV-Cache Optimization](#kv-cache-optimization)
  - [💭 Streaming with Thinking](#-streaming-with-thinking)
  - [📊 Benchmarks](#-benchmarks)
  - [📦 Training Datasets](#-training-datasets)
  - [📝 Survey](#-survey)
  - [🔗 Resources](#-resources)
  - [☎️ We're Hiring!](#️-were-hiring)

## 🛠️ Project
|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.06|JoyAI-VL-Interaction|[[html]](https://joyai-vl-video-future-academy-jd.github.io/JoyAI-VL-Interaction/)|[[GitHub]](https://github.com/jd-opensource/JoyAI-VL-Interaction/) ![](https://img.shields.io/github/stars/jd-opensource/JoyAI-VL-Interaction.svg?style=social)|An Open Real-time Video-Language Interaction System |
|2025.11|Live VLM WebUI|[[docs]](https://build.nvidia.com/spark/live-vlm-webui/overview)|[[GitHub]](https://github.com/NVIDIA-AI-IOT/live-vlm-webui) ![](https://img.shields.io/github/stars/NVIDIA-AI-IOT/live-vlm-webui.svg?style=social)|Real-Time Vision Language Model Interaction with Webcam Streaming |
|-|火山引擎（实时音视频）|[[html]](https://www.volcengine.com/docs/6348/1408245?lang=zh)|-|turn-based chat; 周期性发送 ExternalTextToLLM 触发主动响应 |

## 📋 Technical Report
|Date|Title|Paper|Code|Demo|Comment|
|:---:|:---:|:---:|:---:|:---:|:---:|
|2026.08|MOSS-VL Technical Report|[[pdf]](https://arxiv.org/pdf/2608.15045)|[[GitHub]](https://github.com/OpenMOSS/MOSS-VL) ![](https://img.shields.io/github/stars/OpenMOSS/MOSS-VL.svg?style=social)|[[demo]](https://openmoss.ai/MOSS-VL/)|Cross-attention vision-language architecture for full-duplex streaming interaction|
|2026.08|SeedRealtime: An Audio-Visual Full-Duplex LLM|[[html]](https://seed.bytedance.com/en/SeedRealtime)|-|-|Native audio-visual full-duplex interaction|
|2026.06|JoyAI-VL-Interaction|[[pdf]](https://arxiv.org/pdf/2606.14777v1)|[[GitHub]](https://github.com/jd-opensource/JoyAI-VL-Interaction/) ![](https://img.shields.io/github/stars/jd-opensource/JoyAI-VL-Interaction.svg?style=social)| [[demo]](https://joyai-vl-video-future-academy-jd.github.io/JoyAI-VL-Interaction/) |An Open Real-time Video-Language Interaction System |
|2026.05|Interaction Models: A Scalable Approach to Human-AI Collaboration (Thinking Machines Lab)| [[html]](https://thinkingmachines.ai/blog/interaction-models/)| - | - |Time-aligned micro-turns |
|2026.04|MiniCPM-o 4.5| [[pdf]](https://arxiv.org/pdf/2604.27393)|[[GitHub]](https://github.com/OpenBMB/MiniCPM-o-Demo) ![](https://img.shields.io/github/stars/OpenBMB/MiniCPM-o-Demo.svg?style=social)|[[demo]](https://minicpmo45.modelbest.cn/omni)|New Full-Duplex and Proactive Multimodal Live Streaming Capability|
|2026.03|Gemini 3.1 Flash Live| [[html]](https://ai.google.dev/gemini-api/docs/models/gemini-3.1-flash-live-preview)| - | [[demo]](https://aistudio.google.com/live?model=gemini-3.1-flash-live-preview) |turn-based chat |
|2026.04|Qwen3.5-Omni| [[pdf]](https://arxiv.org/pdf/2509.17765)|- |[[demo]](https://huggingface.co/spaces/Qwen/Qwen3.5-Omni-Online-Demo)|Adaptive Rate Interleave Alignment|
|2025.09|Qwen3-Omni| [[pdf]](https://arxiv.org/pdf/2604.15804)|[[GitHub]](https://github.com/QwenLM/Qwen3-Omni) ![](https://img.shields.io/github/stars/QwenLM/Qwen3-Omni.svg?style=social) ; [[aliyun]](https://github.com/aliyun/alibabacloud-bailian-speech-demo/tree/master/samples/conversation/omni) ![](https://img.shields.io/github/stars/aliyun/alibabacloud-bailian-speech-demo.svg?style=social)|[[demo]](https://huggingface.co/spaces/Qwen/Qwen3-Omni-Demo)|turn-based chat|
|2026.02|Seed2.0|[[pdf]](https://lf3-static.bytednsdoc.com/obj/eden-cn/lapzild-tss/ljhwZthlaukjlkulzlp/seed2/0214/Seed2.0%20Model%20Card.pdf)|[[GitHub]](https://github.com/ByteDance-Seed/Seed2.0) ![](https://img.shields.io/github/stars/ByteDance-Seed/Seed2.0.svg?style=social)|-|Doubao Video Calling; OVBench & LiveSports-3K & OVOBench & ODVBench & ViSpeak |
|2025.12|Seed1.8|[[pdf]](https://github.com/ByteDance-Seed/Seed-1.8/blob/main/Seed-1.8-Modelcard.pdf)|[[GitHub]](https://github.com/ByteDance-Seed/Seed-1.8) ![](https://img.shields.io/github/stars/ByteDance-Seed/Seed-1.8.svg?style=social)|-|Doubao Video Calling; OVBench & LiveSports-3K & OVOBench & ViSpeak & StreamingBench & OmniMMI |

## 💬 Proactive Interaction

### Auxiliary Response Head

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.05|StreamOV: Streaming Omni-Video Understanding via Evidence-Guided Memory and Response Triggering|[[pdf]](https://arxiv.org/pdf/2605.25621)|-|Cross-Attention Trigger over early-decoding hidden states with a trained Respond/Wait classification head|
|2026.03|Proact-VL: A Proactive VideoLLM for Real-Time AI Companions|[[pdf]](https://arxiv.org/pdf/2603.03447)|[[GitHub]](https://github.com/microsoft/AnthropomorphicIntelligence/tree/main/Proact-VL) ![](https://img.shields.io/github/stars/microsoft/AnthropomorphicIntelligence.svg?style=social)|\<\|FLAG\|\>Token Response Head with Transition-Smoothed Classification & Stability Regularization |
|2026.03|StreamReady: Learning What to Answer and When in Long Streaming Videos|[[pdf]](https://arxiv.org/pdf/2603.08620)|-|Learnable \<RDY\> Token with Readiness Head for Evidence-Gated Response Triggering |
|2025.05|StreamBridge: Turning Your Offline Video Large Language Model into a Proactive Streaming Assistant|[[pdf]](https://arxiv.org/pdf/2505.05467)|[[GitHub]](https://github.com/apple/ml-streambridge) ![](https://img.shields.io/github/stars/apple/ml-streambridge.svg?style=social)|Activation Model via \<ACT\> Token with Binary Score Head |
|2025.03|ViSpeak: Visual Instruction Feedback in Streaming Videos|[[pdf]](https://arxiv.org/pdf/2503.12769)|[[GitHub]](https://github.com/HumanMLLM/ViSpeak) ![](https://img.shields.io/github/stars/HumanMLLM/ViSpeak.svg?style=social)|Informative Head for \<seg\> Token |
|2025.03|StreamMind: Unlocking Full Frame Rate Streaming Video Dialogue through Event-Gated Cognition|[[pdf]](https://arxiv.org/pdf/2503.06220)|[[GitHub]](https://github.com/xinding-sys/StreamMind) ![](https://img.shields.io/github/stars/xinding-sys/StreamMind.svg?style=social)|Cognition Gate Network (Shallow Layer Transfer from LLM) for Binary \</response\> / \</silence\> Classification |
|2025.01|Dispider: Enabling Video LLMs with Active Real-Time Interaction via Disentangled Perception, Decision, and Reaction|[[pdf]](https://arxiv.org/pdf/2501.03218)|[[GitHub]](https://github.com/Mark12Ding/Dispider) ![](https://img.shields.io/github/stars/Mark12Ding/Dispider.svg?style=social)|Binary Classification Head on \<TODO\> Token Embedding (BCE Loss); \<ANS\> for History Marking; \<SILENT\> for Reaction-Stage Filtering |
|2024.11|VideoLLM Knows When to Speak: Enhancing Time-Sensitive Video Comprehension with Video-Text Duet Interaction Format|[[pdf]](https://arxiv.org/pdf/2411.17991)|[[GitHub]](https://github.com/yellow-binary-tree/mmduet) ![](https://img.shields.io/github/stars/yellow-binary-tree/mmduet.svg?style=social)|Informative Head & Relevance Head |

### Generative Token-based Trigger

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.06|Harnessing Streaming Video in the Wild|[[pdf]](https://arxiv.org/pdf/2606.08615v1)| - |Training Objective Targeting </silence> </response> |
|2026.04|AURA: Always-On Understanding and Real-Time Assistance via Video Streams|[[pdf]](https://arxiv.org/pdf/2604.04184)|[[GitHub]](https://github.com/aurateam2026/AURA) ![](https://img.shields.io/github/stars/aurateam2026/AURA.svg?style=social)|Unified \<\|silent\|\> Token for Silent Observation with Real-Time QA / Proactive QA / Multi-Response QA; Silent-Speech Balanced Loss |
|2026.03|STRIDE: When to Speak Meets Sequence Denoising for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2603.27593)|[[GitHub]](https://github.com/interlive-team/STRIDE) ![](https://img.shields.io/github/stars/interlive-team/STRIDE.svg?style=social)|Activation Token Denoising over 0/1/[M]; Sequence Duplication; Selective Re-masking|
|2025.12|Streaming Video Instruction Tuning|[[pdf]](https://arxiv.org/pdf/2512.21334)|[[GitHub]](https://github.com/maifoundations/Streamo) ![](https://img.shields.io/github/stars/maifoundations/Streamo.svg?style=social)|Three-State Response Tokens (\</Silence\>, \</Standby\>,\</Response\>) via Unified Next-Token Prediction; Focal Loss for Response Imbalance |
|2025.06|Proactive Assistant Dialogue Generation from Streaming Egocentric Videos|[[pdf]](https://arxiv.org/pdf/2506.05904)|[[GitHub]](https://github.com/pro-assist/ProAssist) ![](https://img.shields.io/github/stars/pro-assist/ProAssist.svg?style=social)|Frame-Level [EOS] Silence Prediction with Negative Frame Sub-Sampling |
|2025.03|LION-FS: Fast & Slow Video-Language Thinker as Online Video Assistant|[[pdf]](https://arxiv.org/pdf/2503.03663)|[[GitHub]](https://github.com/JiuTian-VL/LION-FS) ![](https://img.shields.io/github/stars/JiuTian-VL/LION-FS.svg?style=social)|Streaming EOS Prediction via Fast-Slow Dual-Path; Token Aggregation & Dropping Router for Visual Feature Compression |
|2025.03|AssistPDA: An Online Video Surveillance Assistant for Video Anomaly Prediction, Detection, and Analysis|[[pdf]](https://arxiv.org/pdf/2503.21904)|-|EOS Prediction with Task-Adaptive Threshold for Anomaly Alerting |
|2024.07|What to Say and When to Say it: Live Fitness Coaching as a Testbed for Situated Interaction|[[pdf]](https://arxiv.org/pdf/2407.08101)|[[GitHub]](https://github.com/Qualcomm-AI-research/FitCoach) ![](https://img.shields.io/github/stars/Qualcomm-AI-research/FitCoach.svg?style=social)|Action Tokens \<next\> and \<feedback\> |
|2024.06|VideoLLM-online: Online Video Large Language Model for Streaming Video|[[pdf]](https://arxiv.org/pdf/2406.11816)|[[GitHub]](https://github.com/showlab/videollm-online) ![](https://img.shields.io/github/stars/showlab/videollm-online.svg?style=social)|Streaming EOS Token Prediction |

### RL-optimized Proactive Response

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.05|StreamPro: From Reactive Perception to Proactive Decision-Making in Streaming Video|[[pdf]](https://arxiv.org/pdf/2605.16381)|-|Two-stage proactive training with CB-Stream Loss for SFT and GRPO with turn-level & trajectory-level rewards |
|2026.03|Thinking in Streaming Video|[[pdf]](https://arxiv.org/pdf/2603.12938)|[[GitHub]](https://github.com/johncaged/ThinkStream) ![](https://img.shields.io/github/stars/johncaged/ThinkStream.svg?style=social)|Watch-Think-Speak with \<silent\> & \<response\> Action Tokens; Streaming RLVR (Format + Time + Accuracy Reward) |
|2026.01|Learning to Respond: A Large-Scale Benchmark and Progressive Learning Framework for Trigger-Centric Online Video Understanding|[[pdf]](https://openreview.net/pdf?id=gmpnSSiJt7)|-|Trigger-Centric Online Video Understanding |
|2025.12|MMDuet2: Enhancing Proactive Interaction of Video MLLMs with Multi-Turn Reinforcement Learning|[[pdf]](https://arxiv.org/pdf/2512.06810)|[[GitHub]](https://github.com/yellow-binary-tree/MMDuet2) ![](https://img.shields.io/github/stars/yellow-binary-tree/MMDuet2.svg?style=social)|Text-to-Text "NO REPLY" Response Decision with Multi-Objective Reward (PAUC + Replication + In-Span + Prefix) GRPO |

### Training-free / Feature-based Trigger

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.06|LiveStarPro: Proactive Streaming Video Understanding with Hierarchical Memory for Long-Horizon Streams|[[pdf]](https://arxiv.org/pdf/2606.17798)|[[GitHub]](https://github.com/sotayang/LiveStar) ![](https://img.shields.io/github/stars/sotayang/LiveStar.svg?style=social)|Inference-Time Streaming Verification Decoding (SVeD) for Response/Silence Decisions |
|2026.05|Response-G1: Explicit Scene Graph Modeling for Proactive Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.07575)|-|Fine-Tuning-Free Retrieval-Augmented Trigger Prompting with Query-Guided Scene Graph Evidence|
|2026.03|FluxMem: Adaptive Hierarchical Memory for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2603.02096)|[[GitHub]](https://github.com/YiwengXie/FluxMem) ![](https://img.shields.io/github/stars/YiwengXie/FluxMem.svg?style=social)|Scene-Change Ratio Trigger Reusing Temporal Adjacency Selection Statistics |
|2026.01|QueryStream: Advancing Streaming Video Understanding with Query-Aware Pruning and Proactive Response|[[pdf]](https://openreview.net/pdf?id=738HjJEbml)|-|Relevance-Triggered Active Response |
|2026.01|Event-VStream: Event-Driven Real-Time Understanding for Long Video Streams|[[pdf]](https://arxiv.org/pdf/2601.15655)|-|Motion-Semantic-Prediction Boundary Score; Adaptive Threshold; Event-triggered Decoding |
|2025.11|LiveStar: Live Streaming Assistant for Real-World Online Video Understanding|[[pdf]](https://arxiv.org/pdf/2511.05299)|[[GitHub]](https://github.com/sotayang/LiveStar) ![](https://img.shields.io/github/stars/sotayang/LiveStar.svg?style=social)|Streaming Verification Decoding Perplexity Gate for Response & Silence |
|2025.08|StreamAgent: Towards Anticipatory Agents for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2508.01875)|-|Reactive/Proactive/Speculative Planning; Heuristic Trigger; Tool-Guided Information Hunting |

### Hybrid Trigger Framework

|  Date   |                            Title                             |                   Paper                   |                             Code                             |                           Comment                            |
| :-----: | :----------------------------------------------------------: | :---------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| 2026.03 | Em-Garde: A Propose-Match Framework for Proactive Streaming Video Understanding | [[pdf]](https://arxiv.org/pdf/2603.19054) | [[GitHub]](https://github.com/air-embodied-brain/Em-Garde) ![](https://img.shields.io/github/stars/air-embodied-brain/Em-Garde.svg?style=social) | Query-Time Instruction-Guided Visual Proposal Generation (SFT+GRPO); Lightweight Embedding Cosine Similarity Surge Triggering |
| 2026.03 |                StreamingClaw Technical Report                | [[pdf]](https://arxiv.org/pdf/2603.22120) |                              -                               | Training-Free (Reminder Node); Training-Based (Scenario-Specific Trigger Tokens) |

### Learned Response Timing

|  Date   |                            Title                             |                   Paper                   |                             Code                             |                           Comment                            |
| :-----: | :----------------------------------------------------------: | :---------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| 2026.05 | An Efficient Streaming Video Understanding Framework with Agentic Control | [[pdf]](https://arxiv.org/pdf/2605.17921) | - | R3-Streaming Readiness Head Emits \<Routine\> to Defer Responses until Sufficient Evidence Arrives |
| 2026.04 | Progressive Online Video Understanding with Evidence-Aligned Timing and Transparent Decisions | [[pdf]](https://arxiv.org/pdf/2604.18459) | - | Thinking-QwenVL with Active Thinking Decision Maker (progress/confidence) for Evidence-Aligned Response Timing |
| 2025.10 | Eyes Wide Open: Ego Proactive Video-LLM for Streaming Video  | [[pdf]](https://arxiv.org/pdf/2510.14560) | [[GitHub]](https://github.com/SooLab/EyeWO) ![](https://img.shields.io/github/stars/SooLab/EyeWO.svg?style=social) | Weighted Interval Supervision & Uncertainty-Guided High-Resolution Requests |
| 2025.02 | EgoSpeak: Learning When to Speak for Egocentric Conversational Agents in the Wild | [[pdf]](https://arxiv.org/pdf/2502.14892) | [[GitHub]](https://github.com/jun297/EgoSpeak) ![](https://img.shields.io/github/stars/jun297/EgoSpeak.svg?style=social) | Standalone Audio-Visual Frame-Level Three-Way Classifier (Background / Self / Other) with Anticipatory Prediction |

## 🧠 Long-term Memory Management

### Hierarchical Multi-level Memory

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.08|StreamFlow: Dynamic Memory Flows for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2608.10949)|-|Dynamics-Aware Mid-Term Memory with Pre-Encoding Redundancy Filtering + Fixed-Capacity Latent Long-Term Memory |
|2026.06|LiveStarPro: Proactive Streaming Video Understanding with Hierarchical Memory for Long-Horizon Streams|[[pdf]](https://arxiv.org/pdf/2606.17798)|[[GitHub]](https://github.com/sotayang/LiveStar) ![](https://img.shields.io/github/stars/sotayang/LiveStar.svg?style=social)|Tree-Structured Hierarchical Memory (TSHM) for Long-Horizon Streaming on Existing LiveStar-8B Weights |
|2026.06|Harnessing Streaming Video in the Wild|[[pdf]](https://arxiv.org/pdf/2606.08615v1)| - |short-term memory; mid-term memory; long-term memory; enabling up to 12 hours of context |
|2026.05|StreamOV: Streaming Omni-Video Understanding via Evidence-Guided Memory and Response Triggering|[[pdf]](https://arxiv.org/pdf/2605.25621)|-|Multimodal evidence-guided long-short term memory with dense recent observations and sparse historical evidence under a fixed budget |
|2026.05|Semantic-Aware Adaptive Visual Memory for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.07897)|[[GitHub]](https://github.com/wuhang03/savemem) ![](https://img.shields.io/github/stars/wuhang03/savemem.svg?style=social)|Training-Free Three-Tier Memory with Semantic-Prior-Guided Selective Forgetting & Query-Adaptive Retrieval Scope |
|2026.04|Progressive Online Video Understanding with Evidence-Aligned Timing and Transparent Decisions|[[pdf]](https://arxiv.org/pdf/2604.18459)|-|Hierarchical Progressive Semantic Integration (HPSI) with Learnable Multi-Level Aggregation Tokens Propagated across Clips |
|2026.03|CurveStream: Boosting Streaming Video Understanding in MLLMs via Curvature-Aware Hierarchical Visual Memory Management|[[pdf]](https://arxiv.org/pdf/2603.19571)|-|Curvature-Aware Scorer (Motion Variation + Geometric Curvature); EMA-Based K-Sigma Dynamic Thresholding; Hierarchical Clear/Blurred/Discard Memory with FIFO Eviction|
|2026.03|StreamingClaw Technical Report|[[pdf]](https://arxiv.org/pdf/2603.22120)|-|Hierarchical Memory Evolution |
|2026.03|StreamReady: Learning What to Answer and When in Long Streaming Videos|[[pdf]](https://arxiv.org/pdf/2603.08620)|-|3-Level Visual Memory Tree (FIFO-Centroid-Prototype) & Contextual Memory Bank |
|2026.03|WAT: Online Video Understanding Needs Watching Before Thinking|[[pdf]](https://arxiv.org/pdf/2603.13412)|-|Dual-Level Memory: Short-Term FIFO Queue + Long-Term Memory with Redundancy-Aware Eviction Policy |
|2026.03|Scaling the Long Video Understanding of Multimodal Large Language Models via Visual Memory Mechanism|[[pdf]](https://arxiv.org/pdf/2603.29252)|[[GitHub]](https://github.com/city1517/FlexMem) ![](https://img.shields.io/github/stars/city1517/FlexMem.svg?style=social)|Dual-Pathway Compression for Context Memory and Local Memory; Visual KV-Cache Memory Bank; Cross-attention Memory Recall & MemIndex |
|2026.03|FluxMem: Adaptive Hierarchical Memory for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2603.02096)|[[GitHub]](https://github.com/YiwengXie/FluxMem) ![](https://img.shields.io/github/stars/YiwengXie/FluxMem.svg?style=social)|Three-Level Hierarchical Memory (Short/Mid/Long-Term); Temporal Adjacency Selection & Spatial Domain Consolidation |
|2026.02|FreshMem: Brain-Inspired Frequency-Space Hybrid Memory for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2602.01683)|-|Short-term Sliding Window + Multi-scale Frequency Memory + Space Thumbnail Memory |
|2026.01|HERMES: KV Cache as Hierarchical Memory for Efficient Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2601.14724)|[[GitHub]](https://github.com/haowei-freesky/HERMES) ![](https://img.shields.io/github/stars/haowei-freesky/HERMES.svg?style=social)|Hierarchical KV-Cache (Sensory-Working-Long-Term Memory); Exponential Forgetting Curve & Frame-Level Anchor Tokens; Cross-Layer Memory Smoothing & Position Re-Indexing |
|2025.12|Venus: An Efficient Edge Memory-and-Retrieval System for VLM-based Online Video Understanding|[[pdf]](https://arxiv.org/pdf/2512.07344)|-|Hierarchical Raw Data Layer & Semantic Index Layer; Scene Segmentation and Incremental Clustering for Sparse Memory Construction |
|2025.08|StreamAgent: Towards Anticipatory Agents for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2508.01875)|-|Streaming KV-Cache; CPU Long-Term & GPU Short-Term Hierarchical Memory; Layer-Adaptive KV Recall |
|2025.07|StreamVLN: Streaming Vision-and-Language Navigation via SlowFast Context Modeling|[[pdf]](https://arxiv.org/pdf/2507.05240)|[[GitHub]](https://github.com/InternRobotics/StreamVLN) ![](https://img.shields.io/github/stars/InternRobotics/StreamVLN.svg?style=social)|Sliding-Window KV-Cache with Selective Offloading; 3D Voxel-Based Spatial Token Pruning for Cross-Frame Redundancy Removal |
|2025.01|Streaming Video Understanding and Multi-round Interaction with Memory-enhanced Knowledge|[[pdf]](https://arxiv.org/pdf/2501.13468)|[[GitHub]](https://github.com/hmxiong/StreamChat) ![](https://img.shields.io/github/stars/hmxiong/StreamChat.svg?style=social)|Hierarchical Memory: Ebbinghaus Forgetting Curve Short-Term + Tree-Structured Clustering Long-Term + FAISS Dialogue Memory; Forgetting Probability-Based Frame Sampling |
|2024.09|VideoLLaMB: Long Streaming Video Understanding with Recurrent Memory Bridges|[[pdf]](https://arxiv.org/pdf/2409.01071)|[[GitHub]](https://github.com/bigai-nlco/VideoLLaMB) ![](https://img.shields.io/github/stars/bigai-nlco/VideoLLaMB.svg?style=social)|Recurrent Memory Bridge with Self-Attention Recursive Update & Retrieval Attention; SceneTiling Semantic Segmentation; Linear Memory Scaling |

### Sliding-window / Eviction

|  Date   |                            Title                             |                   Paper                   |                             Code                             |                           Comment                            |
| :-----: | :----------------------------------------------------------: | :---------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| 2026.04 | AURA: Always-On Understanding and Real-Time Assistance via Video Streams | [[pdf]](https://arxiv.org/pdf/2604.04184) | [[GitHub]](https://github.com/aurateam2026/AURA) ![](https://img.shields.io/github/stars/aurateam2026/AURA.svg?style=social) | Dual Sliding-Window Context over Recent Video and QA History; Out-of-Window Video Chunks and \<\|silent\|\> Tokens Discarded |
| 2026.04 |     A Simple Baseline for Streaming Video Understanding      | [[pdf]](https://arxiv.org/pdf/2604.02317) | [[GitHub]](https://github.com/EvolvingLMMs-Lab/SimpleStream)![](https://img.shields.io/github/stars/EvolvingLMMs-Lab/SimpleStream.svg?style=social) | Fixed Recent-frame Sliding Window; Old-frame Eviction without External Memory |
| 2026.03 | Proact-VL: A Proactive VideoLLM for Real-Time AI Companions  | [[pdf]](https://arxiv.org/pdf/2603.03447) | [[GitHub]](https://github.com/microsoft/AnthropomorphicIntelligence/tree/main/Proact-VL) ![](https://img.shields.io/github/stars/microsoft/AnthropomorphicIntelligence.svg?style=social) | Dual-Cache (System & Streaming) Sliding Window with Reverse-RoPE Eviction for Infinite Streaming |
| 2026.03 | STRIDE: When to Speak Meets Sequence Denoising for Streaming Video Understanding | [[pdf]](https://arxiv.org/pdf/2603.27593) | [[GitHub]](https://github.com/interlive-team/STRIDE) ![](https://img.shields.io/github/stars/interlive-team/STRIDE.svg?style=social) | Bounded Visual Cache Eviction; Sliding-window Frame Retention |

### Token Compression / Pruning

|  Date   |                            Title                             |                   Paper                   |                             Code                             |                           Comment                            |
| :-----: | :----------------------------------------------------------: | :---------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| 2026.06 | Towards a Dynamic and Fixed-budget Memory Bank for Efficient Streaming Video Understanding | [[pdf]](https://arxiv.org/pdf/2606.25658) | [[GitHub]](https://github.com/hktk07/CausalMem) ![](https://img.shields.io/github/stars/hktk07/CausalMem.svg?style=social) | Training-Free Fixed-Budget Memory Bank with Online Semantic Basis for Causal Visual Token Selection |
| 2026.05 | An Efficient Streaming Video Understanding Framework with Agentic Control | [[pdf]](https://arxiv.org/pdf/2605.17921) | - | Training-Free Active Forgetting with High-Fidelity Recent Tokens and Aggressive Historical Compression |
| 2025.10 | Recurrent Attention-based Token Selection for Efficient Streaming Video-LLMs | [[pdf]](https://arxiv.org/pdf/2510.17364) |                              -                               | Attention-Score-Based Visual Token Selection with Recurrent FIFO Token Queue; Maximal Marginal Relevance Caption Retrieval |
| 2025.05 | StreamBridge: Turning Your Offline Video Large Language Model into a Proactive Streaming Assistant | [[pdf]](https://arxiv.org/pdf/2505.05467) | [[GitHub]](https://github.com/apple/ml-streambridge) ![](https://img.shields.io/github/stars/apple/ml-streambridge.svg?style=social) | Producer-Consumer Memory Buffer with Conditional Round-Decayed Token Compression (Prioritizing Recent Frames) |
| 2025.04 | TimeChat-Online: 80% Visual Tokens are Naturally Redundant in Streaming Videos | [[pdf]](https://arxiv.org/pdf/2504.17343) | [[GitHub]](https://github.com/yaolinli/TimeChat-Online) ![](https://img.shields.io/github/stars/yaolinli/TimeChat-Online.svg?style=social) | Differential Token Drop (Primary); FIFO Slimmed Token Memory Bank (Supplementary) |
| 2025.03 | VideoScan: Enabling Efficient Streaming Video Understanding via Frame-level Semantic Carriers | [[pdf]](https://arxiv.org/pdf/2503.09387) | [[GitHub]](https://github.com/LyliAgave/VideoScan) ![](https://img.shields.io/github/stars/LyliAgave/VideoScan.svg?style=social) | Single Semantic Carrier Token per Frame (Avg-Pool Embedding + Reused KV Aggregation); Cosine Similarity-Based Dynamic Memory Bank Eviction |

### KV-Cache Compression / Retrieval / Reuse

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.05|CoRDS: Coreset-based Representative and Diverse Selection for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.14310)|[[GitHub]](https://github.com/ailarmhz/CoRDS) ![](https://img.shields.io/github/stars/ailarmhz/CoRDS.svg?style=social)|Training-Free KV-Cache Coreset Selection with Joint K/V Coverage, Diversity & Recency Protection |
|2026.05|Decouple and Cache: KV Cache Construction for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.01858)|[[GitHub]](https://github.com/pangzhan27/DSCache) ![](https://img.shields.io/github/stars/pangzhan27/DSCache.svg?style=social)|Decoupled Streaming Cache (DSCache): Cumulative Past KV Cache + On-Demand Instant Cache with Position-Agnostic Encoding |
|2026.02|Going Down Memory Lane: Scaling Tokens for Video Stream Understanding with Dynamic KV-Cache Memory|[[pdf]](https://arxiv.org/pdf/2602.18434)|[[GitHub]](https://github.com/vatsalag99/MemStream) ![](https://img.shields.io/github/stars/vatsalag99/MemStream.svg?style=social)|Adaptive Key Selection for Sparse Sliding-Window Encoding; Training-Free Retrieval MoE via Reciprocal Rank Fusion of Internal & External Signals|
|2025.12|V-Rex: Real-Time Streaming Video LLM Acceleration via Dynamic KV Cache Retrieval|[[pdf]](https://arxiv.org/pdf/2512.12284)|-|Hash-Bit Hamming Clustering & Weighted Cumulative Sum Early-Exit Thresholding for Dynamic KV-Cache Retrieval; Hierarchical Memory Offloading |
|2025.11|StreamKV: Streaming Video Question-Answering with Segment-based KV Cache Retrieval and Compression|[[pdf]](https://arxiv.org/pdf/2511.07278)|[[GitHub]](https://github.com/sou1p0wer/StreamKV) ![](https://img.shields.io/github/stars/sou1p0wer/StreamKV.svg?style=social)|Cosine Similarity-Based Dynamic Semantic Segmentation; Summary-Vector Representative Key Retrieval; Guidance-Prompt-Driven KV Compression with Layer-Adaptive Budget Allocation |
|2025.11|LiveStar: Live Streaming Assistant for Real-World Online Video Understanding|[[pdf]](https://arxiv.org/pdf/2511.05299)|[[GitHub]](https://github.com/sotayang/LiveStar) ![](https://img.shields.io/github/stars/sotayang/LiveStar.svg?style=social)|Peak-End Memory Compression & Dual-Level Streaming KV Cache |
|2025.10|StreamingTOM: Streaming Token Compression for Efficient Video Understanding|[[pdf]](https://arxiv.org/pdf/2510.18269)|[[GitHub]](https://github.com/YIGE24/StreamingTOM) ![](https://img.shields.io/github/stars/YIGE24/StreamingTOM.svg?style=social)|Causal Temporal Token Reduction (Static-Dynamic DPC & Attention Selection) + Online 4-bit Quantized KV Memory with Representative-Key Retrieval |
|2025.08|StreamMem: Query-Agnostic KV Cache Memory for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2508.15717)|-|Chat Template Proxy Query for Query-Agnostic KV-Cache Pruning & Weighted Merging |
|2025.06|InfiniPot-V: Memory-Constrained KV Cache Compression for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2506.15745)|[[GitHub]](https://github.com/aiha-lab/InfiniPot-V) ![](https://img.shields.io/github/stars/aiha-lab/InfiniPot-V.svg?style=social)|KV-Cache Compression with Temporal-Axis Redundancy Pruning & Value-Norm Ranking with Layer-Adaptive Pooling |
|2025.05|LiveVLM: Efficient Online Video Understanding via Streaming-Oriented KV Cache and Retrieval|[[pdf]](https://arxiv.org/pdf/2505.15269)|-|Streaming-Oriented KV Cache with Video-Specific KV Compression; Frame-Wise KV Merging & FIFO KV Chunk Memory |

### Retrieval-augmented Memory

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.06|What Should a Streaming Video Model Remember?|[[pdf]](https://arxiv.org/pdf/2606.16353)|-|SelectStream with Surprise-Driven Writing, Priority-Preserving Latent Memory Graph & Query-Conditioned Graph Retrieval |
|2026.05|Response-G1: Explicit Scene Graph Modeling for Proactive Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.07575)|-|Query-Guided Scene Graph Memory with Top-K Similarity Retrieval|
|2026.04|OASIS: On-Demand Hierarchical Event Memory for Streaming Video Reasoning|[[pdf]](https://arxiv.org/pdf/2604.17052)|[[GitHub]](https://github.com/Solus-sano/OASIS) ![](https://img.shields.io/github/stars/Solus-sano/OASIS.svg?style=social)|On-Demand Retrieval over Hierarchical Event Memory; Uncertainty-Triggered Controlled Refinement |
|2026.03|PEARL: Personalized Streaming Video Understanding Model|[[pdf]](https://arxiv.org/pdf/2603.20422)|[[GitHub]](https://github.com/Yuanhong-Zheng/PEARL) ![](https://img.shields.io/github/stars/Yuanhong-Zheng/PEARL.svg?style=social)|Dual-Grained Memory (Streaming Memory + Concept Memory); Concept-Aware Retrieval with Query Rewriting for Personalized Concept Grounding|
|2026.02|Vista: Scene-Aware Optimization for Streaming Video Question Answering under Post-Hoc Queries|[[pdf]](https://arxiv.org/pdf/2602.08448)|                              -                               |Scene-aware Segmentation; Temporal-Spatial Scene Token Compression; CPU Offloaded Full Frames with Query-conditioned Top-k Recall|
|2026.02|WeaveTime: Stream from Earlier Frames into Emergent Memory in VideoLLMs|[[pdf]](https://arxiv.org/pdf/2602.22142)| [[GitHub]](https://github.com/zhangyl4/weavetime) ![](https://img.shields.io/github/stars/zhangyl4/weavetime.svg?style=social) |Uncertainty-Gated Hierarchical Retrieval with Entropy-Threshold Triggered Past Context Access|
|2025.12|CogStream: Context-guided Streaming Video Question Answering|[[pdf]](https://arxiv.org/pdf/2506.10516)| [[GitHub]](https://github.com/LiamZhao326/CogStream) ![](https://img.shields.io/github/stars/LiamZhao326/CogStream.svg?style=social) |Temporal-Semantic Clustering with Question-Aware Event Compression; Historical Dialogue Retrieval via LLM Selection|
|2025.11|CacheFlow: Compressive Streaming Memory for Efficient Long-Form Video Understanding|[[pdf]](https://arxiv.org/pdf/2511.13644)|-|Dynamic Token Dropping; GRU-Based Compressive Memory; KV Offloading and Rehydration; Consensus-First Retrieval |
|2025.06|Flash-VStream: Efficient Real-Time Understanding for Long Video Streams|[[pdf]](https://arxiv.org/pdf/2506.23825)|[[GitHub]](https://github.com/IVGSZ/Flash-VStream) ![](https://img.shields.io/github/stars/IVGSZ/Flash-VStream.svg?style=social)|K-Means Clustered Context Synopsis Memory & Feature-Centric Detail Augmentation Memory with Disk-Offloadable Feature Bank |
|2025.03|Streaming Video Question-Answering with In-context Video KV-Cache Retrieval|[[pdf]](https://arxiv.org/pdf/2503.00540)|[[GitHub]](https://github.com/Becomebright/ReKV) ![](https://img.shields.io/github/stars/Becomebright/ReKV.svg?style=social)|Sliding-Window Encoding with KV-Cache Offloading to RAM/Disk; Internal (Self-Attention Key Averaging) & External (CLIP Cosine Similarity) Frame-Level Retrieval |

### Semantic/Textual Abstraction

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.07|FOLIO: Focused Semantic Memory for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2607.13298)|-|Training-Free Focus-Aware Writing with Short-Term Visual Buffer, Entity-Centered Semantic Memory & Evidence Cache |
|2026.04|StreamMeCo: Long-Term Agent Memory Compression for Efficient Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2604.09000)|[[GitHub]](https://github.com/Celina-love-sweet/StreamMeCo) ![](https://img.shields.io/github/stars/Celina-love-sweet/StreamMeCo.svg?style=social)|Connectivity-Aware Compression of Text/Face/Voice Memory Graph Nodes with Time-Decay Retrieval |
|2026.03|Click-to-Ask: An AI Live Streaming Assistant with Offline Copywriting and Online Interactive QA|[[pdf]](https://arxiv.org/pdf/2603.18649)|-|Streaming Event Segmentation; Event-level Historical Caption Memory; Knowledge Extraction Accelerator|
|2026.03|Thinking in Streaming Video|[[pdf]](https://arxiv.org/pdf/2603.12938)|[[GitHub]](https://github.com/johncaged/ThinkStream) ![](https://img.shields.io/github/stars/johncaged/ThinkStream.svg?style=social)|Reasoning-Compressed Streaming Memory: Visual Sliding Window + Reasoning Tokens as Long-Term Semantic Anchors |
|2026.03|Video Streaming Thinking: VideoLLMs Can Watch and Think Simultaneously|[[pdf]](https://arxiv.org/pdf/2603.12262)|[[GitHub]](https://github.com/1ranGuan/VST) ![](https://img.shields.io/github/stars/1ranGuan/VST.svg?style=social)|Short-Term Visual Sliding Window & Long-Term Textual Streaming-Thought Memory with FIFO Eviction; Recursive Temporal Segmentation |
|2026.02|Exploring Multimodal LMMs for Online Episodic Memory Question Answering on the Edge|[[pdf]](https://arxiv.org/pdf/2602.22455)|-|Convert Video into a Lightweight Textual Memory |
|2025.06|Proactive Assistant Dialogue Generation from Streaming Egocentric Videos|[[pdf]](https://arxiv.org/pdf/2506.05904)|[[GitHub]](https://github.com/pro-assist/ProAssist) ![](https://img.shields.io/github/stars/pro-assist/ProAssist.svg?style=social)|Iterative Progress Summarization as Summary-Based Memory Compression |
|2025.04|Memory-efficient Streaming VideoLLMs for Real-time Procedural Video Understanding|[[pdf]](https://arxiv.org/pdf/2504.13915)|[[GitHub]](https://github.com/dibschat/ProVideLLM) ![](https://img.shields.io/github/stars/dibschat/ProVideLLM.svg?style=social)|Multimodal Interleaved Cache: Online Verbalization of Visual-to-Text for Long-Term & Short-Term Visual Tokens |

### Event-centric Structured Memory

|  Date   |                            Title                             |                   Paper                   |                             Code                             |                           Comment                            |
| :-----: | :----------------------------------------------------------: | :---------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| 2026.08 | StreamArena: Toward Continuous, Interactive, and Long-Horizon Agentic Streaming Video Understanding | [[pdf]](https://arxiv.org/pdf/2608.05703) | - | StreamMind Hierarchical Event Memory + Entity Relation Graph + Key Frames with Asynchronous Memory Writing |
| 2026.07 | ObjectStream: Latent Objects as Memory Anchors for Streaming Video Understanding | [[pdf]](https://arxiv.org/pdf/2607.28312) | [[GitHub]](https://github.com/DMK041218/ObjectStream) ![](https://img.shields.io/github/stars/DMK041218/ObjectStream.svg?style=social) | Training-Free Latent Object Anchors with Cross-Frame Association, Persistent Tracks & State-Change Retention |
| 2026.04 | OASIS: On-Demand Hierarchical Event Memory for Streaming Video Reasoning | [[pdf]](https://arxiv.org/pdf/2604.17052) | [[GitHub]](https://github.com/Solus-sano/OASIS) ![](https://img.shields.io/github/stars/Solus-sano/OASIS.svg?style=social) | Hierarchical Event Memory with Intent-Driven Retrieval and Plug-and-Play Training-Free Reasoning |
| 2026.02 | EventMemAgent: Hierarchical Event-Centric Memory for Online Video Understanding with Adaptive Tool Use | [[pdf]](https://arxiv.org/pdf/2602.15329) | [[GitHub]](https://github.com/lingcco/EventMemAgent) ![](https://img.shields.io/github/stars/lingcco/EventMemAgent.svg?style=social) | Event-Centric Dual-Layer Memory (STM with Online Event Segmentation & Reservoir Sampling + LTM with Structured Event Tuples) |
| 2026.01 | Event-VStream: Event-Driven Real-Time Understanding for Long Video Streams | [[pdf]](https://arxiv.org/pdf/2601.15655) |                              -                               | Event-level Memory Bank; Merge-or-Append Event Consolidation |
| 2025.12 | VideoScaffold: Elastic-Scale Visual Hierarchies for Streaming Video Understanding in MLLMs | [[pdf]](https://arxiv.org/pdf/2512.22226) | [[GitHub]](https://github.com/zheng980629/VideoScaffold) ![](https://img.shields.io/github/stars/zheng980629/VideoScaffold.svg?style=social) | Prediction-Guided Elastic-Scale Event Segmentation & Hierarchical Cross-Attention Event Consolidation |
| 2025.09 | StreamForest: Efficient Online Video Understanding with Persistent Event Memory | [[pdf]](https://arxiv.org/pdf/2509.24871) | [[GitHub]](https://github.com/MCG-NJU/StreamForest) ![](https://img.shields.io/github/stars/MCG-NJU/StreamForest.svg?style=social) | Event-Level Tree Hierarchy with Adaptive Merging via Similarity & Merge-Count & Temporal Penalty; Short-Term Spatiotemporal Sliding Window |

### Spatial / 3D Memory

|  Date   |                            Title                             |                   Paper                   |                             Code                             |                           Comment                            |
| :-----: | :----------------------------------------------------------: | :---------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| 2026.01 | OnlineSI: Taming Large Language Model for Online 3D Understanding and Grounding | [[pdf]](https://arxiv.org/pdf/2601.16538) | [[GitHub]](https://github.com/StoreBlank/online-spatial-intelligence) ![](https://img.shields.io/github/stars/StoreBlank/online-spatial-intelligence.svg?style=social) | Fixed-size Spatial Memory with Time-adaptive Sampling and Concatenation; Explicit Point Cloud and Semantic Memory |

### Parametric / Fast-weight Memory

|  Date   |                            Title                             |                   Paper                   |                             Code                             |                           Comment                            |
| :-----: | :----------------------------------------------------------: | :---------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| 2026.08 | StreamTTT: Reconciling Real-Time Perception and Long-Term Memory in Streaming VLMs | [[pdf]](https://arxiv.org/pdf/2608.13416) | - | Parallel Gated TTT Fast-Weight Memory for Long-Range History outside the Short Sliding Attention Context |
| 2025.10 | video-SALMONN S: Streaming Audio-Visual LLMs Beyond Length Limits via Memory | [[pdf]](https://arxiv.org/pdf/2510.11129) | [[GitHub]](https://github.com/bytedance/SALMONN/tree/video-salmonn-S) ![](https://img.shields.io/github/stars/bytedance/SALMONN.svg?style=social) | Test-Time Training Fast-Weight MLP as Streaming Memory with Dual (Reconstruction + Long-Span Prediction) Objective; Cosine Similarity Token Discarding; Prompt-Dependent Modality-Aware KV-Cache Chunk Reading |

## ⚡ Real-time Inference

### Encoding-Decoding Parallelism

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.03|Think-as-You-See: Streaming Chain-of-Thought Reasoning for Large Vision-Language Models|[[pdf]](https://arxiv.org/pdf/2603.02872)|[[GitHub]](https://github.com/EIT-NLP/StreamingLLM/tree/main/TaYS) ![](https://img.shields.io/github/stars/EIT-NLP/StreamingLLM.svg?style=social)|Parallel Dual KV-Cache with Merge-Generate-Split Loop for Concurrent Encoding-Decoding; Decoupled Cross-Modal RoPE; Near-Zero Time-to-First-Token|
|2026.03|Think While Watching: Online Streaming Segment-Level Memory for Multi-Turn Video Reasoning in MLLMs|[[pdf]](https://arxiv.org/pdf/2603.11896)|[[GitHub]](https://github.com/wl666hhh/Think_While_Watching) ![](https://img.shields.io/github/stars/wl666hhh/Think_While_Watching.svg?style=social)|Threaded Parallel Watch-Think Pipeline with Async Segment Prefetch & Adaptive Attention Backend |
|2026.01|Speak While Watching: Unleashing TRUE Real-Time Video Understanding Capability of Multimodal Large Language Models|[[pdf]](https://arxiv.org/pdf/2601.06843)|[[GitHub]](https://github.com/EIT-NLP/Speak-While-Watching) ![](https://img.shields.io/github/stars/EIT-NLP/Speak-While-Watching.svg?style=social)|Decoupled Positional Encoding (Overlapped / Group-Decoupled / Gap-Isolated) for Parallel Perception-Generation Streaming |

### Selective Model Invocation

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.05|An Efficient Streaming Video Understanding Framework with Agentic Control|[[pdf]](https://arxiv.org/pdf/2605.17921)|-|TB-GRPO Fast/Slow Model Routing with Target-Band Control over Heavy-Model Escalation Frequency |
|2026.03|STRIDE: When to Speak Meets Sequence Denoising for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2603.27593)|[[GitHub]](https://github.com/interlive-team/STRIDE) ![](https://img.shields.io/github/stars/interlive-team/STRIDE.svg?style=social)|Two-stage Activation-to-Generation Pipeline; Event-gated Downstream Video-LLM Invocation|
|2026.03|Color When It Counts: Grayscale-Guided Online Triggering for Always-On Streaming Video Sensing|[[pdf]](https://arxiv.org/pdf/2603.22466)|[[GitHub]](https://github.com/lvgd/ColorTrigger) ![](https://img.shields.io/github/stars/lvgd/ColorTrigger.svg?style=social)|Windowed Grayscale Affinity Analysis with Quadratic Programming; Credit-Budgeted RGB Activation; Dynamic Token Router with Asymmetric Grayscale and RGB Token Capacity |
|2026.03|StreamMind: Unlocking Full Frame Rate Streaming Video Dialogue through Event-Gated Cognition|[[pdf]](https://arxiv.org/pdf/2503.06220)|[[GitHub]](https://github.com/xinding-sys/StreamMind) ![](https://img.shields.io/github/stars/xinding-sys/StreamMind.svg?style=social)|SSM-Based Single-Token Perception with Event-Gated Sparse LLM Invocation |
|2026.01|Event-VStream: Event-Driven Real-Time Understanding for Long Video Streams|[[pdf]](https://arxiv.org/pdf/2601.15655)|-|Boundary-aware Event Pooling; Event-triggered Sparse Decoding; Hysteresis Pacing Control |
|2025.09|Open-ended Hierarchical Streaming Video Understanding with Vision Language Models|[[pdf]](https://arxiv.org/pdf/2509.12145)|-|Lightweight RNN Streaming Module with Event-Gated Sparse Frozen VLM Invocation |
|2025.03|LION-FS: Fast & Slow Video-Language Thinker as Online Video Assistant|[[pdf]](https://arxiv.org/pdf/2503.03663)|[[GitHub]](https://github.com/JiuTian-VL/LION-FS) ![](https://img.shields.io/github/stars/JiuTian-VL/LION-FS.svg?style=social)|Routing-Based Response Determination via Fast-Slow Dual-Path; Token Aggregation & Dropping for High-FPS Routing |

### Visual Token Reduction

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.08|StreamFlow: Dynamic Memory Flows for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2608.10949)|-|Raw-Frame Temporal-Residual Filtering before Visual Encoding for Lower Latency and Peak Memory |
|2026.06|Towards a Dynamic and Fixed-budget Memory Bank for Efficient Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2606.25658)|[[GitHub]](https://github.com/hktk07/CausalMem) ![](https://img.shields.io/github/stars/hktk07/CausalMem.svg?style=social)|Online Semantic-Basis Redundancy Estimation with Informative Visual Token Retention under a Fixed Budget |
|2026.05|Semantic-Aware Adaptive Visual Memory for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.07897)|[[GitHub]](https://github.com/wuhang03/savemem) ![](https://img.shields.io/github/stars/wuhang03/savemem.svg?style=social)|Pseudo-Question Semantic Prior for Temporal Pruning, Spatial Selection & Constant-Budget Selective Forgetting |
|2026.04|CodecSight: Leveraging Video Codec Signals for Efficient Streaming VLM Inference|[[pdf]](https://arxiv.org/pdf/2604.06036)|-|Single-pass Compressed-bitstream Ingestion; Motion Vector-guided Patch Pruning; I-frame Anchor KV-Cache Refresh with RoPE-based Position Correction|
|2026.04|A Simple Baseline for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2604.02317)|[[GitHub]](https://github.com/EvolvingLMMs-Lab/SimpleStream)![](https://img.shields.io/github/stars/EvolvingLMMs-Lab/SimpleStream.svg?style=social)|Fixed Recent-frame Window; Bounded-memory Low-latency Inference|
|2026.03|Thinking in Streaming Video|[[pdf]](https://arxiv.org/pdf/2603.12938)|[[GitHub]](https://github.com/johncaged/ThinkStream) ![](https://img.shields.io/github/stars/johncaged/ThinkStream.svg?style=social)|Eager Prefill + CUDA Graph Decode-and-Prune |
|2026.03|FluxMem: Adaptive Hierarchical Memory for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2603.02096)|[[GitHub]](https://github.com/YiwengXie/FluxMem) ![](https://img.shields.io/github/stars/YiwengXie/FluxMem.svg?style=social)|Visual Token Compression via TAS & SDC with Otsu-Based Adaptive Thresholding for Latency & Memory Reduction |
|2026.02|QueryStream: Advancing Streaming Video Understanding with Query-Aware Pruning and Proactive Response|[[pdf]](https://openreview.net/pdf?id=738HjJEbml)|-|Query-Aware Differential Pruning (QDP) & Relevance-Triggered Active Response (RTAR) Scheduling |
|2025.12|StreamingAssistant: Efficient Visual Token Pruning for Accelerating Online Video Understanding|[[pdf]](https://arxiv.org/pdf/2512.12560)|-|Checkerboard-Masked Parallel Spatial Pruning with Adjacency-Constrained Redundancy; Query-Agnostic Continuous Pre-Pruning Pipeline |
|2025.12|Accelerating Streaming Video Large Language Models via Hierarchical Token Compression|[[pdf]](https://arxiv.org/pdf/2512.00891)|[[GitHub]](https://github.com/lern-to-write/STC) ![](https://img.shields.io/github/stars/lern-to-write/STC.svg?style=social)|Hierarchical Token Compression: ViT Cache-Aware Selective Computation & Dual-Anchor Novelty Pruning |
|2025.10|Recurrent Attention-based Token Selection for Efficient Streaming Video-LLMs|[[pdf]](https://arxiv.org/pdf/2510.17364)|-|Attention-Based Visual Token Compression & Caption-Only Question Answering |
|2025.03|VideoScan: Enabling Efficient Streaming Video Understanding via Frame-level Semantic Carriers|[[pdf]](https://arxiv.org/pdf/2503.09387)|[[GitHub]](https://github.com/LyliAgave/VideoScan) ![](https://img.shields.io/github/stars/LyliAgave/VideoScan.svg?style=social)|Single Semantic Carrier per Frame; Prefill-Decode Decoupling; Visual Tokens Discarded after Prefill |
|2024.08|VideoLLM-MoD: Efficient Video-Language Streaming with Mixture-of-Depths Vision Computation|[[pdf]](https://arxiv.org/pdf/2408.16730)|-|Vision Token Computation Skipping with LayerExpert |

### KV-Cache Optimization

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.08|StreamTTT: Reconciling Real-Time Perception and Long-Term Memory in Streaming VLMs|[[pdf]](https://arxiv.org/pdf/2608.13416)|-|Short Sliding KV Cache Dedicated to Recent Evidence with Globally Continuous M-RoPE across Windows |
|2026.06|LiveStarPro: Proactive Streaming Video Understanding with Hierarchical Memory for Long-Horizon Streams|[[pdf]](https://arxiv.org/pdf/2606.17798)|[[GitHub]](https://github.com/sotayang/LiveStar) ![](https://img.shields.io/github/stars/sotayang/LiveStar.svg?style=social)|Inference-Time Streaming KV Cache for Faster Long-Horizon Processing on Existing LiveStar-8B Weights |
|2026.06|Harnessing Streaming Video in the Wild|[[pdf]](https://arxiv.org/pdf/2606.08615v1)| - |vLLM-Friendly; Prefix-aware KV Cache |
|2026.05|CoRDS: Coreset-based Representative and Diverse Selection for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.14310)|[[GitHub]](https://github.com/ailarmhz/CoRDS) ![](https://img.shields.io/github/stars/ailarmhz/CoRDS.svg?style=social)|Inference-Time Coreset Compression over Bottom-Layer KV Caches for Bounded Memory and Compute |
|2026.05|Decouple and Cache: KV Cache Construction for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.01858)|[[GitHub]](https://github.com/pangzhan27/DSCache) ![](https://img.shields.io/github/stars/pangzhan27/DSCache.svg?style=social)|Training-Free KV Cache Construction with Decoupled Past/Instant Caches and Position-Agnostic Encoding for Unbounded Streams |
|2026.04|Don't Pause! Every prediction matters in a streaming video|[[pdf]](https://arxiv.org/pdf/2604.24317)|[[GitHub]](https://github.com/dibschat/SPOT-Bench) ![](https://img.shields.io/github/stars/dibschat/SPOT-Bench.svg?style=social)|AsynKV Long-Short Term KV Memory; Scaling Compute during Dead-Time for Streaming Adaptation |
|2026.04|AURA: Always-On Understanding and Real-Time Assistance via Video Streams|[[pdf]](https://arxiv.org/pdf/2604.04184)|[[GitHub]](https://github.com/aurateam2026/AURA) ![](https://img.shields.io/github/stars/aurateam2026/AURA.svg?style=social)|Floating Video/QA Sliding Windows with Batched N' Chunk Truncation for Prefix KV-Cache Reuse and Lower TTFT |
|2026.01|HERMES: KV Cache as Hierarchical Memory for Efficient Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2601.14724)|[[GitHub]](https://github.com/haowei-freesky/HERMES) ![](https://img.shields.io/github/stars/haowei-freesky/HERMES.svg?style=social)|KV-Cache Reuse for Instant Query Response; Hierarchical Token Compression within Fixed Cache Budget |
|2025.12|V-Rex: Real-Time Streaming Video LLM Acceleration via Dynamic KV Cache Retrieval|[[pdf]](https://arxiv.org/pdf/2512.12284)|-|Hardware-Software Co-Design with Dynamic KV Cache Retrieval Engine Accelerator; Pipelined KV Prediction-Retrieval Overlapped with LLM Computation |
|2025.11|StreamKV: Streaming Video Question-Answering with Segment-based KV Cache Retrieval and Compression|[[pdf]](https://arxiv.org/pdf/2511.07278)|[[GitHub]](https://github.com/sou1p0wer/StreamKV) ![](https://img.shields.io/github/stars/sou1p0wer/StreamKV.svg?style=social)|Sliding-Window Segment Encoding with Immediate Post-Encoding KV Compression |
|2025.10|StreamingVLM: Real-Time Understanding for Infinite Video Streams|[[pdf]](https://arxiv.org/pdf/2510.09608)|[[GitHub]](https://github.com/mit-han-lab/streaming-vlm) ![](https://img.shields.io/github/stars/mit-han-lab/streaming-vlm.svg?style=social)|Bounded KV-Cache Eviction for Constant Memory; No Redundant Recomputation across Windows |
|2025.10|StreamingTOM: Streaming Token Compression for Efficient Video Understanding|[[pdf]](https://arxiv.org/pdf/2510.18269)|[[GitHub]](https://github.com/YIGE24/StreamingTOM) ![](https://img.shields.io/github/stars/YIGE24/StreamingTOM.svg?style=social)|Pre-LLM Causal Token Budget Cap for Prefill Acceleration; Post-LLM Quantized Memory with Selective Dequantization |
|2025.05|LiveVLM: Efficient Online Video Understanding via Streaming-Oriented KV Cache and Retrieval|[[pdf]](https://arxiv.org/pdf/2505.15269)|-|Pre-Generated Video KV Cache; Mean-Pooled Query-Key Chunk Retrieval with FIFO KV Chunk Management |
|2025.03|Streaming Video Question-Answering with In-context Video KV-Cache Retrieval|[[pdf]](https://arxiv.org/pdf/2503.00540)|[[GitHub]](https://github.com/Becomebright/ReKV) ![](https://img.shields.io/github/stars/Becomebright/ReKV.svg?style=social)|Multi-Process Parallel Encoding-Answering; Sliding-Window Attention for Stable-Latency Incremental Processing |

## 💭 Streaming with Thinking

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.05|An Efficient Streaming Video Understanding Framework with Agentic Control|[[pdf]](https://arxiv.org/pdf/2605.17921)|-|Adaptive Thinking with SFT + TB-GRPO to Route Ready Queries between Direct Answers and Slow Reasoning |
|2026.03|Think-as-You-See: Streaming Chain-of-Thought Reasoning for Large Vision-Language Models|[[pdf]](https://arxiv.org/pdf/2603.02872)|[[GitHub]](https://github.com/EIT-NLP/StreamingLLM/tree/main/TaYS) ![](https://img.shields.io/github/stars/EIT-NLP/StreamingLLM.svg?style=social)|Causal Streaming Attention Masking; Decoupled Cross-Modal Positional Encoding; Parallel Dual KV-Cache Mechanism |
|2026.03|Thinking in Streaming Video|[[pdf]](https://arxiv.org/pdf/2603.12938)|[[GitHub]](https://github.com/johncaged/ThinkStream) ![](https://img.shields.io/github/stars/johncaged/ThinkStream.svg?style=social)|Streaming Watch-Think-Speak Paradigm; Reasoning-Compressed Streaming Memory (RCSM); Streaming RLVR (Format + Time + Accuracy Reward) |
|2026.03|Video Streaming Thinking: VideoLLMs Can Watch and Think Simultaneously|[[pdf]](https://arxiv.org/pdf/2603.12262)|[[GitHub]](https://github.com/1ranGuan/VST) ![](https://img.shields.io/github/stars/1ranGuan/VST.svg?style=social)|The Video Streaming Thinking Paradigm; VKG-Based Streaming CoT Data Synthesis; Two-Stage VST-SFT & VST-RL Training |
|2026.03|Think While Watching: Online Streaming Segment-Level Memory for Multi-Turn Video Reasoning in MLLMs|[[pdf]](https://arxiv.org/pdf/2603.11896)|[[GitHub]](https://github.com/wl666hhh/Think_While_Watching) ![](https://img.shields.io/github/stars/wl666hhh/Think_While_Watching.svg?style=social)|Segment-Level Streaming Causal Mask & Positional Encoding; Three-Stage CoT Training; Concurrent Watch-Think Pipeline |
|2025.10|StreamingCoT: A Dataset for Temporal Dynamics and Multimodal Chain-of-Thought Reasoning in Streaming VideoQA|[[pdf]](https://arxiv.org/pdf/2510.25332)|[[GitHub]](https://github.com/Fleeting-hyh/StreamingCoT) ![](https://img.shields.io/github/stars/Fleeting-hyh/StreamingCoT.svg?style=social)| Streaming VideoQA and multimodal CoT tasks |

## 📊 Benchmarks

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.08|StreamArena: Toward Continuous, Interactive, and Long-Horizon Agentic Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2608.05703)|-|243 Full-Length Videos (88.8 min Avg.); 3,646 Open-Ended Tasks for Perception, Retrospection, Proactive Interaction & Tool Use |
|2026.06|OVO-S-Bench: A Hierarchical Benchmark for Streaming Spatial Intelligence in Multimodal LLMs|[[pdf]](https://arxiv.org/pdf/2606.03890)|[[html]](https://internlm.github.io/OVO-S-Bench/)|Streaming spatial understanding benchmark|
|2026.06|X-Stream: Exploring MLLMs as Multiplexers for Multi-Stream Understanding|[[pdf]](https://arxiv.org/pdf/2606.02482)|[[html]](https://peiwensun2000.github.io/xstream/)|Multi-stream understanding benchmark|
|2026.06|LiveStarPro: Proactive Streaming Video Understanding with Hierarchical Memory for Long-Horizon Streams|[[pdf]](https://arxiv.org/pdf/2606.17798)|[[GitHub]](https://github.com/sotayang/LiveStar) ![](https://img.shields.io/github/stars/sotayang/LiveStar.svg?style=social)|OmniStarPro for Long-Horizon Proactive Streaming Video Evaluation |
|2026.06|Harnessing Streaming Video in the Wild|[[pdf]](https://arxiv.org/pdf/2606.08615v1)| - |Streaming-Eval; in-the-wild streaming video scenarios |
|2026.05|OmniInteract: Benchmarking Real-World Streaming Interaction for Real-Time Omnimodal Assistants|[[pdf]](https://arxiv.org/pdf/2605.26485)|[[GitHub]](https://github.com/Lucky-Lance/OmniInteract) ![](https://img.shields.io/github/stars/Lucky-Lance/OmniInteract.svg?style=social)|Omni-modal streaming benchmark; user queries and ambient sounds embedded in the audio track; nested interaction tasks and interruption recovery|
|2026.05|StreamOV: Streaming Omni-Video Understanding via Evidence-Guided Memory and Response Triggering|[[pdf]](https://arxiv.org/pdf/2605.25621)|-|SOVBench for online multi-turn omni-modal evaluation with SOVBench-O and SOVBench-T |
|2026.05|OmniPro: A Comprehensive Benchmark for Omni-Proactive Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2605.18577)|[[GitHub]](https://github.com/RuixiangZhao/OmniPro) ![](https://img.shields.io/github/stars/RuixiangZhao/OmniPro.svg?style=social)|2.7K Human-Verified Samples across 9 Tasks with Probe and Online Evaluation Modes |
|2026.04|Don't Pause! Every prediction matters in a streaming video|[[pdf]](https://arxiv.org/pdf/2604.24317)|[[GitHub]](https://github.com/dibschat/SPOT-Bench) ![](https://img.shields.io/github/stars/dibschat/SPOT-Bench.svg?style=social)|SPOT-Bench with Multi-Turn Proactive Queries; Timeliness-F1 for Temporal Precision and Coverage |
|2026.03|SVCBench: A Streaming Video Counting Benchmark for Spatial-Temporal State Maintenance|[[pdf]](https://arxiv.org/pdf/2603.12703)|[[html]](https://buaa-colalab.github.io/SVCBench/)|A streaming video counting benchmark spanning both proactive and reactive counting tasks|
|2026.03|RIVER: A Real-Time Interaction Benchmark for Video LLMs|[[pdf]](https://arxiv.org/pdf/2603.03985)|[[GitHub]](https://github.com/OpenGVLab/RIVER) ![](https://img.shields.io/github/stars/OpenGVLab/RIVER.svg?style=social)|Memory & Perception & Anticipation|
|2026.03|PEARL: Personalized Streaming Video Understanding Model|[[pdf]](https://arxiv.org/pdf/2603.20422)|[[GitHub]](https://github.com/Yuanhong-Zheng/PEARL) ![](https://img.shields.io/github/stars/Yuanhong-Zheng/PEARL.svg?style=social)|Frame-Level Personalization & Video-Level Personalization; Concept-Definition QA & Real-Time QA & Past-Time QA|
|2026.03|StreamingEval: A Unified Evaluation Framework towards Realistic Streaming Video Understanding|[[pdf]](https://aclanthology.org/2026.findings-acl.295.pdf)|[[GitHub]](https://github.com/wwgTang-111/StreamingEval1) ![](https://img.shields.io/github/stars/wwgTang-111/StreamingEval1.svg?style=social)|Unified Fixed-Capacity Protocol for Encoding Efficiency, Decoding Latency, Storage & Accuracy |
|2026.03|HomeSafe-Bench: Evaluating Vision-Language Models on Unsafe Action Detection for Embodied Agents in Household|[[pdf]](https://arxiv.org/pdf/2603.11975)|[[GitHub]](https://github.com/pujiayue/HomeSafe-Bench) ![](https://img.shields.io/github/stars/pujiayue/HomeSafe-Bench.svg?style=social)|Unsafe Action Detection; Early Warning Timing; Severity Assessment |
|2026.02|Artic: AI-oriented Real-time Communication for MLLM Video Assistant|[[pdf]](https://arxiv.org/pdf/2602.12641)|[[GitHub]](https://github.com/pku-netvideo/DeViBench) ![](https://img.shields.io/github/stars/pku-netvideo/DeViBench.svg?style=social)|Degradation-sensitive QA |
|2026.01|OnlineSI: Taming Large Language Model for Online 3D Understanding and Grounding|[[pdf]](https://arxiv.org/pdf/2601.16538)|[[GitHub]](https://github.com/StoreBlank/online-spatial-intelligence) ![](https://img.shields.io/github/stars/StoreBlank/online-spatial-intelligence.svg?style=social)|Online 3D Object Detection |
|2026.01|PhoStream: Benchmarking Real-World Streaming for Omnimodal Assistants in Mobile Scenarios|[[pdf]](https://arxiv.org/pdf/2601.22575)|[[GitHub]](https://github.com/Lucky-Lance/PhoStream) ![](https://img.shields.io/github/stars/Lucky-Lance/PhoStream.svg?style=social)|Mobile-Centric Scenarios; Perception & Interaction & Planning |
|2025.12|StreamEQA: Towards Streaming Video Understanding for Embodied Scenarios|[[pdf]](https://arxiv.org/pdf/2512.04451)|[[GitHub]](https://github.com/MrYF-Wang/StreamEQA) ![](https://img.shields.io/github/stars/MrYF-Wang/StreamEQA.svg?style=social)|Embodied Scenarios |
|2025.12|StreamGaze: Gaze-Guided Temporal Reasoning and Proactive Understanding in Streaming Videos|[[pdf]](https://arxiv.org/pdf/2512.01707)|[[GitHub]](https://github.com/daeunni/StreamGaze) ![](https://img.shields.io/github/stars/daeunni/StreamGaze.svg?style=social)|Gaze-Guided Streaming Data; Past & Present & Proactive |
|2025.10|Can Multi-Modal LLMs Provide Live Step-by-Step Task Guidance?|[[pdf]](https://arxiv.org/pdf/2511.21998)|[[GitHub]](https://github.com/Qualcomm-AI-research/qualcomm_interactive_cooking_eval) ![](https://img.shields.io/github/stars/Qualcomm-AI-research/qualcomm_interactive_cooking_eval.svg?style=social)|Qualcomm Interactive Cooking|
|2025.10|Eyes Wide Open: Ego Proactive Video-LLM for Streaming Video|[[pdf]](https://arxiv.org/pdf/2510.14560)|[[GitHub]](https://github.com/zhangyl4/EyeWO) ![](https://img.shields.io/github/stars/zhangyl4/EyeWO.svg?style=social)|Explicit Proactives; Implicit Proactive; Contextual Proactive|
|2025.09|StreamForest: Efficient Online Video Understanding with Persistent Event Memory|[[pdf]](https://arxiv.org/pdf/2509.24871)|[[GitHub]](https://github.com/MCG-NJU/StreamForest) ![](https://img.shields.io/github/stars/MCG-NJU/StreamForest.svg?style=social)|ODV-Bench for online autonomous-driving video understanding; Static Target / Dynamic Target / Event-oriented tasks |
|2025.07|OST-Bench: Evaluating the Capabilities of MLLMs in Online Spatio-temporal Scene Understanding|[[pdf]](https://arxiv.org/pdf/2507.07984)|[[GitHub]](https://github.com/InternRobotics/OST-Bench) ![](https://img.shields.io/github/stars/InternRobotics/OST-Bench.svg?style=social)|Agent State; Agent Visible Info; Agent-Object Spatial Relationship |
|2025.07|ProactiveVideoQA: A Comprehensive Benchmark Evaluating Proactive Interactions in Video Large Language Models|[[pdf]](https://arxiv.org/pdf/2507.09313)|[[GitHub]](https://github.com/yellow-binary-tree/ProactiveVideoQA) ![](https://img.shields.io/github/stars/yellow-binary-tree/ProactiveVideoQA.svg?style=social)|Proactive Web-Video QA; Proactive Ego-Centric Video QA; Proactive TV-Series Video QA; Proactive Video Anomaly Detection |
|2025.07|Chat with AI: The Surprising Turn of Real-time Video Communication from Human to AI|[[pdf]](https://arxiv.org/pdf/2507.10510)|[[GitHub]](https://github.com/JiangkaiWu/DeViBench) ![](https://img.shields.io/github/stars/JiangkaiWu/DeViBench.svg?style=social)|DeViBench |
|2025.05|RTV-Bench: Benchmarking MLLM Continuous Perception, Understanding and Reasoning through Real-Time Video|[[pdf]](https://arxiv.org/pdf/2505.02064)|[[GitHub]](https://github.com/LJungang/RTV-Bench) ![](https://img.shields.io/github/stars/LJungang/RTV-Bench.svg?style=social)|Perception; Understanding; Reasoning |
|2025.04|LiveCC: Learning Video LLM with Streaming Speech Transcription at Scale|[[pdf]](https://arxiv.org/pdf/2504.16030)|[[GitHub]](https://github.com/showlab/livecc) ![](https://img.shields.io/github/stars/showlab/livecc.svg?style=social)|LiveSports-3K-CC/QA |
|2025.03|OmniMMI: A Comprehensive Multi-modal Interaction Benchmark in Streaming Video Contexts|[[pdf]](https://arxiv.org/pdf/2503.22952)|[[GitHub]](https://github.com/OmniMMI/M4) ![](https://img.shields.io/github/stars/OmniMMI/M4.svg?style=social)|Streaming Video Understanding; Proactive Reasoning |
|2025.03|ViSpeak: Visual Instruction Feedback in Streaming Videos|[[pdf]](https://arxiv.org/pdf/2503.12769)|[[GitHub]](https://github.com/HumanMLLM/ViSpeak) ![](https://img.shields.io/github/stars/HumanMLLM/ViSpeak.svg?style=social)|Visual Instruction Feedback |
|2025.02|SVBench: A Benchmark with Temporal Multi-Turn Dialogues for Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2502.10810)|[[GitHub]](https://github.com/sotayang/SVBench) ![](https://img.shields.io/github/stars/sotayang/SVBench.svg?style=social)|Multi-Turn Dialogues |
|2025.01|Online Video Understanding: OVBench and VideoChat-Online|[[pdf]](https://arxiv.org/pdf/2501.00584)|[[GitHub]](https://github.com/MCG-NJU/VideoChat-Online) ![](https://img.shields.io/github/stars/MCG-NJU/VideoChat-Online.svg?style=social)|Past; Current; Future |
|2025.01|OVO-Bench: How Far is Your Video-LLMs from Real-World Online Video Understanding?|[[pdf]](https://arxiv.org/pdf/2501.05510)|[[GitHub]](https://github.com/JoeLeelyf/OVO-Bench) ![](https://img.shields.io/github/stars/JoeLeelyf/OVO-Bench.svg?style=social)|Backward Tracing; Real-Time Understanding; Forward Active Responding |
|2025.01|Streaming Video Understanding and Multi-round Interaction with Memory-enhanced Knowledge|[[pdf]](https://arxiv.org/pdf/2501.13468)|[[GitHub]](https://github.com/hmxiong/StreamChat) ![](https://img.shields.io/github/stars/hmxiong/StreamChat.svg?style=social)|Object Search; Long-Term Memory Search; Short-Term Memory Search; Conversational Interaction; Knowledge-Based Question Answering; Simple Factual |
|2024.11|StreamingBench: Assessing the Gap for MLLMs to Achieve Streaming Video Understanding|[[pdf]](https://arxiv.org/pdf/2411.03628)|[[GitHub]](https://github.com/THUNLP-MT/StreamingBench) ![](https://img.shields.io/github/stars/THUNLP-MT/StreamingBench.svg?style=social)|Real-Time Visual Understanding; Omni-Source Understanding; Contextual Understanding |
|2024.07|What to Say and When to Say it: Live Fitness Coaching as a Testbed for Situated Interaction|[[pdf]](https://arxiv.org/pdf/2407.08101)|[[GitHub]](https://github.com/Qualcomm-AI-research/FitCoach) ![](https://img.shields.io/github/stars/Qualcomm-AI-research/FitCoach.svg?style=social)|Fitness Activity Recognition and Coaching |
|2024.03|MovieChat: From Dense Token to Sparse Memory for Long Video Understanding|[[pdf]](https://arxiv.org/pdf/2307.16449)|[[GitHub]](https://github.com/rese1f/MovieChat) ![](https://img.shields.io/github/stars/rese1f/MovieChat.svg?style=social)|Movies and TV |

## 📦 Training Datasets

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2026.08|StreamTTT: Reconciling Real-Time Perception and Long-Term Memory in Streaming VLMs|[[pdf]](https://arxiv.org/pdf/2608.13416)|-|112.4K Real-Time QA Corpus from Answer-Time Relocation plus Action, Spatial Reasoning, Anticipation & Captioning Supervision |
|2026.07|VideoChat3: Fully Open Video MLLM for Efficient and Generalist Video Understanding|[[pdf]](https://arxiv.org/pdf/2607.14935)|[[GitHub]](https://github.com/MCG-NJU/VideoChat3) ![](https://img.shields.io/github/stars/MCG-NJU/VideoChat3.svg?style=social)|I3D-ViT with 16x Compression and a 617K Dataset for Generic Online Video Understanding|
|2026.06|Harnessing Streaming Video in the Wild|[[pdf]](https://arxiv.org/pdf/2606.08615v1)| - |spanning diverse real-world scenarios |
|2026.03|WAT: Online Video Understanding Needs Watching Before Thinking|[[pdf]](https://arxiv.org/pdf/2603.13412)|-|Real-Time Perception; Backward Tracing; Forecasting |
|2026.03|Thinking in Streaming Video|[[pdf]](https://arxiv.org/pdf/2603.12938)|[[GitHub]](https://github.com/johncaged/ThinkStream) ![](https://img.shields.io/github/stars/johncaged/ThinkStream.svg?style=social)|Video Segmentation and Dense Captioning; Diverse Instruction Synthesis; Time-Grounded CoT Generation |
|2026.01|Learning to Respond: A Large-Scale Benchmark and Progressive Learning Framework for Trigger-Centric Online Video Understanding|[[pdf]](https://openreview.net/pdf?id=gmpnSSiJt7)|-|TV-Online |
|2026.01|ROMA: Real-time Omni-Multimodal Assistant with Interactive Streaming Understanding|[[pdf]](https://arxiv.org/pdf/2601.10323)|[[GitHub]](https://github.com/Eureka-Maggie/ROMA) ![](https://img.shields.io/github/stars/Eureka-Maggie/ROMA.svg?style=social)|Online Proactive; Online Narration; Reactive QA |
|2025.12|Streaming Video Instruction Tuning|[[pdf]](https://arxiv.org/pdf/2512.21334)|[[GitHub]](https://github.com/maifoundations/Streamo) ![](https://img.shields.io/github/stars/maifoundations/Streamo.svg?style=social)|Real-Time Narration; Event Caption; Action Caption; Event Grounding; Time-Sensitive QA |
|2025.12|MMDuet2: Enhancing Proactive Interaction of Video MLLMs with Multi-Turn Reinforcement Learning|[[pdf]](https://arxiv.org/pdf/2512.06810)|[[GitHub]](https://github.com/yellow-binary-tree/MMDuet2) ![](https://img.shields.io/github/stars/yellow-binary-tree/MMDuet2.svg?style=social)|Scene Segmentation and Captioning; QA Generation; Proactive Dialogue Construction |
|2025.12|CogStream: Context-guided Streaming Video Question Answering|[[pdf]](https://arxiv.org/pdf/2506.10516)|[[GitHub]](https://github.com/LiamZhao326/CogStream) ![](https://img.shields.io/github/stars/LiamZhao326/CogStream.svg?style=social)|Semi-Automatic QA Pipeline; 1,088 Videos with 59K Hierarchical QA Pairs (Basic, Streaming, Global) |
|2025.11|LiveStar: Live Streaming Assistant for Real-World Online Video Understanding|[[pdf]](https://arxiv.org/pdf/2511.05299)|[[GitHub]](https://github.com/sotayang/LiveStar) ![](https://img.shields.io/github/stars/sotayang/LiveStar.svg?style=social)|Real-Time Narration Generation; Online Temporal Grounding; Frame-Level Dense QA; Contextual Online QA; Multi-Turn Interactive QA |
|2025.10|StreamingCoT: A Dataset for Temporal Dynamics and Multimodal Chain-of-Thought Reasoning in Streaming VideoQA|[[pdf]](https://arxiv.org/pdf/2510.25332)|[[GitHub]](https://github.com/Fleeting-hyh/StreamingCoT) ![](https://img.shields.io/github/stars/Fleeting-hyh/StreamingCoT.svg?style=social)|Hierarchical Video Dense Captioning; Dynamic Question-Answer Pairs Construction; Multimodal Chain-of-Thought Generation |
|2025.10|StreamingVLM: Real-Time Understanding for Infinite Video Streams|[[pdf]](https://arxiv.org/pdf/2510.09608)|[[GitHub]](https://github.com/mit-han-lab/streaming-vlm) ![](https://img.shields.io/github/stars/mit-han-lab/streaming-vlm.svg?style=social)|Sports; Narration |
|2025.10|Eyes Wide Open: Ego Proactive Video-LLM for Streaming Video|[[pdf]](https://arxiv.org/pdf/2510.14560)|[[GitHub]](https://github.com/zhangyl4/EyeWO) ![](https://img.shields.io/github/stars/zhangyl4/EyeWO.svg?style=social)|Explicit Proactive Tasks; Implicit Proactive Tasks; Contextual Proactive Tasks |
|2025.09|StreamForest: Efficient Online Video Understanding with Persistent Event Memory|[[pdf]](https://arxiv.org/pdf/2509.24871)|[[GitHub]](https://github.com/MCG-NJU/StreamForest) ![](https://img.shields.io/github/stars/MCG-NJU/StreamForest.svg?style=social)|Fine-grained Real-time Perception, Motion Prediction|
|2025.06|Proactive Assistant Dialogue Generation from Streaming Egocentric Videos|[[pdf]](https://arxiv.org/pdf/2506.05904)|[[GitHub]](https://github.com/pro-assist/ProAssist) ![](https://img.shields.io/github/stars/pro-assist/ProAssist.svg?style=social)|Multi-Round Dialogue |
|2025.04|LiveCC: Learning Video LLM with Streaming Speech Transcription at Scale|[[pdf]](https://arxiv.org/pdf/2504.16030)|[[GitHub]](https://github.com/showlab/livecc) ![](https://img.shields.io/github/stars/showlab/livecc.svg?style=social)|ASR Transcripts |
|2025.03|AssistPDA: An Online Video Surveillance Assistant for Video Anomaly Prediction, Detection, and Analysis|[[pdf]](https://arxiv.org/pdf/2503.21904)|-|Anomaly Prediction; Anomaly Detection; Anomaly Analysis |
|2025.03|ViSpeak: Visual Instruction Feedback in Streaming Videos|[[pdf]](https://arxiv.org/pdf/2503.12769)|[[GitHub]](https://github.com/HumanMLLM/ViSpeak) ![](https://img.shields.io/github/stars/HumanMLLM/ViSpeak.svg?style=social)|Visual Instruction Feedback |
|2025.02|EgoSpeak: Learning When to Speak for Egocentric Conversational Agents in the Wild|[[pdf]](https://arxiv.org/pdf/2502.14892)|[[GitHub]](https://github.com/jun297/EgoSpeak) ![](https://img.shields.io/github/stars/jun297/EgoSpeak.svg?style=social)|Prediction vs Detection; Frame-Level Speech Labeling |
|2024.11|VideoLLM Knows When to Speak: Enhancing Time-Sensitive Video Comprehension with Video-Text Duet Interaction Format|[[pdf]](https://arxiv.org/pdf/2411.17991)|[[GitHub]](https://github.com/yellow-binary-tree/mmduet) ![](https://img.shields.io/github/stars/yellow-binary-tree/mmduet.svg?style=social)|Multi-Answer Video Grounded QA; Dense Captioning; Temporal Video Grounding |
|2024.07|What to Say and When to Say it: Live Fitness Coaching as a Testbed for Situated Interaction|[[pdf]](https://arxiv.org/pdf/2407.08101)|[[GitHub]](https://github.com/Qualcomm-AI-research/FitCoach) ![](https://img.shields.io/github/stars/Qualcomm-AI-research/FitCoach.svg?style=social)|Fitness Activity Recognition and Coaching |
|2024.06|VideoLLM-online: Online Video Large Language Model for Streaming Video|[[pdf]](https://arxiv.org/pdf/2406.11816)|[[GitHub]](https://github.com/showlab/videollm-online) ![](https://img.shields.io/github/stars/showlab/videollm-online.svg?style=social)|Narration Stream |

## 📝 Survey

|Date|Title|Paper|Code|Comment|
|:---:|:---:|:---:|:---:|:---:|
|2024.01|A Survey on Generative AI and LLM for Video Generation, Understanding, and Streaming|[[pdf]](https://arxiv.org/pdf/2404.16038)|-|- |

## 🔗 Resources
- [JeffShine/Awesome-Streaming-Video-Understanding](https://github.com/JeffShine/Awesome-Streaming-Video-Understanding)
- [sotayang/Awesome-Streaming-Video-Understanding](https://github.com/sotayang/Awesome-Streaming-Video-Understanding)
- [LJungang/Awesome-Video-Reasoning-Landscape](https://github.com/LJungang/Awesome-Video-Reasoning-Landscape)

## ☎️ We're Hiring!
We're hiring multimodal research scientists and interns at JD Explore Academy! If you have top-tier publications and are passionate about video understanding and VLMs, please send your resume to: siqingyi.phoebus@jd.com. We'd love to hear from you!
