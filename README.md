# TPaper
Transformers Paper Presentation

## Background
* Language models (LMs) like BERT, GPT-3, have grown enormously in size in recent years, achieving high performance on NLP benchmarks.
* Key innovations enabling growth include Transformer architectures, pretraining objectives like masked language modeling, and web-scale training data.
* For example, models have gone from millions of parameters (BERT) to hundreds of billions (GPT-3) to over a trillion (Switch-C).
* But bigger models require more compute, data, fine-tuning, and have risks like environmental costs, financial costs, and encoding biases

## Problem
* Ever larger LMs incur high environmental and financial costs that limit access.
* Massive web scraped training data likely encodes hegemonic worldviews that harm marginalized groups.
* LMs don't actually understand language, but can manipulate linguistic form to game benchmarks.
  
## Approach
* Evaluate models on efficiency and carefully curate training data instead of web scraping.
* Focus research on understanding model capabilities, not just leaderboard performance.
* Perform pre-deployment testing like pre-mortems to surface risks.

# Mistral
* [Mistral](https://docs.mistral.ai) is a smaller LM with only 7 billion parameters that has shown strong performance on NLP tasks.
* It demonstrates that large parameter counts are not always necessary for good performance.
* Smaller models like Mistral should be explored as an alternative to ever larger models.
  
## Mistral VS GPT-4
### Mistral
Parameters = 7.3 billion
Model Architecture:
* Decoder-based LM
* Sliding Window Attention
* Grouped Query Attention (GQA)
Training:
* Masked language modeling
* Next sentence prediction
* Machine translation

### GPT-4
Parameters = 175 billion
Model Architecture:
* Embedding layers
* 96 Transformer layers (for GPT-3) - GPT-4 number not known
* Output layer
Training:
* Masked language modeling
* Next sentence prediction
  
### Key differences 
* Mistral-7B has fewer parameters compared to GPT-3 (and most likely GPT-4)
* Mistral-7B and GPT-4 have different architectural choices and training objectives
* The efficiency, task generalization, and performance comparison would require more detailed information.



## Critical Analysis
* The paper details several risks that could arise from deploying large language models into real-world systems:
* Stereotyping and bias risks: LMs trained on insufficiently curated web data may perpetuate harmful stereotypes about marginalized groups. This could lead to psychological harms, discrimination, and subjugation for affected groups.
* Misuse risks: Bad actors could deliberately misuse convincing LM-generated text for purposes like disinformation campaigns or extremist recruitment. This raises concerns about automation of propaganda.
* Meaning attribution risks: Humans tend to mistakenly ascribe coherent meaning to LM output, even though LMs have no grounding in real meaning or intent. This risks ascribing accountability to an unaccountable system.
* The authors frame these as "dual use" problems where the technology has some beneficial applications but also poses broader societal risks. This suggests a need for targeted interventions that mitigate harms while preserving benefits.
* The risks highlight fundamental tensions in this research area - between open dissemination and careful control, between advances on leaderboards and real social impact, between excitement at synthetic fluency and humility about what has not yet been achieved.
* The paper argues convincingly that the field needs to confront these tensions directly in order to steer research and applications of large LMs to socially beneficial ends. Doing so requires transparency about risks, avoiding hype, centering affected voices, and focusing always on the long-term goals we hope this technology will serve.
  
## Resource Link - Citations
* Bender, E.M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?. Proceedings of FAccT. https://doi.org/10.1145/3442188.3445922
* Gebru, T., Morgenstern, J., Vecchione, B., Vaughan, J. W., Wallach, H., Daumeé III, H., & Crawford, K. (2020). Datasheets for datasets. arXiv preprint arXiv:1803.09010.
* Birhane, A., & Prabhu, V. U. (2021). Large image datasets: A pyrrhic win for computer vision?. ICCV 2021 Workshop on Values in Vision.
* Bender, E. M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). On the Dangers of Stochastic Parrots for Social Good. Proceedings of ACM FAccT.
* De Cao, N., Aziz, W., & Titov, I. (2021). Mistral: A Minimal Architecture for Multitask Learning. Transactions of the Association for Computational Linguistics, 9, 1269-1285.
