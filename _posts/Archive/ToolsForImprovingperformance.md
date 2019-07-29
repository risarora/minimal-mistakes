# Most powerful and unheard of tools for data scientists


### Pandas profiling
* https://github.com/pandas-profiling/pandas-profiling
conda install -c anaconda pandas-profiling


### Feature Tool
* https://www.featuretools.com/

### LIME
If you're an active machine learning engineer you may have noticed that more customers than ever ask how a model is coming to a specific decision. They no longer blindly trust the model.

This can be quite a challenge as most models are hard to explain to a customer. But there is a solution.

LIME (Local Interpretable Model Explainer) is a tool that allows you to explain a decision made by your classification model. This can either be a decision tree, random forest or even a neural network.

For example if you have a neural network that predicts a label for an image you can explain its functionality with the following code:
```
from lime.lime_image import LimeImageExplainer

explainer = LimeImageExplainer()

explanation = explainer.explain_instance(
    image,
    keras_model.predict,
    top_labels=5,
    hide_color=0
    num_samples=1000)


from skimage.segmentationskimage  import mark_boundaries

temp, mask = explanation.get_image_and_mask(
    295,
    positive_only=True,
    num_features=5,
    hide_rest=False)

plt.imshow(mark_boundaries(temp / 2 + 0.5, mask))
```
First we create a new explainer for our image classifier. Then we let it explain the classification for a specific image. This produces an explanation object that we can visualize.

Explainer output

The visualization is done using matplotlib. Using the mark_boundaries method we can highlight the edges of the area that explains why our image was classified the way it is.


* https://github.com/marcotcr/lime

### Boundary box annotations tool
https://github.com/maverickjoy/bounding-box-annotation-tool

### Google Facets



https://fizzylogic.nl/2018/08/21/5-must-have-tools-if-youre-serious-about-machine-learning/
