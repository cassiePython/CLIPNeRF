# ColorNerf
Editing color of a single nerf model.

This project is built upon a [PyTorch implementation](https://github.com/yenchenlin/nerf-pytorch).


## Dataset and Nerf Models

Download `nerf_synthetic.zip` from [here](https://drive.google.com/drive/folders/128yBriW1IG_3NJ5Rp7APSTZsJqdJdfc1). Then unzip the file into the directiory
'/data'.

Download pretrained Nerf models from [here](https://drive.google.com/drive/folders/1jIr8dkvefrQmv737fFm2isiT6tqpbTbv). Then place it into the checkpoint directory.

## Run

To edit color of a pre-trained lego:

```
python run_nerf_clip.py --config configs/lego.txt --use_clip --w_clip 1.0 
```

|  Parameter  | Discription  |
|  ----  | ----  |
| --description  | Text prompt |
| --use_clip  | Use CLIP loss to finetune Nerf |
| --w_clip | Weight for CLIP loss |
| --use_alpha | Whether finetune alpha layers |
| --use_feature | Whether finetune feature layers |
| --use_view | Whether finetune view layers |
| --sample_scale | Patch size (the larger, the better, you can set a max value according to your GPU |

You can try different parameters by yourself to achieve different editing results. You will find results in the logs directory.

Note: For color green, you can directly use the above order. But please try other parameters to obtain a desired color. For example, please add use_alpha, use_feature, and use_view to change the color to red.
Sample_scale is also a critical factor to influence the result. 

## Results


<center>

![](https://github.com/cassiePython/ColorNerf/blob/main/results/1-1.gif)![](https://github.com/cassiePython/ColorNerf/blob/main/results/1-2.gif)![](https://github.com/cassiePython/ColorNerf/blob/main/results/1-3.gif)![](https://github.com/cassiePython/ColorNerf/blob/main/results/1-4.gif)
</center>

<center>

![](https://github.com/cassiePython/ColorNerf/blob/main/results/2-1.gif)![](https://github.com/cassiePython/ColorNerf/blob/main/results/2-2.gif)![](https://github.com/cassiePython/ColorNerf/blob/main/results/2-3.gif)![](https://github.com/cassiePython/ColorNerf/blob/main/results/2-4.gif)
</center>
