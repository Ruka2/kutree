---
layout: archive
title: ""
permalink: /resume/
author_profile: false
redirect_from:
  - /resume
---

{% include base_path %}

<link rel="stylesheet" href="{{ base_path }}/assets/css/cv-style.css">

<style>
  .archive {
    width: 100% !important;
    float: none;
    padding-right: 0;
    margin: 0 auto;
  }

  .cv-page {
    background: #fff;
    padding: 2.5rem;
    border-radius: 8px;
    box-shadow: 0 4px 20px rgba(0,0,0,0.08);
  }

  .cv-header {
    text-align: center;
    border-bottom: 2px solid #2a7ae2;
    /* margin-bottom: 2.0rem; */
    /* padding-bottom: 1.5rem; */
  }

  .cv-header h1 {
    font-size: 1.5rem;
    /* margin-bottom: 0.25rem; */
    color: #1a1a1a;
  }

  .cv-title {
    font-size: 1.0rem;
    color: #2a7ae2;
    font-weight: 500;
    margin-bottom: 1rem;
  }

  .cv-contact-info {
    justify-content: center;
    gap: 1.5rem;
    font-size: 0.95rem;
  }

  .cv-badge {
    display: inline-block;
    background: #e8f5e9;
    color: #2e7d32;
    padding: 0.25rem 0.75rem;
    border-radius: 20px;
    font-size: 0.95rem;
    font-weight: 500;
    margin-left: 0.5rem;
  }

  .cv-item-overview {
    margin: 0.5rem 0;
    line-height: 1.7;
    font-size: 0.9rem;
  }

  .cv-item-highlights {
    margin: 0;
    line-height: 1.7;
    font-size: 0.9rem;
  }

  .cv-project-keywords {
    margin: 0;
    font-size: 0.75rem;
  }

  .cv-project-keyword {
    margin: 0;
    font-size: 0.75rem;
  }

  .cv-item-date {
    margin: 0;
    font-size: 0.8rem;
  }

  .cv-item-title {
    margin: 0;
    font-size: 0.9rem;
  }

  .cv-item-subtitle {
    font-weight: 600;
    color: #333;
    margin-top: 0.75rem;
    margin-bottom: 0;
    font-size: 0.9rem;
  }

  .cv-skill-text p {
    margin: 0.4rem 0;
    line-height: 1.6;
    font-size: 0.9rem;
  }

  .cv-skill-text strong {
    color: #2a7ae2;
    font-weight: 600;
    font-size: 0.9rem;
  }

  @media (max-width: 768px) {
    .cv-page {
      padding: 1.5rem;
    }
    .cv-header h1 {
      font-size: 2rem;
    }
    .cv-item-header {
      flex-direction: column;
      gap: 0.25rem;
    }
  }
</style>

<div class="cv-page">
<div class="cv-container">

<header class="cv-header">
  <h1>KU SU WA</h1>
  <div class="cv-title">
    Agent Development Engineer <span style="color:#999;">|</span> LLM Algorithm Engineer
    <span class="cv-badge">Open to Job</span>
  </div>
  <div class="cv-contact-info">
    <span class="cv-contact-item"><i class="fas fa-envelope"></i> sku_contact@163.com</span>
    <!-- <span class="cv-contact-item"><i class="fas fa-map-marker-alt"></i> Beijing, China</span> -->
  </div>
</header>

<section class="cv-section">
  <h2>What I Bring</h2>
  <div class="cv-skill-text">
    <p><strong>LLM Traning:</strong> Post-traning including SFT, DPO; Omni, ASR, TTS models</p>
    <p><strong>Agent Infrastructure:</strong> LangChain, LangGraph, vLLM, SGLang</p>
    <p><strong>DevOps:</strong> MLOps, Containerization, Jenkins</p>
    <p><strong>Programming:</strong> Python, AI Coding (Kimi-cli, Claude Code)</p>
    <p><strong>Prototyping:</strong> Web React, Vue</p>
    <p><strong>Designing:</strong> Live2D Avatar, Cartoon/Anime Designer</p>
    <p><strong>Languages:</strong> Chinese, English</p>
  </div>
</section>

