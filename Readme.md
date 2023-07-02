# EuroSAt Classifier and Application to Detect Deforestation in Indonesia

## Short Description

This land-use classifier was developed using EuroSAT satellite data with the intent to detect and track land-use change in remote areas at risk of deforestation. This project is a first pass and should be seen as a proof of concept. The final model was constructed using transfer learning with ResNet-152v2 as the base model and fine-tuned on labeled satellite data. This model reached 95% accuracy with minimal tuning, which is near state-of-the-art oerformance on this oarticular dataset. The model was then used to detect land use change in a subregion of Indonesia between 2020 and 2023, flagging possible deforestation. Cursory inspetion of the results indicate that the algorithm is far from perfect, but shows promise. Out of sample data is likely a large problem here, and creating a dataset of labeled observations from the target area on which to fine tune could ameliorate this.

Note: this notebook was written for Google Colab, ans won't run as-written in Jupyter.

## Dat

This classifier was trained on the [EuroSAT RBG Dataset from Helber et. al.](https://github.com/phelber/EuroSAT)

New satellite data was retrieved from EEOP's Sentinel-2 Satellite. This is the same satellite data used in EuroSAT and is processed in the same way.

