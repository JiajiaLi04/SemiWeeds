# Performance Evaluation of Semi-supervised Learning Frameworks for Multi-Class Weed Detection
Performance Evaluation of Semi-supervised Learning Frameworks for Multi-Class Weed Detection

More instructions coming soon...

## Installation
- Follow the installation instructions of INSTALL.md

## Training and testing commands
#### Train supervised baseline. For example, using 20% of labeled data
```
python train_net.py \
       --num-gpus 2 \
       --config configs/FCOS/fcos_R_50_ut2_sup20_run0.yaml \
        SOLVER.IMG_PER_BATCH_LABEL 4 SOLVER.IMG_PER_BATCH_UNLABEL 4 SOLVER.IMS_PER_BATCH 4 \
        OUTPUT_DIR ./xx/ \
        TEST.EVAL_PERIOD 2000 \
        SEED 1 \
        SEMISUPNET.Trainer baseline
```

#### Train semi-supervised. For example, using 20% of labeled data + 80% unlabeled data
```
python train_net.py \
      --num-gpus 2 \
      --config configs/FCOS/fcos_R_50_ut2_sup20_run0.yaml \
       SOLVER.IMG_PER_BATCH_LABEL 4 SOLVER.IMG_PER_BATCH_UNLABEL 4 SOLVER.IMS_PER_BATCH 4 \
       OUTPUT_DIR ./xx/ \
       TEST.EVAL_PERIOD 2000 \
       SEED 1 
```
#### Train semi-supervised. For example, using 20% of labeled data + 80% unlabeled data
```
python train_net.py \
        --eval-only \
	--num-gpus 2 \
	--config configs/FCOS/fcos_R_50_ut2_sup20_run0.yaml \
	SOLVER.IMG_PER_BATCH_LABEL 4 SOLVER.IMG_PER_BATCH_UNLABEL 4 SOLVER.IMS_PER_BATCH 4 \
	MODEL.WEIGHTS ./model_final.pth \
	OUTPUT_DIR ./xx/ \
        SEMISUPNET.Trainer baseline \
	SEED 1 
```

## Citation

Is this repository helpful? 😊  

Please consider citing our paper. 👇👇👇
```
@article{li2024performance,
  title={Performance evaluation of semi-supervised learning frameworks for multi-class weed detection},
  author={Li, Jiajia and Chen, Dong and Yin, Xunyuan and Li, Zhaojian},
  journal={Frontiers in Plant Science},
  volume={15},
  pages={1396568},
  year={2024},
  publisher={Frontiers Media SA}
}
```

```
@article{li2023label,
  title={Label-efficient learning in agriculture: A comprehensive review},
  author={Li, Jiajia and Chen, Dong and Qi, Xinda and Li, Zhaojian and Huang, Yanbo and Morris, Daniel and Tan, Xiaobo},
  journal={Computers and Electronics in Agriculture},
  volume={215},
  pages={108412},
  year={2023},
  publisher={Elsevier}
}
```

