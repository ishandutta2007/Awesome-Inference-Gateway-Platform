# Awesome-Inference-Gateway-Platform

## Top Inference Gateway Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on LLM Routing, Multi-Provider Proxying, Fallbacks, Caching, Guardrails, Cost Control & Unified OpenAI-Compatible APIs*

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Inference Gateways** (also called AI Gateways or LLM Gateways). These systems sit between applications and model providers—normalizing APIs, routing requests, enforcing budgets and rate limits, adding fallbacks, caching, observability, and guardrails.



**Examples** include Kong AI Gateway, Envoy AI Gateway, Portkey, LiteLLM, OpenRouter, Cloudflare AI Gateway, TrueFoundry AI Gateway, Zuplo, Gravitee, Gloo, Baseten, Together AI, Fireworks AI, GroqCloud, Tyk AI Gateway, and Apache APISIX AI Gateway (the category leaders).



**Open-source emphasis**: Inference gateways have strong open-source options. **LiteLLM**, **Envoy AI Gateway**, **Kong** (core), **Apache APISIX**, and related projects let teams self-host unified LLM proxies with full control. Commercial platforms add managed scale, enterprise guardrails, and zero-ops. This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms

- **[Portkey](https://portkey.ai/)**  

  Comprehensive AI gateway platform with unified access to 1,600+ models, observability, guardrails, prompt management, and enterprise security (open-source core + managed cloud).



- **[OpenRouter](https://openrouter.ai/)**  

  Managed multi-model marketplace and gateway providing a single API to hundreds of models with simple routing and pay-as-you-go access.



- **[Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/)**  

  Edge-native AI gateway integrated with the Cloudflare platform—caching, rate limiting, analytics, and low-latency routing for major providers.



- **[TrueFoundry AI Gateway](https://www.truefoundry.com/)**  

  Enterprise AI gateway and platform for model routing, governance, observability, and deployment across cloud and on-prem environments.



- **[Zuplo AI Gateway](https://zuplo.com/)**  

  API management platform with AI gateway capabilities for routing, authentication, and developer experience around LLM traffic.



- **[Gravitee AI Gateway](https://www.gravitee.io/)**  

  API management and gateway platform extended for AI/LLM traffic with policy enforcement and observability.



- **[Gloo AI Gateway (Solo.io)](https://www.solo.io/)**  

  Envoy-based gateway and agent gateway offerings focused on AI traffic, MCP, and enterprise service connectivity.



- **[Kong AI Gateway (Konnect / Enterprise)](https://konghq.com/)**  

  Enterprise AI capabilities on Kong’s API platform—AI Proxy, semantic caching, prompt guards, and token-based controls (advanced features often enterprise-licensed).



- **[Baseten](https://www.baseten.co/)**  

  Model inference and deployment platform with gateway-style access to hosted and custom models.



- **[Together AI](https://www.together.ai/)**  

  Inference platform and API for open and proprietary models, often used as a high-performance backend behind gateways.



- **[Fireworks AI](https://fireworks.ai/)**  

  Fast inference platform for open models with OpenAI-compatible endpoints suitable as a gateway upstream.



- **[GroqCloud](https://groq.com/)**  

  Ultra-low-latency inference cloud frequently used as a high-speed provider behind AI gateways.



- **[Nebius AI / Lepton AI and similar inference clouds](https://nebius.com/)**  

  Cloud inference providers offering APIs that gateways route to for capacity and specialized hardware.



- **[NVIDIA Dynamo / NIM-related serving](https://www.nvidia.com/)**  

  NVIDIA inference and serving stack components used in enterprise AI gateway and model-serving architectures.



- **[OctoAI and other specialized inference endpoints](https://octo.ai/)**  

  Hosted inference services commonly integrated as upstreams in multi-provider gateway setups.



## Open-Source GitHub Projects

- **[LiteLLM](https://github.com/BerriAI/litellm)**  

  Leading open-source LLM gateway and proxy—unified OpenAI-compatible interface to 100+ providers, virtual keys, budgets, fallbacks, load balancing, and cost tracking (MIT).



- **[Envoy AI Gateway](https://github.com/envoyproxy/ai-gateway)**  

  Open-source AI gateway built on Envoy for routing application traffic to GenAI services, with Kubernetes-native configuration and multi-provider support (Apache 2.0).



- **[Kong Gateway (OSS) + AI plugins](https://github.com/Kong/kong)**  

  Widely deployed open-source API gateway with AI/LLM plugins for proxying, transformation, and basic AI traffic management (advanced AI features often in Enterprise).



- **[Apache APISIX](https://github.com/apache/apisix)**  

  High-performance cloud-native API gateway with AI plugins for LLM proxying, routing, and caching—strong at scale (Apache 2.0).



- **[Tyk (OSS)](https://github.com/TykTechnologies/tyk)**  

  Open-source API gateway with dashboard and extensibility; used for AI/LLM traffic with custom middleware and policies.



- **[Portkey Gateway (open-source core)](https://github.com/Portkey-AI/gateway)**  

  Open-source AI gateway core from Portkey providing unified API access, routing, and foundational gateway features.



- **[Bifrost and high-performance LLM proxies](https://github.com/)**  

  Emerging Go-based open-source AI gateways focused on ultra-low overhead, multi-key failover, and production throughput.



- **[AISIX and APISIX-derived AI gateways](https://github.com/)**  

  Open-source AI-native gateways (including projects from APISIX creators) adding semantic routing, guardrails, and MCP support in the core.



- **[Helicone (open components / proxy)](https://github.com/Helicone)**  

  Observability-focused LLM tooling with open components that can act as or integrate with gateway-style proxies.



- **[vLLM, TGI, and OpenAI-compatible serving proxies](https://github.com/)**  

  Open inference servers that expose OpenAI-compatible APIs and are frequently placed behind or combined with gateway layers.



### Additional Strong Open-Source Options

- Deploying **LiteLLM** as the default self-hosted multi-provider proxy for most teams.

- Choosing **Envoy AI Gateway** or **Kong/APISIX** when you already run Envoy or a mature API gateway and want AI traffic to inherit existing policies.

- Using **Apache APISIX** for high-QPS, cloud-native environments that need AI plugins on a battle-tested core.

- Combining open gateways with commercial inference providers (Groq, Fireworks, Together, etc.) for best latency/cost.

- Accepting that managed guardrails, SOC2/HIPAA packages, global edge PoPs, and zero-ops still favor commercial platforms (Portkey, Cloudflare AI Gateway, OpenRouter, TrueFoundry, Kong Konnect, etc.).

- Focusing open-source efforts on zero markup, data residency, and full control of routing logic.



**Frameworks for building custom systems**: Run LiteLLM or Envoy AI Gateway as the proxy → configure providers, virtual keys, and fallbacks → add Redis/Postgres for state and budgets → enforce guardrails via plugins or external services → observe with OpenTelemetry or gateway-native logs. Suitable for platform and ML infrastructure teams. Many enterprises pair an open gateway core with a commercial control plane for governance and support.



## How to Contribute

1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.

- Inference gateways handle API keys, prompts, and potentially sensitive outputs. Self-hosted deployments require hardened secrets management, network controls, and monitoring. This list is not security or compliance advice.



---

**Made for platform engineers, MLOps teams, and developers routing LLM traffic at scale.**

Let's keep inference routing unified, observable, and as open as practical.
