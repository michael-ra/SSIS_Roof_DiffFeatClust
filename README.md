
# Semi-Supervised Roof Segmentation
### Solar Potential Analysis using Semi-Supervised Image Segmentation based on Differentiable Feature Clustering

This is our take on semi-supervised image segmentation based on a paper on unsupervised image segmentation
by Kanezaki and Tanak [[1]](#1). We improved on their model and adjusted it for our needs in roof segmentation.
Our aim was to segment roofs to presegment them, before humans will fine-tune the segmentation. 

[The paper to this project is avaliable in this Github Repo as well.](https://github.com/michael-ra/SSIS_Roof_DiffFeatClust/blob/main/SSIS_Roof_DiffFeatClust.pdf)

#### Short summary of the network
- Convolutional model
- Average Pooling inside the network
- Skip-Connection around a part of the 'main' network
- Different losses for (supervised) pretraining and unsupervised training
- Enable pretraining on roof masks to help the network segment roofs from the rest
- Everything implemented in Tensorflow

Also, we have done data-cleaning, checking and used a data-centric approach to select high quality and relevant data (as especially our masks were not that great in every picture, sometimes only filling 1% of the image i.e.).
We also compared all different types and gradual improvements we have made to suit the model to our usecase in comparison to the baseline model found in [the original paper](#1).
In the end, we also compared our Deeplearning networks to a more traditional machine learning approach (k-means) and also a basic method for segmentation based on greyscaling the image.
## Authors

- [Michael Ramich](https://github.com/michael-ra)
- [Magnus Müller](https://github.com/MagMueller/)

## Notebook features

- Data preprocessing
- Data checking
- Tensorflow dataset from own generator
- Different Tensorflow models using the functional API
- Outputs results in Tensorboard
- k-means and greyscaling segmentation as a comparison

## Contributing

Contributions are always welcome! Although we published this project, it does not mean it is finished! 
If you see anything, that can be done better, or can be improved - please contribute!

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`.

## Final network image

![Image of the tensorflow model](https://github.com/michael-ra/SSIS_Roof_DiffFeatClust/blob/main/Model.jpeg?raw=true)
## References

<a id="1">[1]</a> K. A. Kanezaki and M. Tanaka. Unsupervised learning of
image segmentation based on differentiable feature clustering.
IEEE Transactions on Image Processing, 29:8055–8068
