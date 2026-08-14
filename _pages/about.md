---
layout: about
title: About
permalink: /
# subtitle: PhD candidate at the <a href="https://web.cs.toronto.edu/">University of Toronto</a> · Researcher at the <a href="https://vectorinstitute.ai/">Vector Institute</a>

profile:
  align: right
  image: amin-rakhsha.webp
  image_circular: false
  more_info: >
    <p style="display: block; width: 100%; text-align: center; font-family: var(--bs-body-font-family, Arial, sans-serif);">Toronto, Canada</p>
    <div class="social">
      <div class="contact-icons" style="font-size: 1.6rem; white-space: nowrap;">
        <a href="mailto:aminr@cs.toronto.edu" title="Email" aria-label="Email"><i class="fa-solid fa-envelope" aria-hidden="true"></i></a>
        <a href="https://scholar.google.com/citations?user=Uqpl3zwAAAAJ" title="Google Scholar" aria-label="Google Scholar"><i class="ai ai-google-scholar" aria-hidden="true"></i></a>
        <a href="/assets/pdf/amin-rakhsha-cv.pdf" title="CV" aria-label="CV"><i class="ai ai-cv" aria-hidden="true"></i></a>
        <a href="https://www.linkedin.com/in/amin-rakhsha-380737125" title="LinkedIn" aria-label="LinkedIn"><i class="fa-brands fa-linkedin" aria-hidden="true"></i></a>
      </div>
    </div>

selected_papers: false
social: false

announcements:
  enabled: false
  scrollable: false
  limit: 5

latest_posts:
  enabled: false
  scrollable: false
  limit: 0
---

<style>
  .post > article > .clearfix > p:not(:has(br)) {
    text-align: justify;
  }

  .research-question {
    font-size: 1.3rem;
  }

  @media (max-width: 576px) {
    .post > article > .clearfix > p:not(:has(br)) {
      text-align: left;
    }
  }
</style>

