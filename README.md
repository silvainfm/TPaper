# On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?
By Emily M. Bender, Angelina McMillan-Major, Timnit Gebru, Shmargaret Shmitchell
Published on March 1st 2021.

## Background
* Language models (LMs) like BERT, GPT-3, have grown enormously in size in recent years, achieving high performance on NLP benchmarks.
* Key innovations enabling growth include Transformer architectures, pretraining objectives like masked language modeling, and web-scale training data.
* For example, models have gone from millions of parameters (BERT) to hundreds of billions (GPT-3) to over a trillion (Switch-C).
* But bigger models require more compute, data, fine-tuning, and have risks like environmental costs, financial costs, and encoding biases

<img width="566" alt="Screenshot 2023-10-27 at 17 11 46" src="https://github.com/silvainfm/TPaper/assets/61249160/0fdac739-7f32-4ad2-9023-ca6e80038360">

### Question: Are ever larger LMs inevitable or necessary? 

## Problem
* Ever larger LMs incur high environmental and financial costs that limit access.
* Massive web scraped training data likely encodes hegemonic worldviews that harm marginalized groups.
* LMs don't actually understand language, but can manipulate linguistic form to game benchmarks. (most probable next token)
* Could be used for propaganda - malicious intent and manipulation of narratives
  
## Approach
* The old machine learning adage "Garbage In, Garbage Out" applies here.
* Evaluate models on efficiency and carefully curate training data instead of web scraping. Focus on data engineering.
* Focus research on understanding model capabilities, not just leaderboard performance.
* Perform pre-deployment testing like pre-mortems to surface risks.

# Mistral
* [Mistral](https://docs.mistral.ai) is a smaller LM with only 7 billion parameters that has shown strong performance on NLP tasks.
* It demonstrates that large parameter counts are not always necessary for good performance.
* Smaller models like Mistral should be explored as an alternative to ever larger models.
  
## Mistral VS GPT-4
### Mistral - Pseudocode
Parameters = 7.3 billion
Model Architecture:
* Decoder-based LM
* Sliding Window Attention
* Grouped Query Attention (GQA)
Training:
* Masked language modeling
* Next sentence prediction
* Machine translation

[Code demo from Harper Carroll](https://github.com/brevdev/notebooks/blob/main/mistral-finetune-own-data.ipynb)

### GPT-4 - Pseudocode
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

### Question: How much cheaper to run is Mistral VS GPT-4? (give an order of magnitude)

### Cost differences
<img width="729" alt="cost_mVSg" src="https://github.com/silvainfm/TPaper/assets/61249160/50f669bc-1aa1-4560-80dd-af7572530486">

From "Mistral 7B is 187x cheaper compared to GPT-4"

## Critical Analysis
What the authors overlook: 
* Benefits of large models - The authors focus heavily on risks and limitations, but could acknowledge more potential benefits, like usefulness for accessible AI applications. This would strengthen the overall balanced analysis.
* Incremental approaches - While the paper advocates for small data and models, they could also propose incremental ways to scale up safely, leveraging techniques like staged model releases. A nuanced middle path between massive models and tiny models could be carved out.
* Positive initiatives - Though critical overall, they overlook some positive work happening around equity, accountability, and transparency in AI. Highlighting progress could constructively advance goals.

What could be futher developed: 
* Concrete guidance - The authors take a high level view but could go further in providing concrete guidance and actionable steps for model development, documentation, testing... 
* Engagement with affected groups - More direct engagement with marginalized populations could surface overlooked concerns and make proposals more responsive to community needs.
* Long-term policy - they could look beyond technical interventions to long-term policy, regulation, and governance to align LM development with social good. More focus here could strengthen impact.

## Conclusion
* Several risks that could arise from deploying large language models into real-world systems:
  * Stereotyping and bias risks: LMs trained on insufficiently curated web data may perpetuate harmful stereotypes about marginalized groups. This could lead to psychological harms, discrimination, and subjugation for these groups.
  * Misuse risks: Bad actors could misuse convincing LM-generated text for purposes like disinformation campaigns or extremist recruitment. This raises concerns about automation of propaganda. For example, scams could become more convincing...
  * Meaning attribution risks: Humans tend to mistakenly trust meaning to LM output, even though LMs have no grounding in real meaning or intent. This risks attributing accountability to an unaccountable system.
* The authors frame these as "dual use" problems where the technology has some beneficial applications but also poses broader societal risks. This suggests a need for targeted interventions that mitigate harms while preserving benefits.
* The risks highlight fundamental tensions in this research area - between open dissemination and careful control, between advances on leaderboards and real social impact, between excitement at synthetic fluency and humility about what has not yet been achieved.
* The paper argues convincingly that the field needs to confront these tensions directly for better research and applications of large LMs to socially beneficial ends. This requires transparency about risks, avoiding hype, centering affected voices, and focusing always on the long-term goals we hope this technology will serve.
  
## Resources & Citations
* Bender, E.M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?. Proceedings of FAccT. https://doi.org/10.1145/3442188.3445922
* Gebru, T., Morgenstern, J., Vecchione, B., Vaughan, J. W., Wallach, H., Daumeé III, H., & Crawford, K. (2020). Datasheets for datasets. arXiv preprint arXiv:1803.09010.
* Bender, E. M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). On the Dangers of Stochastic Parrots for Social Good. Proceedings of ACM FAccT.
* [Mistral 7B is 187x cheaper compared to GPT-4](https://www.linkedin.com/pulse/mistral-7b-187x-cheaper-compared-gpt-4-tzejf#:~:text=%2B%20Follow%20Mistral%207B%20is,window%20attention.%20Group)
* [ChatGPT-4 versus Mistral AI 7B](https://www.linkedin.com/pulse/chatgpt-4-versus-mistral-ai-7b-thibaud-cainne#:~:text=After%20a%20few%20hours%20struggling,4%20gives%20better)
* [Mistral Code Demo - finetuning on your own data](https://github.com/brevdev/notebooks/blob/main/mistral-finetune-own-data.ipynb)

