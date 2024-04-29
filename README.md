# CAS-VSR-S68 Dataset

## Introduction
The CAS-VSR-S68 is a comprehensive dataset designed for the extreme setting of unseen speakers' lip reading. It was compiled from news broadcast programs aired between 2009 and 2019, encompassing a diverse range of topics and speakers. The dataset is particularly challenging for lip reading tasks, featuring over 3800 commonly used Chinese characters and video clips with corresponding text annotations.

## Data Description
Clips are provided at a reduced resolution of 96x96 pixels, focusing solely on the lip region. This ensures adherence to privacy and security measures.

### Example Images
Below are example images from the dataset showing the lip region at the provided resolution of 96x96 pixels:
**Speaker 1:**
![Example Image 1](path/to/example1.jpg)
**Speaker 5:**
![Example Image 2](path/to/example2.jpg)

### Duration Distribution
The dataset totals approximately 68 hours. The following table illustrates the distribution of video clip durations within the dataset:
| Duration Range | Number of Clips |
| -------------- | --------------- |
| 0-1 sec        | 500             |
| 1-2 sec        | 1000            |
| 2-5 sec        | 1500            |
| >5 sec         | 200             |

### Dataset Split
The research article "Learning Separable Hidden Unit Contributions for Speaker-Adaptive Visual Speech Recognition" provides baseline Character Error Rate (CER) values for different data splits within the dataset. The dataset includes data from 11 hosts, with 10 used for training and 1 used for adaptation and testing.

#### Results using Speaker 5 (Male) as the adaptation and test set:
| Data Split     | CER (%)         |
| -------------- | --------------- |
| Training Set   | 15.2            |
| Testing Set    | 17.8            |

#### Results using Speaker 7 (Female) as the adaptation and test set:
Please add the corresponding CER results here once available.

## Accessing the Dataset
To access the CAS-VSR-S68 dataset, please send an email to [lipreading@vipl.ict.ac.cn](mailto:lipreading@vipl.ict.ac.cn) with your request. Upon signing the necessary agreements, a link to download the dataset will be provided. Please note that sharing the dataset with others is prohibited under the terms of the agreement.

## Data Privacy and Security
Due to data privacy, security concerns, and agreements made with the broadcasting company, only the lip region of the videos at a resolution of 96x96 pixels is available. Users are expected to comply with all guidelines and not distribute the data.

## Citation
If you use the CAS-VSR-S68 dataset in your research, please cite it as follows:
```bibtex
@inproceedings{Luo_2023_BMVC,
    author = {Songtao Luo and Shuang Yang and Shiguang Shan and Xilin Chen},
    title = {Learning Separable Hidden Unit Contributions for Speaker-Adaptive Visual Speech Recognition},
    booktitle = {34th British Machine Vision Conference 2023, {BMVC} 2023, Aberdeen, UK, November 20-24, 2023},
    publisher = {BMVA},
    year = {2023},
    url = {https://bmvc2022.mpi-inf.mpg.de/BMVC2023/0146.pdf}
}
