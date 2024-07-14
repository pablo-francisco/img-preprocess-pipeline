# img-preprocess-pipeline

## Description:

The package **img-preprocess-pipeline** is used to:

- Load images
- Display images
- Preprocess images to input in machine learning projects
    - Reshape images
    - Normalize images
    - Augument images

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install img-preprocess-pipeline

```bash
pip install img-preprocess-pipeline
```

## Usage
### Preprocessing
```python
from img-preprocess-pipeline.preprocessing import tools, pipeline


tools.reshape_image(image) #Reshapes a image and returns a dictionary with the title "Reshaped" and the resulting image

tools.scale_image(image) #Scales a image (with range 0 to 1) and returns a dictionary with the title "Scaled" and the resulting image

tools.scale_image(image) #Scales a image (with range 0 to 1) and returns a dictionary with the title "Scaled" and the resulting image


tools.random_augumentation(image) #Create a new image modifying the saturation, brightness and rotation (in a random approach) of the original image and returns a dictionary with the title "Augumented image" and the resulting image.


tools.pipeline(image) #Create a new image using all the other functions in "tools" in combined into a pipeline. Returns a dictionary with the title "Preprocessed" and the resulting image.

```

### Utils

```python
from img-preprocess-pipeline.utils import io, display_images

image_path = "your_image.png"

io.load_image(image_path,grayscale=False) #Load the image from the directory in scale RGB (with grayscale=False) and returns a tensor array.

io.save_image(image,save_path) #Saves a image converting from tensorinto a numpy array.

io.display_images(image,image1,...,image_x) #Displays the images and the respective labels of the images (Scaled,Preprocessed...) in a matrix of images with shape of (1,X) images.
```

## Author
Pablo Francisco

## License
[MIT](https://choosealicense.com/licenses/mit/)