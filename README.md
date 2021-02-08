# HAKE-Action-Torch

**Seven-in-One**: CVPR'18 (Part States), CVPR'19 (interactiveness), CVPR'20 (PaStaNet, Dj-RN, SymNet), NeurIPS'20 (IDN), TPAMI(Extended TIN).

Work in progress.

<p align='center'>
    <img src="misc/hake_demo.jpg", height="300">
</p>

HAKE-Action-Torch (**PyTorch**) is a project to open the SOTA action understanding studies based on our project: [Human Activity Knowledge Engine](http://hake-mvig.cn/home/). It includes SOTA models and their corresponding HAKE-enhanced versions based on our six papers (CVPR'18/19/20, NeurIPS'20). The TensorFlow version of HAKE-Action is [here](https://github.com/DirtyHarryLYL/HAKE-Action).

Currently, it is manintained by [Yong-Lu Li](https://dirtyharrylyl.github.io/), Xinpeng Liu and Zhanke Zhou, Hongwei Fan.

#### **News**: (2021.2.7) Upgraded [HAKE-Activity2Vec](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/Activity2Vec) is released! Images/Videos --> human box + ID + skeleton + part states + action + representation. An offical demo is coming soon.
<p align='center'>
    <img src="https://github.com/DirtyHarryLYL/HAKE-Action-Torch/blob/Activity2Vec/demo/a2v-demo.gif", height="400">
</p>

(2021.1.15) Our extended version of [TIN (Transferable Interactiveness Network)](https://arxiv.org/abs/2101.10292) is accepted by TPAMI!

(2020.10.27) The code of [IDN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/IDN-(Integrating-Decomposing-Network)) ([Paper](https://arxiv.org/abs/2010.16219)) in NeurIPS'20 is released!

## Project
```Branches
HAKE-Action-Torch
  ├──Master Branch                          # Unified pipeline; CVPR'18/20, PaStanet and Part States.
  ├──IDN-(Integrating-Decomposing-Network)  # NeurIPS'20, HOI Analysis: Integrating and Decomposing Human-Object Interaction.
  ├──DJ-RN-Torch                            # CVPR'20, Detailed 2D-3D Joint Representation for Human-Object Interaction.
  ├──TIN-Torch                              # CVPR'19, Transferable Interactiveness Knowledge for Human-Object Interaction Detection.
  └──SymNet-Torch                           # CVPR'20, Symmetry and Group in Attribute-Object Compositions.
```

## Papers
- [Extended TIN](https://arxiv.org/abs/2101.10292) (TPAMI'21)
- [IDN](https://arxiv.org/pdf/2010.16219.pdf) (NeurIPS'20)
- [PaStaNet](https://arxiv.org/pdf/2004.00945.pdf) (CVPR'20)
- [DJ-RN](https://arxiv.org/pdf/2004.08154.pdf) (CVPR'20)
- [SymNet](https://arxiv.org/pdf/2004.00587.pdf) (CVPR'20)
- [TIN](https://arxiv.org/pdf/1811.08264.pdf) (CVPR'19)
- [Part States](http://ai.ucsd.edu/~haosu/papers/cvpr18_partstate.pdf) (CVPR'18)

## Model Zoo
Coming soon.

### Results on HICO-DET with different object detections.
|Method| Detector |HAKE| Full(def) | Rare(def) | None-Rare(def)| Full(ko) | Rare(ko) | None-Rare(ko) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|[TIN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/TIN-Torch)| COCO |-| 17.54	|13.80	|18.65|	19.75|	15.70|	20.96|
|[DJ-RN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/DJ-RN-Torch)| COCO |-| 21.34|18.53|22.18|23.69|20.64|24.60|
|[IDN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/IDN-(Integrating-Decomposing-Network))|COCO|-|23.36|22.47|23.63|26.43|25.01|26.85|
|[IDN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/IDN-(Integrating-Decomposing-Network))|COCO+HICO-DET|-|26.29|22.61|27.39|28.24|24.47|29.37|
|[TIN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/TIN-Torch)| GT Pairs |-|34.26|22.90 |37.65|-|-|-|
|[IDN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/IDN-(Integrating-Decomposing-Network))|GT Pairs|-|43.98|40.27|45.09|-|-|-|

### Results on V-COCO. 
As VCOCO is built on COCO, thus finetuning detector on VCOCO basically contributes marhinally to performance.
|Method | HAKE | AP(role) |
|:---:|:---:|:---:|
|[TIN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/TIN-Torch)|-|47.8|
|[IDN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/IDN-(Integrating-Decomposing-Network))|-|53.3|

### Results on [Ambiguous-HOI](https://github.com/DirtyHarryLYL/DJ-RN).
|Method| mAP |
|:---:|:---:|
|[TIN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/TIN-Torch)| 8.22 |
|[DJ-RN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/DJ-RN-Torch)| 10.37 |


## Modules

### 1. Unified Model
Coming soon.

### 2. HAKE Only (CVPR'20)
Coming soon.

### 3. Activity2Vec (CVPR'20)
The independent Torch version is in: [Activity2Vec (A2V)](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/Activity2Vec).

### 4. IDN (NeurIPS'20)
The independent Torch version is in: [IDN](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/IDN-(Integrating-Decomposing-Network)).

### 5. DJ-RN (CVPR'20)
The independent Torch version is in: [DJ-RN-Torch](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/DJ-RN-Torch)

### 6. TIN (CVPR'19)
The independent Torch version is in: [TIN-Torch](https://github.com/DirtyHarryLYL/HAKE-Action-Torch/tree/TIN-Torch)

### 7. SymNet (CVPR'20)
Coming soon.

## Citation
If you find our works useful, please consider citing:
```
---IDN:
@inproceedings{li2020hoi,
  title={HOI Analysis: Integrating and Decomposing Human-Object Interaction},
  author={Li, Yong-Lu and Liu, Xinpeng and Wu, Xiaoqian and Li, Yizhuo and Lu, Cewu},
  booktitle={NeurIPS},
  year={2020}
}
---HAKE:
@inproceedings{li2020pastanet,
  title={PaStaNet: Toward Human Activity Knowledge Engine},
  author={Li, Yong-Lu and Xu, Liang and Liu, Xinpeng and Huang, Xijie and Xu, Yue and Wang, Shiyi and Fang, Hao-Shu and Ma, Ze and Chen, Mingyang and Lu, Cewu},
  booktitle={CVPR},
  year={2020}
}
@inproceedings{lu2018beyond,
  title={Beyond holistic object recognition: Enriching image understanding with part states},
  author={Lu, Cewu and Su, Hao and Li, Yonglu and Lu, Yongyi and Yi, Li and Tang, Chi-Keung and Guibas, Leonidas J},
  booktitle={CVPR},
  year={2018}
}
---DJ-RN
@inproceedings{li2020detailed,
  title={Detailed 2D-3D Joint Representation for Human-Object Interaction},
  author={Li, Yong-Lu and Liu, Xinpeng and Lu, Han and Wang, Shiyi and Liu, Junqi and Li, Jiefeng and Lu, Cewu},
  booktitle={CVPR},
  year={2020}
}
---TIN
@inproceedings{li2019transferable,
  title={Transferable Interactiveness Knowledge for Human-Object Interaction Detection},
  author={Li, Yong-Lu and Zhou, Siyuan and Huang, Xijie and Xu, Liang and Ma, Ze and Fang, Hao-Shu and Wang, Yanfeng and Lu, Cewu},
  booktitle={CVPR},
  year={2019}
}
---SymNet
@inproceedings{li2020symmetry,
  title={Symmetry and Group in Attribute-Object Compositions},
  author={Li, Yong-Lu and Xu, Yue and Mao, Xiaohan and Lu, Cewu},
  booktitle={CVPR},
  year={2020}
}
```

## TODO
- [ ] TIN-based element analysis
- [ ] Refined Activity2Vec
- [ ] Extended DJ-RN
- [ ] SymNet in Torch
- [ ] HAKE only model

## [HAKE](http://hake-mvig.cn/home/)
**HAKE**[[website]](http://hake-mvig.cn/home/) is a new large-scale knowledge base and engine for human activity understanding. HAKE provides elaborate and abundant **body part state** labels for active human instances in a large scale of images and videos. With HAKE, we boost the action understanding performance on widely-used human activity benchmarks. Now we are still enlarging and enriching it, and looking forward to working with outstanding researchers around the world on its applications and further improvements. If you have any pieces of advice or interests, please feel free to contact [Yong-Lu Li](https://dirtyharrylyl.github.io/) (yonglu_li@sjtu.edu.cn).

If you get any problems or if you find any bugs, don't hesitate to comment on GitHub or make a pull request! 

HAKE-Action-Torch is freely available for free non-commercial use, and may be redistributed under these conditions. For commercial queries, please drop an e-mail. We will send the detail agreement to you.
