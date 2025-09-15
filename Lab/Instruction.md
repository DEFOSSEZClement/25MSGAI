# MSGAI lab innstructions

## Course Overview
This course covers the fundamentals and applications of generative AI.

The lab consists of three parts, each with two group tutorial sessions to be given by the TAs and one individual homework to be solved by students.

- Part 1: [Fine-tuning Generative Models](#part-1-diffusion)
    - Tutorial 1A - Fine-tuning diffusion
    - Tutorial 1B - Sampling of diffusion 
    - Homework 1 
- Part 2: [Benchmarking Generative Models](#part-2-large-language-models)
    - Tutorial 2A - Language transformer models
    - Tutorial 2B - Few-Shot (+Sampling) / Fine-tuning of LLM
    - Homework 2 
- Part 3: Modeling of Generative Models
    - Tutorial 3A - Solving DTMC
    - Tutorial 3B - Solving CTMC
    - Homework 3 
    

## Part 1: Diffusion
We will **NOT** provide any technical assistance during the lab, please refer to the internet or other students for questions regarding your setup.

### Prerequisites

You need to have access to a computer able to load the different models we are going to use. All the code will be run on your personal computer.

Alternatively you can use [colab](https://colab.google.com) to run the different notebooks, but be aware of the limitations implied.

### Technical requirements

The code will be written in **Python** using **Pytorch** for the experiments. The lab is designed to run on Linux or a similar platform. We provide the environment required in the file [lab1to4_requirements-env-cuda](Lab1to4_requirements-env-cuda.txt).

````bash
python -m venv .venv
source .venv/bin/activate          # Windows: .\.venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r Lab/Lab1to4_requirements-env-cuda.txt
````

After installing the requirements, run the following command to set up nbstripout (this prevents notebook outputs from being committed to git):

````bash
nbstripout --install
````

Note: You must have access to a CUDA compatible GPU, as the code will not run on CPU only. Make sure you have installed and correctly set up CUDA 12.4 first.
We will share a notebook at the beginning of each lab, along with the information about the dataset or additional material we'll be using.

## Part 2: Large Language Models
We will **NOT** provide any technical assistance during the lab, please refer to the internet or other students for questions regarding your setup.

### Prerequisites

You need to have access to a computer able to load the different models we are going to use. All the code will be run on your personal computer.

Alternatively you can use [colab](https://colab.google.com) to run the different notebooks, but be aware of the limitations implied.

> This Lab and HW will make use of a small LLM, which benefits greatly from a GPU. The GPUs from Google Collab should be sufficient for this
model.


> ⚠️ Before attending the lab, make sure you have run the first set of cells for that lab, since you may need to download the models and configure huggingface access.

## Hugging Face credentials and pre-downloading models

Follow these steps before the session to configure your Huggingface API token.

- Copy the provided `.env.template` at the repo root to a file named `.env` and fill in your token:
- The notebooks will call `load_dotenv()` and read the `HUGGINGFACE_API_KEY` environment variable. Do not hardcode tokens inside notebooks.
- Ensure `.env` is in `.gitignore` (the repo already includes an entry for `.env`) so you don't accidentally push secrets.


### Submitting the Homework to Ilias
**N.B.** To submit this homework, you must make sure all outputs in the notebooks are present, and that the notebooks are
correctly formatted.

We do recommend using `git` to commit your work, to be able to revert breaking changes. 

