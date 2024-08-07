# **Library**: img-preprocess-pipeline

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)


[![GitHub License](https://img.shields.io/badge/License-MIT-green)](https://github.com/pablo-francisco/img-preprocess-pipeline/blob/master/LICENSE)
[![GitHub Commits](https://badgen.net/github/commits/pablo-francisco/img-preprocess-pipeline/master?color=green&icon=github)](https://github.com/pablo-francisco/img-preprocess-pipeline/commits/master)


# 📋 Table of Contents

1. 📖 [Project description](#Project-description)
2. 🔨 [Installation](#Installation)
3. ⚙️ [Functions](#Functions)
4. ☕ [Author and contact](#Author-and-contact)
5. ©️   [License](#License)


# <a name="Project-description">📖 Project description</a>

The **img-preprocess-pipeline** package provides a comprehensive solution for loading, displaying, and preprocessing images, streamlining their use in machine learning projects. Its features include:

- **Image Loading:** Import images from various sources and formats.
- **Image Displaying:** Quickly and intuitively visualize images.
- **Image Preprocessing:** Prepare images for use in machine learning models through:
    - **Reshaping:** Adjust the dimensions of images as needed.
    - **Normalization:** Scale pixel values to a specific range, enhancing model performance.
    - **Data Augmentation:** Apply techniques to expand the dataset and increase model robustness.

This package aims to simplify and automate image preprocessing steps, optimizing the workflow in machine learning projects, the library link can be found [here](https://pypi.org/project/img-preprocess-pipeline/).

# <a name="Installation">🔨 Installation</a>

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install img-preprocess-pipeline

```bash
pip install img-preprocess-pipeline
```

### **Import**

```python
from image_preprocessing.preprocessing import tools, pipeline
from image_preprocessing.utils import io, display_images
```

# <a name="Functions">⚙️ Functions</a>



### Load image

```python
image_path = "your_image.png"
io.load_image(image_path,grayscale=False)
```

- Input: 
    - image_path: directory of image
    - grayscale: load image with grayscale or RGB

- Output: 
    - image (PIL Jpeg)

**Description**:

Load the image from the directory in scale RGB (with grayscale=False) and returns a tensor array.

**Output example**:

![alt text](images/cat.jpg)


---

### Save image
```python
io.save_image(image,save_path) 
```
- Input:
    - image: choosen image file
    - save_path: directory to save the image

- Output:
    - None

**Description**:

Saves a image converting into a numpy array.

---


### **Reshape image**
```python
tools.reshape_image(image)
```


- Input:
    - image or dict: {title_of_image: image}
- Output:
    - dict: {'Reshaped': reshaped_image}

**Description**:

Reshapes a image and returns a dictionary with the title "Reshaped" and the resulting image.

**Output example**:

![alt text](images/reshaped_image.jpg)

---

### **Scaling image**

```python
tools.scale_image(image)

```

- Input:
    - image or dict: {title_of_image:image}
- Output:
    - dict: {'Scaled':scaled_image}

**Description**:
Scales a image (with range 0 to 1) and returns a dictionary with the title "Scaled" and the resulting image"""

**Output example**:

![alt text](images/scaled_image.jpg)

---

### Random augumentation

```python
tools.random_augumentation(image)
```

- Input:
    - image or dict: {title_of_image:image}
- Output:
    - dict: {'Augumented image':augumented_image}

**Description**:
Create a new image modifying the saturation, brightness and 
rotation (in a random approach) of the original image and returns 
a dictionary with the title "Augumented image" and the resulting image.

**Output example**:

![alt text](images/augumented_image.jpg)

---

### Preprocessing pipeline

```python
pipeline.preprocess_pipeline(image) 
```
- Input:
    - image or dict: {title_of_image:image}
- Output:
    - dict: {'Preprocessed':preprocessed_image}

**Description**:

Create a new image using all the other functions in "tools" in
combined into a pipeline. Returns a dictionary with the title 
"Preprocessed" and the resulting image.

**Output example**:

![alt text](images/preprocessed_image.jpg)

---
### Display images
```python
display_images.plot_images(image,image1,...,image_x) 
```

- Input:
    - dict of multiple images files. 
        Ex: 
        ```python
        image1_with_label={'Original': image1}
        ```

- Output:
    - None

**Description**:

Displays the images and the respective labels of the images (Scaled,Preprocessed...) in a matrix of images with shape of (1,X) images.

**Output example**:

![alt text](images/plot_images.png)

## <a name="Author-and-contact">☕ Author and contact</a>

Pablo Francisco Melo Bezerra

[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pablo-francisco-a07443239/)



## <a name="License">©️ License</a>
[MIT](https://choosealicense.com/licenses/mit/)