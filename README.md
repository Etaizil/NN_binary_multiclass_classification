# Binary and Multiclass classification

## Description
This repository contains neural network implementations for both **binary** and **multiclass classification** tasks. In the first part we train to classify two chosen **sign language hand digits** in a binary classification problem, where in the second part we extends to a multiclass classification problem to classify between all hand digits **0 – 9**. The second part includes a Base Model, and also two experiments to observe the effects of changes in architecture and hyperparameters on model performance.

## Key Features

- **Binary Classification**: A network is trained to classify two chosen sign language hand digits.
- **Multiclass Classification**: A Base Model network is trained to distinguish between all sign language hand digits 0 – 9.
- **Experiments in Multiclass Classification**:
    1. **Architecture Experiment**: Changing the network architecture to observe its impact on performance.
    2. **Hyperparameter Experiment**: Modifying hyperparameters to study their effects on model performance.
- **CUDA Support**: The code can leverage GPU acceleration for faster computations. In **Google Colab**, go to **Runtime** → **Change runtime type** → **Select "T4 GPU"** → **Save**.
- **Training & Evaluation**: Includes Jupyter Notebook for training the network, evaluating its performance, and plotting loss and accuracy metrics for both binary and multiclass tasks.

## Dataset

The dataset used in this project is based on **sign language hand digits**.

## Getting Started

**Note: This notebook has been prepared for the evaluation of a tester that will run specific code blocks, without the training phase.**
**If you'd like to train, test, and just play with the code in the notebook, please make sure to remove the `%%script echo skipping` from the relevant code blocks.**
See "Instructions for Training the Model from Scratch" for more.

## Downloading the .npy files
Please make sure to download examples.zip in order to upload pictures for model evaluation.

### Run the Notebook on Google Colab
To get started, simply run the notebook on **Google Colab**. The workflow is easy and straightforward, with no setup required — the dataset is handled automatically.

📌 **Access the notebook here:** [Google Colab Notebook](https://colab.research.google.com/drive/11X9J2gXqmLOWoQkGUD4JWVuCYijpxok-?usp=sharing)

---

The following instructions are for those who would like to only evaluate the model with the .npy files.

### 1. Skip Initial Cells
- All cells before the model loading section are prefixed with `%%script echo skipping`.
- These cells will not execute and will clear the last printed output.
- No need to use "Run All".

### 2. Start from the `gdown` Download Cell
- Navigate to the **Test Environment (of part 2 only)** section in the notebook.
- Run the import cell to import necessary libraries.
- Locate the cell where the model is downloaded using `gdown`.
- Run this cell to download the pre-trained model from Google Drive.

### 3. Upload `.npy` Files for Prediction
- In the final cell, you'll be prompted to upload `.npy` files.
- Choose the sign language digit images you want the model to classify.

### 4. View Predictions
- After uploading, the model will output the predicted digit for each file.

---

## Instructions for Training the Model from Scratch

If you'd like to **train the model** again, follow these steps:

1. **Remove `%%script echo skipping`** from the relevant code blocks.
2. **Save the trained model**:
   - Navigate to the **Save Trained Model** section in the notebook.
   - Modify the code block where the model is saved by changing the model name to the desired one.
   
   ```python
   # We chose MODEL 2 - with hidden layers.
   torch.save(model_two, 'chosen_model.pth')

3. **Run the code block.**  This will save the model to the content folder.

4. **Upload the model to Google Drive and get link ID**
  - Download the saved model file (e.g., chosen_model.pth) to your computer.
  - Upload it to your Google Drive.
  - Set the file sharing permissions to Viewer and copy the sharing link.
  - (**Right-click** on the file → **Share** → **Share** → **Anyone with the link** → **Viewer** → **copy** the sharing link, and **Save**).
  - From the Google Drive sharing link, copy the model ID part. This is the string that appears between d/ and /view in the link.

6. **Update the gdown Download Cell**

  - In the notebook, locate the cell that downloads the model using gdown.
  ```python
  !gdown --id 1YyPuLs8_eZ4xdevcmRmdf_VVurPnLmvZ
  ```
  - Replace the current model ID with your newly copied ID from Google Drive.

7. **Proceed with the rest of the notebook**

  - After updating the model ID and running the code, the notebook will download the trained model from your Google Drive.
  - Run the cells below the model download section to continue for evaluation. The last code block will allow you to upload .npy files for evaluation.
  - **Note:**  Even when doing "Run all" again, the model that will be loaded is the model that was uploaded to google drive, not the last run.

---

## Results

In the **multiclass classification** part, two experiments were conducted:
1. **Architecture Experiment**: Different network architectures were tested to assess their impact on performance.
2. **Hyperparameter Experiment**: Changes in hyperparameters were made to see how they affected the model's performance.

For further details on the model design, experiments, and results, please refer to the attached report, which provides a comprehensive analysis of the entire project.

---

Feel free to reach out if further clarification is needed!


## License

This project is licensed under the MIT License - see the LICENSE file for details.
