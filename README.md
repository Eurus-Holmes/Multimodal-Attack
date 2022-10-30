# Multimodal-Attack

From https://github.com/adversarial-for-goodness/Co-Attack

```
conda create -n coAttack python=3.7
conda activate coAttack
pip install -r requirements.txt
```

## Datasets

Flickr30k: https://drive.google.com/drive/folders/19tKLlNvBN3mbXHDYZzCkQ3I2jNxjjHFT?usp=sharing

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
