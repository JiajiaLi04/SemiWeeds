# Performance Evaluation of Semi-supervised Learning Frameworks for Multi-Class Weed Detection
Performance Evaluation of Semi-supervised Learning Frameworks for Multi-Class Weed Detection

More instructions coming soon...

## Installation
- Follow the installation instructions of INSTALL.md

## Training commands
### Train supervised baseline. For example, using 20% of labeled data
```
python train_net.py \
       --num-gpus 2 \
       --config configs/FCOS/coco-customized/fcos_R_50_ut2_sup20_run0.yaml \
        SOLVER.IMG_PER_BATCH_LABEL 4 SOLVER.IMG_PER_BATCH_UNLABEL 4 SOLVER.IMS_PER_BATCH 4 \
        OUTPUT_DIR ./output/2_baseline_weeds_fcos/1_baseline_20/ \
        TEST.EVAL_PERIOD 2000 \
        SEED 1 \
        SEMISUPNET.Trainer baseline
```

### Train semi-supervised. For example, using 20% of labeled data + 80% unlabeled data
```
python train_net.py \
      --num-gpus 2 \
      --config configs/FCOS/coco-customized/fcos_R_50_ut2_sup20_run0.yaml \
       SOLVER.IMG_PER_BATCH_LABEL 4 SOLVER.IMG_PER_BATCH_UNLABEL 4 SOLVER.IMS_PER_BATCH 4 \
       OUTPUT_DIR ./output/2_weeds_fcos_2/1_weed_detection_20/ \
       TEST.EVAL_PERIOD 2000 \
       SEED 1 
```


## Citation

Is this repository helpful? 😊  

Please consider citing our paper. 👇👇👇


