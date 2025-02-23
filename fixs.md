## fix some libraries to proper version
!pip install scipy==1.13.0
!pip install scikit-learn==1.3.1
!pip install matplotlib==3.8.0

## rouge score library version does not have rouge_score.__version__ attribute
`print("Rouge Score version:", rouge_score.__version__)`

import importlib.metadata

try:
    rouge_score_version = importlib.metadata.version('rouge-score')
    print("Rouge Score version:", rouge_score_version)
except importlib.metadata.PackageNotFoundError:
    print("rouge-score package is not installed.")

## max_steps=500,
fix max steps to 500

## change model repo to my own
peft_model.push_to_hub("fujiazhiyu/phi-2-dialogsum-finetuned")
tokenizer.push_to_hub("fujiazhiyu/phi-2-dialogsum-finetuned")

## change model path
/kaggle/working/peft-dialogue-summary-training/final-checkpoint/checkpoint-500
