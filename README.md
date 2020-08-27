# [SIIM-ISIC Melanoma Classification](https://www.kaggle.com/c/siim-isic-melanoma-classification) 

### Identify melanoma in lesion images

## Team Members

- [Pratik Bedre](https://www.kaggle.com/cdeotte)
- [Gyanendra Das](https://github.com/Luckygyana)
- [Saksham Aggarwal](https://github.com/saksham20aggarwal)

# Our Approach



We used **EfficientNet [B0-B6]**, **Resnest**,**Resnext**, with Sizes **192x192** **256x256** **384x384** **512x512** **768x768** **384x512**[HxW]

## Summary

#### What Worked for Us

- Heavy TTA (X20)
- Cutmix
- Coarse dropout
- SWA(Stochastic Weight Averaging)
- Loss-Label Smoothing, BCE
- Optimizers - AdamW, Adam
- 2018, 2020 and malignant datasets
- 5 checkpoints' prediction averaging(stabalised our model's predictions)
- some models were trained with different height width ratios

#### What didn't Work for Us

- Loss functions-Focal loss, dice loss
- Optimizer- Ranger
- Hair removal/addition
- Pseudo labelling
- 2019 dataset
- Preprocessing techniques from [Aptos Competition](https://www.kaggle.com/c/aptos2019-blindness-detection)
- Progressive learning

### Ensembling techniques

- Weighted average
- Power Average
- Minmax ensemble(didn't help)<br>


## Our final Submission
15+ pytorch model (with context) and 15+ tf models (without context) - 0.9627 (public LB) 0.9470 (private LB) 0.9618 (CV)
It could have achieved us 6th rank on the private leader board of the competition.
