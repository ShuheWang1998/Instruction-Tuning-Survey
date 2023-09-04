# Instruction-Tuning-Survey

This repository contains resources referenced in the paper [Instruction Tuning for Large Language Models: A Survey](https://arxiv.org/abs/2308.10792). 

If you find this repository helpful, please cite the following:
```latex
@article{zhang2023instruction,
  title={Instruction Tuning for Large Language Models: A Survey},
  author={Zhang, Shengyu and Dong, Linfeng and Li, Xiaoya and Zhang, Sen and Sun, Xiaofei and Wang, Shuhe and Li, Jiwei and Hu, Runyi and Zhang, Tianwei and Wu, Fei and others},
  journal={arXiv preprint arXiv:2308.10792},
  year={2023}
}
```

## Table of Contents 
* [Overview](#Overview)
* [Natural Language Instruction Tuning](Instruction-Tuned-LLMs)
  * [Datasets](#Datasets)
  * [Models](#Models)
* [Multi-modality Instruction Tuning](Multi-modality-Instruction-Tuning)
  * [Datasets](#Datasets)
  * [Models](#Models)
* [Domain-specific Instruction Tuning](Domain-specific-Instruction-Tuning)
  

## Overview

Instruction tuning (IT) refers to the process of further training large language models (LLMs) on a dataset consisting 
of `(instruction, output)` pairs
 in a supervised fashion, 
which bridges the gap between the next-word prediction objective of LLMs and the users' objective of having LLMs adhere 
to human instructions. The general pipeline of instruction tuning is shown in the following: 
![project](./assets/method_overview.png)

In the [paper](https://arxiv.org/abs/2308.10792), we make a systematic review of the literature, including the general methodology of IT, 
the construction of IT datasets, the training of IT models, 
and applications to different modalities, domains and application, along with analysis on aspects that influence the outcome of IT (e.g., generation of instruction outputs, size of the instruction dataset, etc). We also 
review the potential pitfalls of IT along with criticism against it, along with efforts
pointing out current deficiencies of existing strategies and suggest some avenues for fruitful research.
The typology of the paper is as follows: 



## Natural Language Instruction Tuning

### Datasets 

<table>
    <tr>
        <th>头部1</th>
        <th>头部2</th>
        <th>头部3</th>
    </tr>
    <tr>
        <td rowspan="2">这是跨两行的内容</td>
        <td>内容2.1</td>
        <td>内容3.1</td>
    </tr>
    <tr>
        <td>内容2.2</td>
        <td>内容3.2</td>
    </tr>
    <tr>
        <td>内容1.3</td>
        <td>内容2.3</td>
        <td>内容3.3</td>
    </tr>
</table>


<table>


</table>

### Models

<table>
    <tr>
        <th>Instruction tuned LLMs</th>
        <th># Params</th> 
        <th>Paper</th>
        <th>Project</th>
        <th>Base Model</th>
        <th colspan="3">Instruction Train Set</th>
    </tr>
    <tr>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th>Self-build</th>
        <th>Dataset Name</th>
        <th>Size</th>
    </tr>
    <tr>
        <td> Instruct-GPT</td>
        <td>176B</td>
        <td>[paper]()</td>
        <td>GPT-3</td>
        <td>Yes</td>
        <td>-</td>
        <td>-</td>
        <td>-</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td>Self-build</td>
        <td>Dataset Name</td>
        <td>Size</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td>Self-build</td>
        <td>Dataset Name</td>
        <td>Size</td>
    </tr>
</table>



| BLOOMZ | 176B   |  [paper]() |    [project](https://huggingface.co/bigscience/bloomz)  | BLOOM   | No     | xP3       | -  | 
| FLAN-T5 | 11B   |  [paper]()   |     [project](https://huggingface.co/google/flan-t5-xxl)    | T5      | No   | FLAN 2021 | - | 
| Alpaca | 7B     |  [paper]()  |    [project](https://github.com/tatsu-lab/stanford_alpaca)  | LLaMA   | Yes       | -  | 52K  | 
| Vicuna | 13B    |  [paper]()  |    [project](https://github.com/lm-sys/FastChat)   | LLaMA   | Yes       | -  | 70K  | 
| GPT-4-LLM | 7B    |  [paper]()   |     [project](https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM)  | LLaMA   | Yes       | -  | 52K | 
| Claude | -     |  [paper]()  |     -     | -       | Yes       | -  | - | 
| WizardLM | 7B   |  [paper]()   |    [project](https://github.com/nlpxucan/WizardLM)   | LLaMA   | Yes       | Evol-Instruct | 70K  | 
| ChatGLM2 | 6B   |  [paper]()   |    [project](https://github.com/THUDM/ChatGLM2-6B)   | GLM     | Yes       | -  | 1.1 Tokens | 
| LIMA | 65B   | [paper]() ｜  -  | LLaMA   | Yes       | -  | 1K  | 
| OPT-IML | 175B |  [paper]()  |    [project](https://huggingface.co/facebook/opt-iml-30b)   | OPT     | No | -  | - | 
| Dolly 2.0 | 12B  |  [paper]()  |    [project](https://github.com/databrickslabs/dolly)    | Pythia  | No  | -  | 15K  | 
| Falcon-Instruct | 40B  |  [paper]()  |   [project](https://huggingface.co/tiiuae/falcon-40b-instruct)    | Falcon  | No  | -  | - | 
| Guanaco | 7B   |  [paper]()  |    [project](https://huggingface.co/JosephusCheung/Guanaco)    | LLaMA   | Yes       | -  | 586K | 
| Minotaur | 15B   |  [paper]()   |    [project](https://huggingface.co/openaccess-ai-collective/minotaur-15b)  | Starcoder Plus | No   | -  | -  | 
| Nous-Hermes | 13B  |  [paper]()   |    [project](https://huggingface.co/NousResearch/Nous-Hermes-13b)   | LLaMA   | No   | -  | 300K+ | 
| TÜLU  | 6.7B  |  [paper]()  |   [project](https://github.com/allenai/open-instruct)   | OPT     | No     | Mixed     | - | 
| YuLan-Chat | 13B  |  [paper]()  |    [project](https://github.com/RUC-GSAI/YuLan-Chat)    | LLaMA   | Yes     | -  | 250K  | 
| MOSS  | 16B   |  [paper]()  |    [project](https://github.com/OpenLMLab/MOSS)   | -  | Yes | -  | -  | 
| Airoboros  | 13B   |  [paper]() |    [project](https://github.com/jondurbin/airoboros)    | LLaMA   | Yes       | -  | -  | 
| UltraLM | 13B    |  [paper]() |    [project](https://github.com/thunlp/UltraChat)   | LLaMA   | Yes       | -  | - | 

## Multi-modality Instruction Tuning

### Datasets

### Models

## Domain-specific Instruction Tuning


