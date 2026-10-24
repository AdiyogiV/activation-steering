# Make an AI funnier with one vector

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AdiyogiV/activation-steering/blob/main/steer-humor.ipynb)

Activation steering in about 50 lines of PyTorch, on a small open model (Qwen2.5-1.5B). No retraining, no fine-tuning.

## Run it

1. Click **Open in Colab** above.
2. `Runtime → Run all`. A free T4 GPU is already selected. It takes about 3 minutes.
3. Move the humor slider, turn the dial, or make your own direction: pirate, Shakespeare, grumpy (watch it start refusing), anything.

## What it does

1. **Every word becomes a list of numbers.** That list is the model's activation, what it is "thinking" at that point.
2. **Find the humor direction.** The model writes funny and serious answers to the same questions. Compare its activations on the two, and the difference is the humor direction.
3. **Add it while the model runs.** Same question, same seed, no system prompt. The only change is the vector added inside the model.

## Why it matters

This is the same math as abliteration, which finds the *refusal* direction and removes it, so the model stops saying no.
Explainer with diagrams: [thread on X](https://x.com/abhi_inthewild/status/2113974169113370766).

## Further reading

- Turner et al. (2023), [Activation Addition](https://arxiv.org/abs/2308.10248)
- Panickssery et al. (2023), [Steering Llama 2 via Contrastive Activation Addition](https://arxiv.org/abs/2312.06681)
- Zou et al. (2023), [Representation Engineering](https://arxiv.org/abs/2310.01405)
- Arditi et al. (2024), [Refusal in Language Models Is Mediated by a Single Direction](https://arxiv.org/abs/2406.11717)
- Anthropic, [Golden Gate Claude](https://www.anthropic.com/news/golden-gate-claude) and [Persona vectors](https://www.anthropic.com/research/persona-vectors)

By Abhinav Vashisht · [@abhi_inthewild](https://x.com/abhi_inthewild)
