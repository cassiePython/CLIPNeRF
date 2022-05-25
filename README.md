# CVPR2022: CLIP-NeRF: Text-and-Image Driven Manipulation of Neural Radiance Fields

<img src='https://cassiepython.github.io/clipnerf/images/teaser.gif'/>

### [Project Page](https://cassiepython.github.io/clipnerf/) | [Paper (ArXiv)](https://arxiv.org/abs/2112.05139)


[Can Wang](https://cassiepython.github.io/)<sup>1</sup>,
[Menglei Chai](https://mlchai.com/)<sup>2</sup>,
[Mingming He](http://mingminghe.com/)<sup>3</sup>,
[Dongdong Chen](http://www.dongdongchen.bid/)<sup>4</sup>,
[Jing Liao](https://liaojing.github.io/html/)<sup>1</sup> <br>
<sup>1</sup>City University of Hong Kong, <sup>2</sup>Creative Vision, Snap Inc., <sup>3</sup>USC Institute for Creative Technologies, <sup>4</sup>Microsoft Cloud AI


## Abstract
<img src='imgs/framework.png'/>
We present CLIP-NeRF, a multi-modal 3D object manipulation method for neural radiance fields (NeRF). By leveraging the joint language-image embedding space of the recent Contrastive Language-Image Pre-Training (CLIP) model, we propose a unified framework that allows manipulating NeRF in a user-friendly way, using either a short text prompt or an exemplar image. Specifically, to combine the novel view synthesis capability of NeRF and the controllable manipulation ability of latent representations from generative models, we introduce a disentangled conditional NeRF architecture that allows individual control over both shape and appearance. This is achieved by performing the shape conditioning via applying a learned deformation field to the positional encoding and deferring color conditioning to the volumetric rendering stage. To bridge this disentangled latent representation to the CLIP embedding, we design two code mappers that take a CLIP embedding as input and update the latent codes to reflect the targeted editing. The mappers are trained with a CLIP-based matching loss to ensure the manipulation accuracy. Furthermore, we propose an inverse optimization method that accurately projects an input image to the latent codes for manipulation to enable editing on real images. We evaluate our approach by extensive experiments on a variety of text prompts and exemplar images and also provide an intuitive interface for interactive editing.


## Supplyment

I add the code of the single NeRF color editing in the supplyment directory. 
