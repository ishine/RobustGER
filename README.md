# Large Language Models are Efficient Learners of Noise-Robust Speech Recognition

[[Paper]](https://openreview.net/pdf?id=ceATjGPTUD) [[Data]](https://huggingface.co/datasets/PeacefulData/Robust-HyPoradise) [[Model]](https://huggingface.co/PeacefulData/RobustGER)

<p align="center">  <img src="https://github.com/YUCHEN005/RobustGER/blob/master/tutorials/robust_ger.png" height ="300"> </p>

This work extends the latest ASR generative error correction (GER) [benchmark](https://openreview.net/pdf?id=cAjZ3tMye6) to noise-robust ASR with a Robust HyPoradise dataset, and it proposes a language-space denoising approach for GER that has achieved a new breakthrough.

## Conda Environment Configuration

Our code is built based on [lit-gpt](https://github.com/Lightning-AI/lit-gpt), please refer to [official tutorial](https://github.com/Lightning-AI/lit-gpt#setup) to build a conda environment. Then, please install the required packages using following command:
```bash
pip install -r requirements.txt
```

## Code

- Model code: `lit_gpt/robust_ger.py`;
- Training script: `finetune.sh`;
- Inference script: `infer.sh`;

To run the training or inference script, you need to enter the scripts (including `.sh` and the called `.py` files) and modify all the absolute paths of data, model, and experiment directory to be your own (*Hint:* search for "~/RobustGER"). Then, directly run the `.sh` script using `bash` command.

## Models

- For LLMs, please refer to [tutorial](https://github.com/YUCHEN005/RobustGER/tree/master/tutorials) for configuration steps, which support many mainstream LLMs like [LLaMA-2](https://github.com/YUCHEN005/RobustGER/blob/master/tutorials/download_llama_2.md);
- For well-trained adapter checkpoints, please refer to our [HuggingFace repo](https://huggingface.co/PeacefulData/RobustGER).

## Dataset

We have released our Robust HyPoradise dataset at [HuggingFace](https://huggingface.co/datasets/PeacefulData/Robust-HyPoradise).

## References
```bib
@inproceedings{hu2024large,
  title={Large Language Models are Efficient Learners of Noise-Robust Speech Recognition},
  author={Hu, Yuchen and Chen, Chen and Yang, Chao-Han Huck and Li, Ruizhe and Zhang, Chao and Chen, Pin-Yu and Chng, Eng Siong},
  booktitle={International Conference on Learning Representations},
  year={2024}
}

@inproceedings{chen2023hyporadise,
  title={HyPoradise: An Open Baseline for Generative Speech Recognition with Large Language Models},
  author={Chen, Chen and Hu, Yuchen and Yang, Chao-Han Huck and Siniscalchi, Sabato Marco and Chen, Pin-Yu and Chng, Eng Siong},
  booktitle={Advances in Neural Information Processing Systems},
  year={2023}
}
```
