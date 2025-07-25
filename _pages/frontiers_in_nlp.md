---
layout: page
permalink: /frontiers-in-NLP
title: Frontiers in NLP
in_navbar: false
---

#### Frontiers in NLP

> <span style="font-size:1.6em;">Thursday, July 17, 12:30 - 17:40 </span> <br>
> <span style="font-size:1.6em;">[UBC Computer Science Department-ICICS X836]()</span> <br>

<div style="text-align: center; margin-top: 20px;">
  <a href="https://docs.google.com/forms/d/e/1FAIpQLScp2r-RSRdcw1T862ArSZIcJHyo-hEsgCE9H5LWwHAQX-DOvg/viewform?usp=dialog" style="display: inline-block; padding: 10px 20px; font-size: 16px; color: white; background-color: #007BFF; border-radius: 5px; text-decoration: none;">Register Now</a>
</div>


<h5> Invited Speakers </h5>

<div style="display: flex; flex-direction: column; align-items: center; gap: 0px;">
<div style="text-align: center; margin: 10px;">
    <img src="/assets/img/frontiers-in-nlp/YuvalPinter.jpeg" alt="Yual Pinter" style="width: 150px; height: 150px; object-fit: cover; border-radius: 50%;">
    <p><strong>Yuval Pinter</strong><br>Ben Gurion University<br></p>
    <details style="text-align:left">
      <summary><strong>Talk Title:</strong> Building Character: Tokenization in Theory and in Practice </summary>
      <p><strong>Abstract:</strong> The end-to-end nature of recent NLP models, most prominently large language models (LLMs), makes it hard for us to figure out how their individual processing steps are affected by properties of text and language, for example how they represent individual words in alignment with how humans perceive them and build utterances from the bottom up. We can find instances where models struggle with lexical changes in register, domain, or innovation, but the underlying mechanisms still mostly elude us. </br>In this talk, I will focus on the lexical and sub-lexical levels of LLM representations, challenging models with recognition of words and the processes they are formed through, looking at subword tokenization algorithms from the point of view of their downstream performance requirements and the challenges posed by different languages. I will present SaGe, a subword tokenizer that incorporates context into the vocabulary creation objective; BoundlessBPE, which allows breaking past the limits of regex pretokenization; and Splinter, a pre-tokenization algorithm that relinearizes Hebrew text to conform the concatenative tokenization pipeline with Semitic templatic morphology.</p>
      <p><strong>Bio:</strong> Yuval Pinter is a Senior Lecturer in the Department of Computer Science at Ben-Gurion University of the Negev, focusing on NLP as PI of the MeLeL lab. Yuval got his PhD at the Georgia Institute of Technology School of Interactive Computing as a Bloomberg Data Science PhD Fellow. Prior to this, he worked as a Research Engineer at Yahoo Labs and as a Computational Linguist at Ginger Software, and obtained an MA in Linguistics and a BSc in CS and Mathematics, both from Tel Aviv University.</p>
    </details>
  </div><br/>

  <div style="text-align: center; margin: 10px;">
    <img src="/assets/img/frontiers-in-nlp/Tuhin-Chakrabarty.png" alt="Tuhin Chakrabarty" style="width: 150px; height: 150px; object-fit: cover; border-radius: 50%;">
    <p><strong>Tuhin Chakrabarty</strong><br>Stony Brook University</p>
    <details style="text-align:left">
      <summary><strong>Talk Title:</strong> GPTs are Un‘fair’ : An Early Look at the Labor Market Dilution Potential by Training on Copyrighted Data </summary>
      <p><strong>Abstract:</strong> Prior work on Generative AI and Copyright has primarily focused on memorization and verbatim regurgitation of copyrighted data that may or may not violate Fair Use. The fourth fair use factor instructs courts to inquire into the effect of the use upon the potential market for or value of the copyrighted work. While there's been compelling arguments in Copyright cases alongside few anecdotal evidences on how training AI on copyrighted books poses risk towards potential dilution of labor market, there has been no large scale data driven empirical research to support such claims.  To understand impact of AI on the Future of Creative Labor we conducted a large scale behavioral experiment where MFA candidates from top writing programs in the US were pitted against state of the art large language models. MFA candidates were compensated to reproduce an excerpt written by an award winning author using the authors distinctive style and voice based on a provided content. LLMs were then assigned to perform the same task under two treatment conditions— i) using the same long context, few shot prompts provided to MFAs ii) by fine-tuning on authors entire oeuvre. Through planned pairwise contrasts and blind assessments between treatment conditions we evaluated the resulting excerpts by both experts and lay readers recruited from Prolific who rate each pair on (i) overall writing quality and (ii) stylistic fidelity to the original author without knowing if a given text was human written or AI-generated. Our results reveal striking differences between AI approaches across lay readers and experts. Lay readers consistently preferred AI-generated excerpts over MFA-written ones regardless of the treatment condition. In contrast based on expert judgements, while in-context prompting produced excerpts were less favored than those written by MFA candidates,  excerpts generated by fine-tuned models surpassed MFAs. These findings empirically validate several commenters' assertions that fine-tuning requires distinct considerations under the first fair use factor. Equally concerning, analysis using Pangram (a state of art AI detection tool) revealed stark detectability contrasts. Few-shot AI-generated text was identified with 100% accuracy, while fine-tuned AI outputs achieved an alarmingly low 0% detection rate.  Fine-tuned models produce undetectable, high-quality outputs competing directly with human creators, potentially devaluing original work and undermining economic incentives copyright law protects. Additionally preference of AI generated text among lay readers is particularly significant as they represent the actual consumer. These results demonstrate compelling early evidence that unauthorized use of copyrighted data poses genuine threats to creative labor markets.</p>
      <p><strong>Bio:</strong> Tuhin Chakrabarty is  Assistant Professor at the Computer Science Department in Stony Brook University (SUNY). Prior to this he obtained his PhD from Columbia University where his research supported by an Amazon Fellowship and a NYTimes R&D fellowship.His research interests are broadly in AI, NLP and Human AI Interaction and his goal is to design and build reliable AI systems that can handle implicature and ambiguity, understand human behavior and are aligned with the requirements humans have from technology. His research often relies on knowledge, methods, and perspectives from multiple disciplines to address complex problems or questions that cannot be fully understood or solved within the boundaries of Computer Science. Tuhin's work has been covered in MIT Tech Review, Bloomberg, Washington Post and he has been the receipent of Best Paper Honorable Mention award at ACM CHI and more recently an Outstanding Position Paper award at ICML for his focus on building  prioritizing Human Centered AI.</p>
    </details>
  </div><br/>
  
  <div style="text-align: center; margin: 10px;">
    <img src="/assets/img/frontiers-in-nlp/sarahwiegreffe.jpeg" alt="Sarah Wiegreffe" style="width: 150px; height: 150px; object-fit: cover; border-radius: 50%;">
    <p><strong>Sarah Wiegreffe</strong><br>Allen Institute for AI</p>
    <details style="text-align:left">
      <summary><strong>Talk Title:</strong> Demystifying the Inner Workings of Language Models </summary>
      <p><strong>Abstract:</strong> Large language models (LLMs) power a rapidly-growing and increasingly impactful suite of AI technologies. However, due to their scale and complexity, we lack a fundamental scientific understanding of much of LLMs’ behavior, even when they are open source. The “black-box” nature of LMs not only complicates model debugging and evaluation, but also limits trust and usability. In this talk, I will describe how my research on interpretability (i.e., understanding models’ inner workings) has answered key scientific questions about how models operate. I will then demonstrate how deeper insights into LLMs’ behavior enable both 1) targeted performance improvements and 2) the production of transparent, trustworthy explanations for human users.</p>
      <p><strong>Bio:</strong> Sarah Wiegreffe is a current postdoctoral researcher at the Allen Institute for AI (Ai2) and the University of Washington, and an incoming (starting in August) assistant professor of Computer Science at the University of Maryland. She has worked on the explainability and interpretability of neural networks for NLP since 2017, with a focus on understanding how language models make predictions in order to make them more transparent to human users. She has been honored as a 3-time Rising Star in EECS (2023), Machine Learning (2024), and Generative AI (2024). She received her PhD in Computer Science from Georgia Tech in 2022, during which time she interned at Google and Ai2 and won the Ai2 outstanding intern award. She frequently serves on conference program committees, receiving outstanding area chair awards at ACL 2023 and EMNLP 2024. Her website is https://sarahwie.github.io/.</p>
    </details>
    
  </div><br/>
  
  <div style="text-align: center; margin: 10px;">
    <img src="/assets/img/frontiers-in-nlp/Yossi_Levi.jpg" alt="Yossi Levi" style="width: 150px; height: 150px; object-fit: cover; border-radius: 50%;">
    <p><strong>Yossi Levi</strong><br>Technion</p>
    <details style="text-align:left">
      <summary><strong>Talk Title:</strong> CLIP Latent space geometry </summary>
      <br><strong>Abstract:</strong> The talk covers two papers to be presented at ICML 2025. I will present our recent work analyzing the geometry of CLIP’s latent space from both geometric and probabilistic perspectives. We show that the embedding space is better characterized by two distinct, shifted ellipsoids, rather than a shared hypersphere. This finding challenges common assumptions about CLIP’s latent structure.</br>Building on this double-ellipsoid perspective, we introduce a new measure called conformity, which captures how closely a sample aligns with its modality mean. We observe that common concepts tend to align closely with the modality mean, while rare ones are significantly offset, suggesting a geometric analogue for the notion of concept commonality.</br>Finally, I will introduce Whitened CLIP (W-CLIP) — a simple, linear transformation of the latent space into an isotropic space. It enables the use of embedding norms as a surrogate for likelihood approximation. This approach supports a wide range of applications, including domain shift detection and the identification of generative artifacts.</p>
      <p><strong>Bio:</strong> Meir Yossef Levi (Yossi Levi) is in the final stages of his Ph.D. at the Technion, advised by Prof. Guy Gilboa, after receiving both his B.Sc. and M.Sc. in Electrical Engineering from the Technion. His research focuses on multimodal representation learning, with a particular interest in understanding the latent geometry of vision-language models and its implications. His recent work centers on CLIP, with two papers accepted to ICML 2025 on this topic. Prior to this, he studied robust classification in 3D vision, with publications at ICCV and 3DV.</p>
    </details>
  </div><br/>
  
  <div style="text-align: center; margin: 10px;">
    <img src="/assets/img/frontiers-in-nlp/aaron-mueller.jpg" alt="Aaron Mueller" style="width: 150px; height: 150px; object-fit: cover; border-radius: 50%;">
    <p><strong>Aaron Mueller</strong><br>Boston University</p>
    <details style="text-align:left">
      <summary><strong>Talk Title:</strong> How Do Language Models Think? A Causal Framework for Understanding Language Model Representations</summary>
      <p><strong>Abstract:</strong> The goal of language model (LM) interpretability is to explain the behaviors of LMs in terms of their internal computations. Achieving this could enable us to predict LM behaviors on future examples, or to precisely steer or edit their behaviors.  However, current interpretability methods lack principled foundations; there is little consensus on what the most effective scientific abstractions are, or how to evaluate progress. This talk is guided by two questions: (i) What are the right terms and abstractions for describing the inner workings of a language model? (ii) How would we know when we’ve found the right abstraction? I will first present a causal framework for LM interpretability designed to address these questions. Building on this framework, I will then discuss the more practical problem of building a concrete evaluation standard for the field. I will present insights from our recent work on building a mechanistic interpretability benchmark, which enables systematic comparison of different approaches to understanding model mechanisms. I will conclude by discussing an underexplored open problem: the presence of non-human-like concepts in language models. I will briefly discuss how this complicates our ability to understand and validate mechanistic explanations, and discuss ongoing work focused on understanding when and why non-human-like concepts arise in LMs—and what we could do with them.</p>
      <p><strong>Bio:</strong> Aaron Mueller is an assistant professor in the Department of Computer Science at Boston University. His research centers on developing language modeling methods and evaluations inspired by causal and linguistic principles, and applying these for precise model control and improved efficiency. He completed a Ph.D. at Johns Hopkins University and was a Zuckerman postdoctoral fellow at Northeastern and the Technion. His work has been published in ML and NLP venues (such as ICLR, ACL, and EMNLP) and has won awards at TMLR and ACL. He has recently been featured in the New York Times (2023) and IEEE Spectrum (2024) as an organizer of the BabyLM Challenge.</p>
    </details>
  </div>
