# Explainable AI for Multivariate Spatio Temporal Dataset: Meteonet

Implementation is associated with the Research carried out with the title "Explainable Spatio-Temporal Image Segmentation for multivariate data: A Case Study on Precipitation Nowcasting"

This includes,
 - Downloading the raw data from Meteonet Dataset
 - Processing raw data and creating sequences of inputs and targets
 - Normalizing and appling pre-processing to the data
 - Building a Predictive model, Training and Evaluating
 - Appling XAI approaches on the prediction(GRAD CAM and Integrated Gradients)

---

## Pre-requisits

1. Python Conda Environment created with environment.yml file

```python
conda env create -n meteonet-xai -f environment.yml
```

2. Minimum Memory(RAM) of 16 GB (Recommended to use Google Colab for Execution to avoid memory issues)

## Instructions

Executing the notebooks in the following order will download the meteonet data from source and will lead until the model training, evalutaion and appling XAI approaches. Non of the datasets/intermediate data are added to the repo due to storage issues.

1. *1_download_raw_data.ipynb*:   Download the data from original sources and writes them to `raw_data`
2. *2_create_input_target_sequences.ipynb*:   Reads data from `raw_data` and writes to `processed_data` folder 
3. *3_save_normalized_data.ipynb*:    Reads data from `processed_data` and writes to `processed_normalized_data` folder
4. *4_train_test_n_xai.ipynb*:    Reads data from `processed_normalized_data` and generates the final results

Running them inorder will Download the necessary data for the next step. But If needed to skip any step and move to the following one, Can download the data manually into the respective input folder and proceed.
