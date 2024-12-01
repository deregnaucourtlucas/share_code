# ECOLAF


## DESCRIPTION

This package offers a user-friendly toolkit to build an adaptive multimodal late fusion pipeline (*ECOLAF*) based on Dempster-Shafer Theory from multiple single-modality neural networks.
The proposed pipeline can be used for semantic segmentation and classification tasks.

Mettre les équations et des exemples plus visuels pourrait pimper la description !!!


## USAGE
Firstly, a single-modality neural network need to be defined for each modality. Please make sure that each neural network has a *forward* method. If the dataset you are working with has *K* classes, please make sure that your models output *K+1* values to fit the Dempster-Shafer framework. 

Then you can build an *ECOLAF* pipeline as follows: `MyModel = ECOLAF(list_of_single_modality_networks, num_classes)`.

Given a list of multimodal images, the inference can be done as follows: `output = MyModel(list_of_images, **kwargs)`.

An example is provided in `test/test_code.py`.


## CITATIONS

If you use ECoLaF, please cite the following work:

```
@InProceedings{deregnaucourt_2025_WACV,
    author    = {Deregnaucourt, Lucas and Laghmara, Hind and Lechervy, Alexis and Ainouz, Samia},
    title     = {An Conglict-guided Evidential Fusion for Multimodal Semantic Segmentation},
    booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
    month     = {February},
    year      = {2025},
}
```
