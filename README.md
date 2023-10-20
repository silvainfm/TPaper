# TPaper
Transformers Paper Presentation

## Background
* Language models (LMs) like BERT, GPT-3, etc have grown enormously in size in recent years, achieving high performance on NLP benchmarks.
* But bigger models require more compute, data, and have risks like encoding biases.

## Problem
* Ever larger LMs incur high environmental and financial costs that limit access.
* Massive web scraped training data likely encodes hegemonic worldviews that harm marginalized groups.
* LMs don't actually understand language, but can manipulate linguistic form to game benchmarks.
  
## Approach
* Evaluate models on efficiency and carefully curate training data instead of web scraping.
* Focus research on understanding model capabilities, not just leaderboard performance.
* Perform pre-deployment testing like pre-mortems to surface risks.

# Mistral
* Mistral is a smaller LM with only 7 billion parameters that has shown strong performance on NLP tasks.
* It demonstrates that large parameter counts are not always necessary for good performance.
* Smaller models like Mistral should be explored as an alternative to ever larger models.
  
### Sample output

### Processing overview

## Critical Analysis
* Details risks of deploying LMs including perpetuating stereotypes, being deliberately misused, and users mistakenly ascribing meaning.
* Discusses dual use problems - LMs useful for some applications but have broad societal risks.
  
## Resource Link - Citations
* Bender, E.M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?. Proceedings of FAccT. https://doi.org/10.1145/3442188.3445922
* Gebru, T., Morgenstern, J., Vecchione, B., Vaughan, J. W., Wallach, H., Daumeé III, H., & Crawford, K. (2020). Datasheets for datasets. arXiv preprint arXiv:1803.09010.
* Birhane, A., & Prabhu, V. U. (2021). Large image datasets: A pyrrhic win for computer vision?. ICCV 2021 Workshop on Values in Vision.
* Bender, E. M., Gebru, T., McMillan-Major, A., & Shmitchell, S. (2021). On the Dangers of Stochastic Parrots for Social Good. Proceedings of ACM FAccT.
* De Cao, N., Aziz, W., & Titov, I. (2021). Mistral: A Minimal Architecture for Multitask Learning. Transactions of the Association for Computational Linguistics, 9, 1269-1285.
