# MSCOCO-Flikcr30K_FG
**Rethinking Benchmarks for Cross-modal Image-text Retrieval**  
Weijing Chen, Linli Yao and Qin Jin  
The 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, Taipei, July 2023.  
[ [arXiv preprint](https://arxiv.org/abs/2304.10824) | [Read the paper](https://doi.org/10.1145/3539618.3591758) | [data sources](https://github.com/cwj1412/MSCOCO-Flikcr30K_FG)]

## Background
With the prevalence of large scale multimodal pretraining models, several state-of-the-art models (e.g. X-VLM) have achieved near perfect performance on widely-used image-text retrieval benchmarks, i.e. MSCOCO-Test-5K and Flickr30K-Test-1K. In this paper, we review the two common benchmarks and observe that they are insufficient to assess the true capability of models on fine-grained cross-modal semantic matching. The reason is that a large amount of images and texts in the benchmarks are coarse-grained.  

<img src="https://github.com/cwj1412/MSCOCO-Flikcr30K_FG/blob/master/current_issues.jpg" alt="Illustration of ’coarse-grained images and texts’ issues in current benchmarks">

Based on the observation, we renovate the coarse-grained images and texts in the old benchmarks and establish the improved benchmarks called ***MSCOCO-FG*** and ***Flickr30K-FG***. Specifically, on the image side, we enlarge the original image pool by adopting more similar images. On the text side, we propose a novel semi-automatic renovation approach to refine coarse-grained sentences into finer-grained ones with little human effort. 

<img src="https://github.com/cwj1412/MSCOCO-Flikcr30K_FG/blob/master/new_image_examples.jpg" width="48%" alt="Examples of the old text and improved text for the same image" align="middle"> <img src="https://github.com/cwj1412/MSCOCO-Flikcr30K_FG/blob/master/new_text_examples.jpg" width="48%" alt="Illustration of the original and our new retrieval image pools on MSCOCO and Flickr30K" align="left">


## Download
### Images
We collect similar images for each target image in MSCOCO-Test-5K/Flickr30K-Test-1K from *2017 Unlabeled images* released by [COCO](https://cocodataset.org/). For easy use, we have already assembled all similar image sets and removed duplicate images. According to copyright restrictions, We only provide the list of filenames for images in new image pools.  

See `Images` for more details. If you wish to evaluate your model on our new benchmarks, you can turn to the offical website of [COCO](https://cocodataset.org/) and [Flickr30K](http://shannon.cs.illinois.edu/DenotationGraph/) to download the corresponding images.

### Text Annotations
We provide new fine-grained text annotations for images in of MSCOCO-Test-5K/Flickr30K-Test-1K.  
See `Annotations` for more details.

## Citation
If you find this code useful for your research, please consider citing:
```
@inproceedings{chen2023rethinking,
  title = {Rethinking Benchmarks for Cross-modal Image-text Retrieval},
  author = {Chen, Weijing and Yao, Linli and Qin, Jin},
  booktitle = {Proceedings of the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval (SIGIR '23)},
  year = {2023}
}
```
