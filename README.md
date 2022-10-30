# Multimodal-Attack

From https://github.com/adversarial-for-goodness/Co-Attack

```
conda create -n coAttack python=3.7
conda activate coAttack
pip install -r requirements.txt
```

## Datasets

Flickr30k: https://drive.google.com/drive/folders/19tKLlNvBN3mbXHDYZzCkQ3I2jNxjjHFT?usp=sharing


## Evaluation
|Adv|Instruction|
|---|---|
|0|No Attack|
|1|Attack Text|
|2|Attack Image|
|3|Attack Both (vanilla)|
|4|Co-Attack|


## Attack Clip

```
python RetrievalCLIPEval.py --adv 4 --gpu 0 --image_encoder ViT-B/16 --cls \
--config configs/Retrieval_flickr.yaml \
--output_dir output/Retrieval_flickr 
```

## Attack ALBEF

```
python RetrievalEval.py --adv 4 --gpu 0 --cls \
--config configs/Retrieval_flickr.yaml \
--output_dir output/Retrieval_flickr \
--checkpoint /content/Co-Attack/flickr30k.pth
```

## Experiments

Colab: https://colab.research.google.com/drive/1ohH4Mo4b15UcAlXUP7_Ta3Dxg_2XhX14?usp=sharing
