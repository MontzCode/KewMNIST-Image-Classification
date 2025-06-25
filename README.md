# Plant Image Classification with Keras in R

This repository contains the code and resources for building a simple neural network to classify plant images from the KewMNIST dataset. The project is implemented entirely in R using the `keras` and `tensorflow` libraries. It serves as a practical example of computer vision for ecological applications.

This project is based on the Week 12 lab for the "BIO728P: AI and Data Analytics in Ecology and Evolution" course.


*(Image showing model predictions. Correct predictions are labeled in blue, incorrect in red.)*

## About the Dataset

The `Kew-MNIST-full-dataset.Rdata` file contains the **KewMNIST** dataset, which consists of 500x500 pixel grayscale images of plants, categorized into six classes:
1.  Flower
2.  Leaf
3.  Plant-Tag
4.  Stem
5.  Whole-Plant
6.  Fruit *(Note: This class name is inferred, as the scripts refer to 6 classes)*

## Model Architecture and Performance

The project implements a simple sequential neural network with the following layers:
1.  **Flatten Layer:** Transforms the 500x500 image matrices into a 1D vector.
2.  **Dense Layer:** A fully connected layer with 128 units and a ReLU activation function.
3.  **Output Layer:** A dense layer with 6 units (one for each class) and a Softmax activation function to output class probabilities.

The model is trained for 10 epochs, and its performance (loss and accuracy) is tracked.



## Repository Contents

-   `BIO728P-Week-12-Setup-Script.R`: An R script to install and configure the necessary environment, including `keras`, `tensorflow`, and `reticulate`.
-   `BIO728P-Week-12-KewMNIST-Script.R`: The main R script that performs the following steps:
    -   Loads the KewMNIST dataset.
    -   Builds the neural network model.
    -   Trains the model on the training data.
    -   Evaluates the model's accuracy on the test data.
    -   Generates and visualizes predictions on new images.
    -   Calculates per-class accuracy.
-   `Kew-MNIST-full-dataset.Rdata`: The dataset file required to run the main script. *(Note: Due to its potential size, you might need to use Git LFS or provide a download link if it's too large for a standard GitHub repository).*
-   `.gitignore`: A standard R `.gitignore` file to exclude unnecessary files from version control.
-   `LICENSE`: The MIT License file.

## How to Run

### 1. Prerequisites
-   [R](https://www.r-project.org/)
-   [RStudio Desktop](https://posit.co/download/rstudio-desktop/)
-   [Python](https://www.python.org/downloads/)

### 2. Setup
1.  Clone this repository to your local machine:
    ```bash
    git clone https://github.com/[Your-Username]/Computer-Vision-KewMNIST.git
    cd Computer-Vision-KewMNIST
    ```
2.  Open the `BIO728P-Week-12-Setup-Script.R` in RStudio.
3.  **Important:** Before running, you may need to edit the Python path in the script to match your local Python installation:
    ```R
    # In BIO728P-Week-12-Setup-Script.R
    use_python("C:/path/to/your/python.exe", required = TRUE)
    ```
4.  Run the entire setup script from a fresh R session. This will install all required packages and libraries.

### 3. Training and Evaluation
1.  Ensure the `Kew-MNIST-full-dataset.Rdata` file is in the same directory as the R scripts.
2.  Open and run the `BIO728P-Week-12-KewMNIST-Script.R` file in RStudio.
3.  The script will train the model, evaluate its performance, and generate plots showing the results.
