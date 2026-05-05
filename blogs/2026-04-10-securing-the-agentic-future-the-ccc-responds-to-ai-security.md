---
title: "Securing the Agentic Future: The CCC Responds to AI Security Consultations on Both Sides of the Atlantic"
url: "https://confidentialcomputing.io/2026/04/10/securing-the-agentic-future-the-ccc-responds-to-ai-security-consultations-on-both-sides-of-the-atlantic/"
date: "Fri, 10 Apr 2026 20:12:19 +0000"
author: "Confidential Computing Consortium"
feed_url: "https://confidentialcomputing.io/feed/"
---
<figure class="wp-block-image size-large"><img alt="" class="wp-image-3985" height="536" src="https://confidentialcomputing.io/wp-content/uploads/sites/10/2026/04/Blog-3-1024x536.jpg" width="1024" /></figure>



<p>The Confidential Computing Consortium (CCC) has recently submitted formal responses to two major government consultations on AI security: the US National Institute of Standards and Technology (NIST) Request for Information on the secure development and deployment of AI agent systems (NIST-2025-0035), and the UK Government&#8217;s Department for Science, Innovation and Technology (DSIT) Call for Information on Secure AI Infrastructure. Taken together, these responses make a consistent and compelling case: as AI systems become foundational to national security, public services, and economic competitiveness, hardware-enforced trust must become a foundational layer of AI infrastructure.</p>



<h2 class="wp-block-heading"><strong>A Shared Threat Landscape</strong></h2>



<p>Both responses begin from the same premise: AI agent systems face a category of risk that conventional cybersecurity tools were not designed to address. The threats are not merely traditional data breaches, they target the unique characteristics of AI itself.</p>



<p>Key risks highlighted across both submissions include:</p>



<ul class="wp-block-list">
<li><strong>Model weight theft</strong>, where proprietary model weights can be exfiltrated through API abuse or direct memory dumps by malicious insiders or compromised infrastructure</li>



<li><strong>The infrastructure trust gap</strong>, where standard cloud security protects against external attackers but leaves model weights and inference data accessible to the cloud provider&#8217;s hypervisor or privileged administrators</li>



<li><strong>Memory scraping and cold boot attacks</strong>, which can extract sensitive context, credentials, or cryptographic material from unprotected RAM</li>



<li><strong>Memory poisoning</strong>, where adversarial content injected into an agent&#8217;s long-term memory is triggered later, with the temporal gap between injection and execution making detection very difficult</li>



<li><strong>MCP-specific threats</strong> (highlighted in the NIST response), including shadow servers, tool poisoning, and confusion attacks that undermine the integrity of agent-to-tool communication</li>



<li><strong>&#8220;Confused deputy&#8221; attacks</strong> in multi-agent systems, where a compromised agent manipulates another into sharing sensitive data without adequate authentication</li>
</ul>



<h2 class="wp-block-heading"><strong>Why Confidential Computing Is the Answer</strong></h2>



<p>The central recommendation of both responses is that protecting AI systems requires moving beyond perimeter-based controls toward architectures rooted in hardware-enforced trust; specifically, attested, hardware-based Trusted Execution Environments (TEEs).</p>



<p>Confidential Computing addresses several of these risks directly:</p>



<ul class="wp-block-list">
<li><strong>Data-in-use protection</strong> encrypts agent memory and model weights during processing, ensuring that even cloud providers and privileged infrastructure operators cannot access sensitive workloads</li>



<li><strong>Remote attestation</strong> cryptographically verifies that the correct, unmodified agent code is running on a genuine, trusted platform before any secrets are released, providing technical guarantees rather than mere contractual assurances</li>



<li><strong>Cryptographically assured workload identity</strong> gives each agent an ephemeral identity rooted in hardware attestation, replacing static API keys with dynamic, verifiable credentials</li>



<li><strong>Key Broker Services</strong> release decryption keys and credentials only after successful attestation, meaning that if the environment doesn&#8217;t match an approved policy, keys are simply not released</li>



<li><strong>Confidential Inference</strong> (highlighted in the UK response) keeps user prompts encrypted in transit, decrypting them only inside an attested TEE, preventing cloud operators or intermediaries from accessing prompt contents</li>
</ul>



<p>The UK response also draws attention to the need to extend these protections to accelerators such as GPUs, which in multi-tenant environments represent a significant attack vector, and to future-proof the transport layer against &#8220;Store Now, Decrypt Later&#8221; attacks using Post-Quantum Cryptography (PQC).</p>



<h2 class="wp-block-heading"><strong>Looking Ahead: Agentic Zero Trust and Standardisation</strong></h2>



<p>As AI agents become more capable and autonomous, potentially holding wallet keys, signing transactions, and communicating with other agents, the CCC&#8217;s responses call for a shift toward what we describe as Agentic Zero Trust: a model where every inter-agent interaction is cryptographically authenticated, and where an agent&#8217;s identity is bound to its code measurement rather than a pre-shared secret.</p>



<p>Both responses also call on governments to take an active role in standardisation. The NIST response urges the US to define clear &#8220;Confidential AI&#8221; assurance levels so that AI providers can credibly demonstrate they are technically unable to access user data. The UK response similarly highlights the need to standardise attestation reports across hardware vendors – AMD, Intel, Arm, and NVIDIA – to enable a unified root of trust across the UK AI sector.</p>



<p>On the supply chain side, the NIST response raises a specific concern: MCP authentication is currently optional by design and package signing is inconsistently required, creating risks at every startup. Both responses make clear that governance assurances are not a substitute for cryptographic guarantees.</p>



<h2 class="wp-block-heading"><strong>Read the Full Responses</strong></h2>



<p>These are just highlights from two detailed submissions that together cover threat modelling, technical controls, patching challenges for stateful agents in TEEs, monitoring constraints imposed by Confidential Computing, and much more.</p>



<p><a href="https://www.linuxfoundation.org/hubfs/Confidential%20Computing%20Consortium/CCC%20response%20to%20NIST-2025-0035-001.pdf">Read the CCC&#8217;s full response to NIST-2025-0035 →</a></p>



<p><a href="https://www.linuxfoundation.org/hubfs/Confidential%20Computing%20Consortium/CCC%20response%20to%20UK%20Gov_%20Secure%20AI%20infrastructure%20CFI.pdf">Read the CCC&#8217;s full response to the UK Government&#8217;s Secure AI Infrastructure Call for Information →</a></p>
