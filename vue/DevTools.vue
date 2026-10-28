<script setup>
import { ref } from "vue";

const terminalTab = ref("audit");
const mobileMenuOpen = ref(false);
const copiedEmail = ref(null);

const handleCopyEmail = (email) => {
  navigator.clipboard.writeText(email);
  copiedEmail.value = email;
  setTimeout(() => { copiedEmail.value = null; }, 2000);
};

const techStack = [
  { n: "Anthropic Claude API", d: "Frontier LLM Reasoning & Tool Calling" },
  { n: "Python", d: "AsyncIO, Pydantic & ML Pipelines" },
  { n: "FastAPI", d: "Sub-millisecond Microservices" },
  { n: "React", d: "Next.js Reactive Dashboards" },
  { n: "Docker", d: "Containerized Agent Sandboxes" },
  { n: "PyTorch", d: "Deep Learning & Vision Inference" },
  { n: "Neo4j", d: "Graph Knowledge Reasoning" },
  { n: "Redis", d: "In-Memory Session State Cache" },
];
</script>

<template>
  <div class="dark min-h-screen bg-[#090D16] text-[#F3F4F6] font-sans antialiased selection:bg-blue-600 selection:text-white">
    <!-- Announcement -->
    <div class="border-b border-[#1F293D] bg-[#0F1626]/60 backdrop-blur px-4 py-2 text-center text-xs sm:text-sm">
      <div class="mx-auto flex max-w-6xl items-center justify-center gap-2">
        <span class="inline-flex items-center gap-1 rounded-full bg-[#D97706]/10 border border-[#D97706]/30 px-2 py-0.5 font-mono text-[10px] font-semibold uppercase tracking-wider text-[#F59E0B]">
          <span class="h-1.5 w-1.5 rounded-full bg-[#D97706] animate-ping"></span>
          Anthropic Partner
        </span>
        <span class="text-[#94A3B8] hidden sm:inline">Announcing</span>
        <span class="font-medium text-white">SphereAgent Engine: Frontier Claude API Multi-Agent Orchestration</span>
        <a href="#sphereagent" class="inline-flex items-center font-semibold text-[#3B82F6] hover:text-[#38BDF8] transition-colors underline-offset-4 hover:underline">
          Explore Architecture &rarr;
        </a>
      </div>
    </div>

    <!-- Header -->
    <header class="sticky top-0 z-40 border-b border-[#1F293D] bg-[#090D16]/80 backdrop-blur-md">
      <div class="mx-auto flex h-16 max-w-7xl items-center justify-between px-6">
        <a href="#" class="flex items-center gap-3 group">
          <div class="flex h-9 w-9 items-center justify-center rounded-lg bg-gradient-to-tr from-blue-600 via-indigo-600 to-amber-500 shadow-lg shadow-blue-500/20">
            <svg class="h-5 w-5 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round">
              <circle cx="12" cy="12" r="9"></circle>
              <path d="M12 3a9 9 0 0 0 0 18"></path>
              <circle cx="12" cy="12" r="3" fill="currentColor"></circle>
            </svg>
          </div>
          <div class="flex flex-col">
            <div class="flex items-center gap-1.5">
              <span class="text-lg font-bold tracking-tight text-white">StakeSphere</span>
              <span class="rounded bg-blue-500/10 border border-blue-500/30 px-1.5 py-0.2 font-mono text-[9px] font-semibold uppercase text-blue-400">AI</span>
            </div>
            <span class="text-[10px] text-[#94A3B8] tracking-tight hidden sm:block">AI Studio &amp; Agentic Platform</span>
          </div>
        </a>

        <nav class="hidden md:flex items-center gap-7 text-[13.5px] font-medium text-[#94A3B8]">
          <a href="#sphereagent" class="hover:text-white transition-colors">SphereAgent Engine</a>
          <a href="#services" class="hover:text-white transition-colors">Engineering Services</a>
          <a href="#stack" class="hover:text-white transition-colors">Tech Architecture</a>
          <a href="#team" class="hover:text-white transition-colors">Team &amp; Contact</a>
        </nav>

        <div class="flex items-center gap-3">
          <a href="mailto:wajahat.joyo@stakesphere.me?subject=StakeSphere%20Engineering%20Consultation" class="inline-flex items-center justify-center gap-1.5 rounded-lg bg-gradient-to-r from-blue-600 to-indigo-600 px-4 py-2 text-xs font-semibold text-white shadow-md shadow-blue-600/25 hover:from-blue-500 hover:to-indigo-500 transition-all">
            <span>Book Consultation</span>
          </a>
        </div>
      </div>
    </header>

    <!-- Hero -->
    <section class="relative border-b border-[#1F293D] pt-16 pb-20 sm:pt-24 sm:pb-28 text-center px-6">
      <div class="inline-flex items-center gap-2 rounded-full border border-[#1F293D] bg-[#0F1626]/80 px-3.5 py-1.5 mb-8">
        <span class="h-2 w-2 rounded-full bg-emerald-400 animate-pulse"></span>
        <span class="font-mono text-xs font-medium text-[#94A3B8]">AI-Native Software Engineering Studio &bull; Frontier Agentic Platform</span>
      </div>

      <h1 class="mx-auto max-w-5xl text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight leading-[1.08] text-white">
        StakeSphere — Autonomous AI Products &amp; <span class="bg-gradient-to-r from-blue-400 via-indigo-300 to-amber-300 bg-clip-text text-transparent">Custom Software Engineering</span>
      </h1>

      <p class="mx-auto mt-6 max-w-3xl text-lg sm:text-xl leading-relaxed text-[#94A3B8]">
        We build production-grade agentic workflows, custom enterprise applications, and intelligent microservices powered by frontier LLMs.
      </p>

      <div class="mt-10 flex flex-col sm:flex-row items-center justify-center gap-4">
        <a href="#sphereagent" class="w-full sm:w-auto inline-flex items-center justify-center gap-2 rounded-xl bg-gradient-to-r from-blue-600 via-blue-500 to-indigo-600 px-7 py-3.5 text-sm font-semibold text-white shadow-lg shadow-blue-500/25">
          Explore Our AI Platform
        </a>
        <a href="mailto:wajahat.joyo@stakesphere.me?subject=StakeSphere%20Engineering%20Consultation" class="w-full sm:w-auto inline-flex items-center justify-center gap-2 rounded-xl border border-[#1F293D] bg-[#0F1626] px-7 py-3.5 text-sm font-semibold text-white hover:bg-[#172238]">
          Book a Engineering Consultation
        </a>
      </div>

      <!-- Live Terminal -->
      <div class="mt-14 mx-auto max-w-4xl overflow-hidden rounded-2xl border border-[#1F293D] bg-[#0B101D] text-left shadow-2xl">
        <div class="flex flex-wrap items-center justify-between gap-3 border-b border-[#1F293D] bg-[#0F1626] px-4 py-3">
          <div class="flex items-center gap-2">
            <span class="h-3 w-3 rounded-full bg-red-500/70 inline-block"></span>
            <span class="h-3 w-3 rounded-full bg-yellow-500/70 inline-block"></span>
            <span class="h-3 w-3 rounded-full bg-emerald-500/70 inline-block"></span>
            <span class="ml-2 font-mono text-xs text-[#94A3B8]">sphereagent-orchestrator [claude-3-5-sonnet]</span>
          </div>
          <div class="flex gap-1.5 font-mono text-xs">
            <button @click="terminalTab = 'audit'" :class="['px-3 py-1 rounded border text-xs capitalize', terminalTab === 'audit' ? 'bg-[#1F293D] text-white border-blue-500' : 'text-[#94A3B8] border-[#1F293D]']">Code Audit</button>
            <button @click="terminalTab = 'graph'" :class="['px-3 py-1 rounded border text-xs capitalize', terminalTab === 'graph' ? 'bg-[#1F293D] text-white border-blue-500' : 'text-[#94A3B8] border-[#1F293D]']">Knowledge Graph</button>
            <button @click="terminalTab = 'support'" :class="['px-3 py-1 rounded border text-xs capitalize', terminalTab === 'support' ? 'bg-[#1F293D] text-white border-blue-500' : 'text-[#94A3B8] border-[#1F293D]']">Support Swarm</button>
          </div>
        </div>

        <div class="p-5 font-mono text-xs leading-relaxed text-slate-300 min-h-[200px]">
          <div v-if="terminalTab === 'audit'" class="space-y-2">
            <div class="text-[#94A3B8]">> sphereagent.audit(repo="enterprise/auth-service")</div>
            <div class="text-slate-400 pl-4 border-l border-blue-500/30">
              <div>[AST-Parser] Constructing syntax trees across 48 Python microservices... OK (42ms)</div>
              <div>[Claude-3.5-Sonnet] Executing deep context reasoning over 184,200 tokens</div>
              <div class="text-amber-300">! DETECTED: Race condition in Redis token renewal cache (line 142)</div>
              <div class="text-emerald-300">✓ REMEDIATION AUTO-GENERATED: Applied distributed lock with test case</div>
            </div>
          </div>
          <div v-if="terminalTab === 'graph'" class="space-y-2">
            <div class="text-[#94A3B8]">> sphereagent.query_graph("Client-921 SLA Dependencies")</div>
            <div class="text-slate-400 pl-4 border-l border-amber-500/30">
              <div>[Claude-Tool] extract_entities(["Client-921", "SLA", "Dependencies"])</div>
              <div>[Cypher-Synthesizer] MATCH (c:Client)-[:SUBSCRIBED_TO]->(s:SLA) RETURN s</div>
              <div class="text-blue-300">✓ Neo4j returned 6 edge relationships in 18ms. Zero hallucination grounding.</div>
            </div>
          </div>
          <div v-if="terminalTab === 'support'" class="space-y-2">
            <div class="text-[#94A3B8]">> event_received: "Stripe payment succeeded, webhook failed"</div>
            <div class="text-slate-400 pl-4 border-l border-indigo-500/30">
              <div>[Dispatcher-Agent] Intent: Billing Sync Discrepancy</div>
              <div>[Stripe-Agent] Claude tool_call: verify_charge(id="ch_3N1987") -> Succeeded</div>
              <div class="text-purple-300">✓ Resolved in 380ms with Redis state reconciliation &amp; audit log.</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Flagship Product -->
    <section id="sphereagent" class="py-20 px-6 max-w-7xl mx-auto border-b border-[#1F293D]">
      <div class="text-center max-w-3xl mx-auto">
        <span class="font-mono text-xs text-[#F59E0B] uppercase tracking-wider bg-[#D97706]/10 px-3 py-1 rounded-full border border-[#D97706]/30">
          Proprietary Flagship Product
        </span>
        <h2 class="mt-4 text-3xl sm:text-5xl font-extrabold text-white">SphereAgent Engine</h2>
        <p class="mt-4 text-[#94A3B8]">
          Our proprietary multi-agent orchestration framework built on the Claude API for automated code auditing, knowledge graph reasoning, and intelligent customer support microservices.
        </p>
      </div>

      <div class="mt-14 grid gap-8 md:grid-cols-3">
        <div class="p-7 rounded-2xl border border-[#1F293D] bg-[#0F1626]">
          <h3 class="text-xl font-bold text-white">Automated Code Auditing</h3>
          <p class="mt-2 text-sm text-[#94A3B8]">
            Multi-pass AST analysis, race condition and vulnerability detection using Claude 3.5 Sonnet's 200k context window with automated PR generation.
          </p>
        </div>
        <div class="p-7 rounded-2xl border border-[#1F293D] bg-[#0F1626]">
          <h3 class="text-xl font-bold text-white">Knowledge Graph Reasoning</h3>
          <p class="mt-2 text-sm text-[#94A3B8]">
            Combines Claude's tool calling with Neo4j enterprise property graphs for hallucination-free, multi-hop contextual reasoning over enterprise data lakes.
          </p>
        </div>
        <div class="p-7 rounded-2xl border border-[#1F293D] bg-[#0F1626]">
          <h3 class="text-xl font-bold text-white">Intelligent Customer Microservices</h3>
          <p class="mt-2 text-sm text-[#94A3B8]">
            Stateful multi-agent swarms built on asynchronous FastAPI and Redis state stores with API transaction dispatching and guardrails.
          </p>
        </div>
      </div>
    </section>

    <!-- Services -->
    <section id="services" class="py-20 px-6 max-w-7xl mx-auto border-b border-[#1F293D]">
      <div class="text-center max-w-3xl mx-auto">
        <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Custom Software &amp; AI Services</h2>
        <p class="mt-3 text-[#94A3B8]">What our engineering team builds for clients:</p>
      </div>
      <div class="mt-12 grid gap-8 md:grid-cols-3">
        <div class="p-7 rounded-2xl border border-[#1F293D] bg-[#0F1626]">
          <h3 class="text-lg font-bold text-white">Custom AI &amp; LLM Integration</h3>
          <p class="mt-2 text-xs text-[#94A3B8] leading-relaxed">
            Enterprise RAG pipelines, Autonomous Agents, and FastAPI microservices with streaming SSE and rigorous Pydantic validation.
          </p>
        </div>
        <div class="p-7 rounded-2xl border border-[#1F293D] bg-[#0F1626]">
          <h3 class="text-lg font-bold text-white">Full-Stack Web &amp; Cloud Architecture</h3>
          <p class="mt-2 text-xs text-[#94A3B8] leading-relaxed">
            React, Next.js, Docker, Kafka event streaming, Neo4j, and cloud-native Kubernetes deployments.
          </p>
        </div>
        <div class="p-7 rounded-2xl border border-[#1F293D] bg-[#0F1626]">
          <h3 class="text-lg font-bold text-white">Computer Vision &amp; Deep Learning</h3>
          <p class="mt-2 text-xs text-[#94A3B8] leading-relaxed">
            PyTorch neural networks, transfer learning for domain models, and real-time inference with TensorRT and ONNX.
          </p>
        </div>
      </div>
    </section>

    <!-- Tech Stack -->
    <section id="stack" class="py-20 px-6 max-w-7xl mx-auto border-b border-[#1F293D]">
      <div class="text-center max-w-3xl mx-auto mb-12">
        <h2 class="text-3xl font-extrabold text-white">Architecture &amp; Tech Stack</h2>
      </div>
      <div class="grid grid-cols-2 sm:grid-cols-4 gap-4">
        <div v-for="item in techStack" :key="item.n" class="p-5 rounded-xl border border-[#1F293D] bg-[#0F1626]">
          <div class="text-sm font-bold text-white">{{ item.n }}</div>
          <div class="text-[11px] text-[#94A3B8] mt-1">{{ item.d }}</div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer id="team" class="py-20 px-6 max-w-7xl mx-auto text-center">
      <h2 class="text-3xl font-extrabold text-white">Built by the StakeSphere Engineering Team</h2>
      <div class="mt-10 grid sm:grid-cols-2 gap-6 max-w-3xl mx-auto">
        <div class="p-6 rounded-xl border border-[#1F293D] bg-[#0F1626] text-left">
          <h3 class="text-lg font-bold text-white">Wajahat Joyo</h3>
          <p class="text-xs text-blue-400 font-mono">Co-Founder &bull; Lead AI Engineer</p>
          <div class="mt-4 flex items-center justify-between">
            <a href="mailto:wajahat.joyo@stakesphere.me" class="text-xs text-slate-300 hover:text-white">wajahat.joyo@stakesphere.me</a>
            <button @click="handleCopyEmail('wajahat.joyo@stakesphere.me')" class="text-[11px] font-mono px-2 py-1 bg-black/40 border border-[#1F293D] rounded">
              {{ copiedEmail === 'wajahat.joyo@stakesphere.me' ? 'Copied!' : 'Copy' }}
            </button>
          </div>
        </div>
        <div class="p-6 rounded-xl border border-[#1F293D] bg-[#0F1626] text-left">
          <h3 class="text-lg font-bold text-white">Ahad Dev</h3>
          <p class="text-xs text-indigo-400 font-mono">Co-Founder &bull; Systems Architect</p>
          <div class="mt-4 flex items-center justify-between">
            <a href="mailto:ahad.dev@stakesphere.me" class="text-xs text-slate-300 hover:text-white">ahad.dev@stakesphere.me</a>
            <button @click="handleCopyEmail('ahad.dev@stakesphere.me')" class="text-[11px] font-mono px-2 py-1 bg-black/40 border border-[#1F293D] rounded">
              {{ copiedEmail === 'ahad.dev@stakesphere.me' ? 'Copied!' : 'Copy' }}
            </button>
          </div>
        </div>
      </div>

      <div class="mt-14 border-t border-[#1F293D] pt-8 text-xs text-[#94A3B8]">
        &copy; 2026 StakeSphere (stakesphere.me). All rights reserved. Powered by the Anthropic Claude API.
      </div>
    </footer>
  </div>
</template>
