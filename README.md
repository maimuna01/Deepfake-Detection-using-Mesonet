# Deepfake Detection Using MesoNet Architecture

This project focuses on detecting deepfakes in images using the MesoNet network architecture, which is specifically designed for identifying facial manipulations. The model leverages key deep learning frameworks including TensorFlow, Keras, PyTorch, and OpenCV for efficient processing and analysis.

## Requirements

- Python 3.5
- Numpy 1.14.2
- Keras 2.1.5

## Frameworks and Tools:
- **TensorFlow**, **Keras**: For model development and training.
- **PyTorch**: Supporting model optimization and performance tuning.
- **OpenCV**: Used for image processing and manipulation tasks.

## Dataset Overview:

### Training Set:
- **Forged Images**: 5,111
- **Real Images**: 7,250

### Validation Set:
- **Forged Images**: 2,889
- **Real Images**: 4,259

[Download link for the dataset](https://my.pcloud.com/publink/show?code=XZLGvd7ZI9LjgIy7iOLzXBG5RNJzGFQzhTRy)

### Balance:
- Both the training and validation sets maintain a balanced distribution between forged and real images. This balance ensures that the model is effectively trained to recognize deepfake patterns and generalize across different data scenarios.

## Pretrained models

You can find the pretrained weight in the `weights` folder. The `_DF` extension correspond to a model trained to classify deepfake-generated images and the `_F2F` to Face2Face-generated images.

## How to Run
1. Clone the Repository
```bash
git clone https://github.com/Deepfake-Detection-using-Mesonet.git
cd Deepfake-Detection-using-Mesonet
```
2. Download and Prepare the Dataset
```bash
/data
  /train
    /real
    /forged
  /validation
    /real
    /forged
```

3. Train the Model
```bash
python train.py --epochs 50 --batch_size 32
```

4. Validate the Model
```bash
python validate.py --model mesonet_model.h5 --data_dir ./data/validation
```

5. Run Inference on New Data
```bash
python predict.py --image_path ./path_to_image.jpg --model mesonet_model.h5
```

## Purpose:
The primary goal of this project is to develop a robust detection framework that identifies deepfake images with high accuracy. By training the model on a diverse dataset, the system is validated for real-world deployment, providing a critical tool for cybersecurity and digital forensics.

## Key Features:
- **MesoNet Architecture**: A compact Convolutional Neural Network (CNN) architecture designed for detecting facial forgeries with precision.
- **Cybersecurity Application**: The system enhances the integrity of digital media by identifying manipulated content, safeguarding against threats like misinformation, identity theft, and fraud.

## Authors

**Maimuna Khatoon** - [Github](https://github.com/maimuna01)

**Charvi Jaiswal** - [Github](https://github.com/charvijaiswal)

**Sheryl Sokhi** - [Github](https://github.com/sherylsokhi)

**Tulika Tripathi** - [Github](https://github.com/tulitrip)

## References

Afchar, D., Nozick, V., Yamagishi, J., & Echizen, I. (2018, September). [MesoNet: a Compact Facial Video Forgery Detection Network](https://arxiv.org/abs/1809.00888). In IEEE Workshop on Information Forensics and Security, WIFS 2018.