<section class="cv-section">
  <h2>Project Experience</h2>

  <article class="cv-item">
    <div class="cv-item-header">
      <div class="cv-item-title">Latency-Optimized Multi-Agent Conversational AI System</div>
      <div class="cv-item-date">2026.03 - 2026.06</div>
    </div>
    <div class="cv-project-keywords">
      <span class="cv-project-keyword">Asyncio</span>
      <span class="cv-project-keyword">AgentScope</span>
      <span class="cv-project-keyword">Mem0</span>
      <span class="cv-project-keyword">SGLang</span>
      <span class="cv-project-keyword">Vtube studio API</span>
    </div>
    <div class="cv-item-overview">
      <strong>Overview:</strong> Designed a multi-agent collaborative architecture to minimize end-to-end latency in LLM-based dialogue systems. The system establishes asynchronous pipelines that monitor information gain and time thresholds during the streaming reasoning process. It fragments intermediate chain-of-thought (COT) reasoning into incremental fragment, synthesizes them into concise summaries, and proactively delivers follow-up responses to users.
    </div>
    <div class="cv-item-subtitle">Key Results:</div>
    <ul class="cv-item-highlights">
      <li>Full-duplex voice interaction with an average response latency of ~2.5 seconds across multi-turn dialogue tasks.</li>
      <li>Configuration-based model selection and cost control.</li>
      <li>Integrated agent memory and skills; step-wise summarization ensures tool/skill expansion does not degrade average response time.</li>
    </ul>
    <div class="cv-item-subtitle">Technical Implementation:</div>
    <ul class="cv-item-highlights">
      <li>Using the AgentScope framework to customizing agent hook functions to support the proposed streaming-generation tracing methodology.</li>
      <li>Built a voice interaction system with pipeline: SileroVAD (front-end VAD) -> SenseVoice-Small (ASR) -> Qwen3.5-35B-A3B (LLM) -> CosyVoice3-0.5B (TTS); and an agent Loop: mem0 (Agent Memory), arXiv paper retrieval, and online search (Skills).</li>
      <li>Deployed SGLang inference serving with prefix caching to accelerate reusable multi-turn dialogue.</li>
      
    </ul>
  </article>

  <article class="cv-item">
    <div class="cv-item-header">
      <div class="cv-item-title">Intelligent Vehicle Cockpit Assistant</div>
      <div class="cv-item-date">2025.05 - 2026.01</div>
    </div>
    <div class="cv-project-keywords">
      <span class="cv-project-keyword">PyTorch</span>
      <span class="cv-project-keyword">LlamaFactory</span>
      <span class="cv-project-keyword">vLLM</span>
      <span class="cv-project-keyword">Qwen-Agent</span>
      <span class="cv-project-keyword">MCP</span>
      <span class="cv-project-keyword">RAG</span>
      <span class="cv-project-keyword">Docker</span>
      <span class="cv-project-keyword">ONNX Runtime</span>
    </div>
    <div class="cv-item-overview">
      <strong>Overview:</strong> Developed an in-vehicle assistant for smart automotive car, including context chaining, intent routing, skill integration, and RAG-based user preference recommendation. Given the Android and CPU-only devices, implements model compression via ONNX quantization with static calibration for offline deployment.
    </div>
    <div class="cv-item-subtitle">Key Results:</div>
    <ul class="cv-item-highlights">
      <li>Online servicing the AI assistant for a Japanese automaker, maintained via OTA updates for approximately one year.</li>
      <li>Enabled voice control of OS operations, software applications, and ~5,000 in-vehicle device commands (e.g., HVAC, windows).</li>
      <li>Achieved 93% consistency with online map API results for route planning within Beijing; stress-tested system latency at approximately 3,000ms.</li>
    </ul>
    <div class="cv-item-subtitle">Technical Implementation:</div>
    <ul class="cv-item-highlights">
      <li>Fine-tuned the hunyuan-4b-instruct LLM model via SFT for automotive interaction and route planning; applied DPO training to align open-domain chatting boundaries and refusal policies, mitigating LLM repetition and optimizing naturalistic tone for the small-parameter model.</li>
      <li>Developed MCP server, consolidating NLP tasks (intent classification, decomposition, and entity extraction) into tools with fixed SOP chain. </li>
      <li>Fused dual LoRA weights and constructed a calibration dataset for LLM static quantization, enabling deployment on the Android-based unit.</li>
    </ul>
  </article>
</section>

</div>
</div>
