Aligning Prompting Techniques with LLM Architectures for Enhanced Mathematical Reasoning Overview

This repository contains the experimental code and evaluation pipelines corresponding to the research paper: “Aligning Prompting Techniques with LLM Architecture for Enhanced Mathematical Reasoning” The project investigates how different prompt engineering strategies interact with model size and architecture to influence mathematical reasoning performance in Large Language Models (LLMs). Using the GSM8K benchmark, we conduct a systematic comparison across multiple prompting techniques, datasets sizes, and model scales.

Research Objectives Analyze the effectiveness of different prompting techniques for mathematical reasoning Study how prompting performance varies across model sizes and architectures Evaluate robustness under different dataset scales Provide quantitative insights using accuracy-based and error-based metrics Prompting Techniques Implemented

The following prompting strategies are implemented and evaluated: Standard Prompting Direct question-answer format without intermediate reasoning Computationally inexpensive but limited for complex reasoning tasks

Chain-of-Thought (CoT) Prompting Encourages step-by-step reasoning before producing the final answer Improves reasoning accuracy, especially for larger models

Meta Prompting Uses structured, reflective instructions guiding the reasoning process Aims to reduce ambiguity and improve consistency

Meta Few-Shot Prompting Combines meta-level instructions with few-shot examples Enables models to generalize reasoning strategies more effectively Models Evaluated

Experiments are conducted on the following LLMs: Google Flan-T5 Small (80M) Base (250M) Large (780M) Gemma 3 (1B) LLaMA 3.2 (3B) Both Hugging Face–based and locally deployed (Ollama) models are used to ensure architectural diversity.

Dataset GSM8K (Grade School Math 8K) Training set: 7,743 questions Testing set: 1,300 questions Subsets of 100, 1000, and 7473 questions are used to analyze scaling behavior.

Methodology Preprocessing Text normalization and cleaning Numeric word-to-digit conversion Mathematical symbol standardization Ground-truth answer extraction Prompt Application Each question is evaluated using all prompting strategies Experiments repeated across different dataset sizes Evaluation

Model outputs are assessed using: Binary Accuracy Closeness Accuracy Error Rate R² (Coefficient of Determination) MSE, RMSE MAPE, SMAPE This combination ensures both exact correctness and approximate numerical reliability are captured.

Key Findings No single prompting technique is universally optimal Chain-of-Thought prompting benefits larger models the most Meta Few-Shot prompting achieves the highest overall closeness accuracy Smaller models show more stable improvements under Meta and Meta Few-Shot prompting Dataset size significantly affects prompt effectiveness and regression stability These findings emphasize the importance of aligning prompting strategies with model architecture and scale, rather than relying on a one-size-fits-all approach.