I am a PhD candidate in Computer Science at the [University of Toronto](https://web.cs.toronto.edu/), advised by [Amir-massoud Farahmand](https://academic.sologen.net/), and a PhD researcher at the [Vector Institute](https://vectorinstitute.ai/)

My research focuses on making intelligent systems that can reason and act robustly over long horizons. My work in **reinforcement learning (RL)** spans accelerated planning and learning algorithms, model-based RL with imperfect models, and adversarial attacks. More recently, I have focused on **LLM reasoning** and **AI agents**, developing efficient inference-time algorithms and evaluation frameworks for targeted post-training, partly during internships at [Autodesk AI Lab](https://www.research.autodesk.com/research-areas/science/ai-lab/) and [Qualcomm AI Research](https://www.qualcomm.com/research/artificial-intelligence).

<h2 id="education" style="margin-top: 2.5rem;">Education</h2>

---

**University of Toronto** — _PhD in Computer Science_  
September 2020–October 2026 (expected) · Toronto, Canada  
Supervisor: [Amir-massoud Farahmand](https://academic.sologen.net/)

**Sharif University of Technology** — _BSc in Computer Engineering_  
September 2020 · Tehran, Iran

<h2 id="research-experience" style="margin-top: 2.5rem;">Research Experience</h2>

---

**University of Toronto and Vector Institute** — _PhD Researcher_  
September 2020–Present · Toronto, Canada

**Qualcomm AI Research** — _Research Intern_  
June–September 2025 · Amsterdam, Netherlands

**Autodesk AI Lab** — _Research Intern_  
February–May 2025 · Toronto, Canada

**Max Planck Institute for Software Systems (MPI-SWS)** — _Research Intern and Collaborator_  
July 2019–January 2021 · Saarbrücken, Germany

**Chinese University of Hong Kong (CUHK)** — _Research Intern and Collaborator_  
July 2018–January 2019 · Hong Kong

<h2 id="selected-honors-and-awards" style="margin-top: 2.5rem;">Selected Honors and Awards</h2>

---

- **Silver Medal, International Mathematical Olympiad (IMO)** — July 2016
- Borealis AI Global Fellowship — May 2022
- Three University of Toronto Research Awards — 2020, 2021, 2023
- Iran’s National Elite Foundation Fellowship — 2015–2020

<h2 id="research-directions" style="margin-top: 2.5rem;">Research Topics</h2>

---

<h3 style="margin-top: 2rem;font-weight: bold;">AI Agents Model Evaluation</h3>

<figure style="width: 70%; margin: 1rem auto 1.5rem;">
  <img
    src="{{ '/assets/img/lumina.webp' | relative_url }}"
    alt="Comparison of conventional and specialized model-based planners"
    width="110"
    height="550"
    loading="lazy"
    decoding="async"
    style="display: block; width: 100%; height: auto;"
  >
</figure>

_What capabilities are needed to solve long-horizon agentic tasks, and which of them is the bottleneck for our model and task?_
{: .research-question }

With LUMINA, we use a POMDP formulation of agentic tasks to identify a set of critical capabilities and develop an evaluation suite that measures the importance of each capability for a model–task pair. The resulting diagnoses guide targeted model post-training and agentic system design.

<div class="publications">

{% capture lumina_publications %}
{% bibliography --query @*[keywords~=dir_lumina] --group_by none %}
{% endcapture %}
{{ lumina_publications | regex_replace: '<a href="https://doi\.org/[^"]+"[^>]*>DOI</a>', '' }}

</div>

<h3 style="margin-top: 2rem;font-weight: bold;">Parallel Test-time Scaling of LLM Reasoning</h3>

<figure style="width: 70%; margin: 1rem auto 1.5rem;">
  <img
    src="{{ '/assets/img/mob.webp' | relative_url }}"
    alt="Preview of the developed agent evaluation framework"
    width="1500"
    height="750"
    loading="lazy"
    decoding="async"
    style="display: block; width: 100%; height: auto;"
  >
</figure>

_How should we utilize parallel inference to scale LLM reasoning when no ground-truth evaluation is available?_
{: .research-question }

We propose Majority-of-the-Bests (MoB), an algorithm for selecting among independently generated LLM outputs. MoB uses bootstrapping to become more robust to noisy reward models compared to Best-of-N.

<div class="publications">

{% capture mob_publications %}
{% bibliography --query @*[keywords~=dir_mob] --group_by none %}
{% endcapture %}
{{ mob_publications | regex_replace: '<a href="https://doi\.org/[^"]+"[^>]*>DOI</a>', '' }}

</div>

<h3 style="margin-top: 2rem;font-weight: bold;">Model-based Reinforcement Learning with Imperfect Models</h3>

<figure style="width: 90%; margin: 1rem auto 1.5rem;">
  <img
    src="{{ '/assets/img/mb_planning.webp' | relative_url }}"
    alt="Comparison of conventional and specialized model-based planners"
    width="1900"
    height="950"
    loading="lazy"
    decoding="async"
    style="display: block; width: 100%; height: auto;"
  >
</figure>

_How can an RL agent utilize an erroneous model of the environment?_
{: .research-question }

In many applications, an approximate model of the environment is available that is not completely accurate: a robotic simulator, a pretrained foundation model, or a misspecified learned model. We develop specialized RL algorithms that can benefit from these models while remaining robust to the model's error.

<div class="publications">

{% capture model_based_publications %}
{% bibliography --query @*[keywords~=dir_model_based] --group_by none %}
{% endcapture %}
{{ model_based_publications | regex_replace: '<a href="https://doi\.org/[^"]+"[^>]*>DOI</a>', '' }}

</div>

<h3 style="margin-top: 2rem;font-weight: bold;">Accelerated Reinforcement Learning</h3>

<figure style="width: 50%; margin: 1rem auto 1.5rem;">
  <img
    src="{{ '/assets/img/accelerated_planning.webp' | relative_url }}"
    alt="Comparison of classical and accelerated reinforcement-learning updates toward the optimal value"
    width="640"
    height="320"
    loading="lazy"
    decoding="async"
    style="display: block; width: 100%; height: auto;"
  >
</figure>

_How can we design general and scalable acceleration methods for iterative RL algorithms, analogous to those in optimization?_
{: .research-question }

Standard iterative RL algorithms can converge slowly as the task horizon grows. We develop accelerated methods with improved convergence rates while retaining comparable per-iteration cost.

<div class="publications">

{% capture accelerated_publications %}
{% bibliography --query @*[keywords~=dir_accelerated] --group_by none %}
{% endcapture %}
{{ accelerated_publications | regex_replace: '<a href="https://doi\.org/[^"]+"[^>]*>DOI</a>', '' }}

</div>

<h3 style="margin-top: 2rem;font-weight: bold;">Adversarial Attacks in Reinforcement Learning</h3>

<figure style="width: 70%; margin: 1rem auto 1.5rem;">
  <img
    src="{{ '/assets/img/adv_attack.webp' | relative_url }}"
    alt="Adversarial manipulation of next-state and reward feedback in reinforcement learning"
    width="1520"
    height="760"
    loading="lazy"
    decoding="async"
    style="display: block; width: 100%; height: auto;"
  >
</figure>

_How vulnerable are RL agents to adversarial attacks that alter the state transitions or rewards?_
{: .research-question }

We study the security of RL systems, including training-time attacks that manipulate rewards or transition dynamics. Our work characterizes when an agent can be steered toward an adversarially chosen policy and how costly such attacks must be.

<div class="publications">

{% capture adversarial_publications %}
{% bibliography --query @*[keywords~=dir_adversarial] --group_by none %}
{% endcapture %}
{{ adversarial_publications | regex_replace: '<a href="https://doi\.org/[^"]+"[^>]*>DOI</a>', '' }}

</div>