</div><br/>


<div style="display: flex; flex-wrap: wrap;">

  <!-- Schedule section -->
  <div style="width: 70%; padding-right: 20px;">
    <h5> Schedule </h5>
    <div style="border: 1px solid #ddd; padding: 10px; border-radius: 5px; background-color: #f9f9f9;">
      <ul style="list-style-type: none; padding: 0;">
        <li style="padding: 5px 0;"><strong>12:30 - 13:15</strong> &mdash; Lunch</li>
        <li style="padding: 5px 0;"><strong>13:15 - 14:05</strong> &mdash; Yuval Pinter <em>(Ben Gurion University of the Negev)</em></li>
        <li style="padding: 5px 0;"><strong>14:05 - 14:55</strong> &mdash; Tuhin Chakrabarty <em>(Stony Brook University)</em></li>
        <li style="padding: 5px 0;"><strong>14:55 - 15:15</strong> &mdash; Break</li>
        <li style="padding: 5px 0;"><strong>15:15 - 16:05</strong> &mdash; Sarah Wiegreffe <em>(Allen Institute for AI)</em></li>
        <li style="padding: 5px 0;"><strong>16:05 - 16:55</strong> &mdash; Yossi Levi <em>(Technion)</em></li>
        <li style="padding: 5px 0;"><strong>16:45 - 17:40</strong> &mdash; Aaron Mueller <em>(Boston University)</em></li>
      </ul>
    </div>
  </div>

  <!-- Organizers section -->
  <div style="width: 30%;">
    <h5> Organizers  </h5>
    <div style="display: flex; flex-direction: column; align-items: center;">
      <div style="text-align: center; margin-top: 30px;">
        <img src="/assets/img/frontiers-in-nlp/vered-shwartz.png" alt="Vered Shwartz" style="width: 150px; height: auto; ">
        <p><br>Vered Shwartz<br>UBC & Vector Institute</p>
      </div>
    </div>
  </div>

</div>


For questions, issues and inquiries, please email vshwartz@cs.ubc.ca
