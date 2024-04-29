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
| Speaker | Total Duration (min) |
|---------|----------------------|
| S1      | 708.85               |
| S2      | 671.99               |
| S3      | 621.02               |
| S4      | 584.59               |
| S5      | 461.52               |
| S6      | 324.00               |
| S7      | 294.03               |
| S8      | 171.56               |
| S9      | 143.19               |
| S10     | 82.91                |
| S11     | 39.21                |
| **Total** | **4103.37(68.3h)**       |

### Dataset Split
The research article "Learning Separable Hidden Unit Contributions for Speaker-Adaptive Visual Speech Recognition" provides baseline Character Error Rate (CER) values for different data splits within the dataset. The dataset includes data from 11 hosts, with 10 used for training and 1 used for adaptation and testing.

#### Results using Speaker 6 (Male) as the adaptation and test set:
| Adapt (min) | Baseline (%) | Proposed Method (%)(LDVSD) |
|-------------|--------------|---------------------|
| 0                  | 19.61    | 19.37           |
| 1                  | 21.53    | 20.69           |
| 3                  | 18.65    | 18.55           |
| 5                  | 17.55    | **16.72**           |

#### Results using Speaker 10 (Female) as the adaptation and test set:
| Adapt (min) | Baseline (%) | Proposed Method (%)(LDVSD) |
|-------------|--------------|---------------------|
| 0           | 44.93        | 43.24               |
| 1           | 38.63        | 37.38               |
| 3           | 36.37        | 35.64               |
| 5           | 33.79        | **33.17**               |

For more details, please refer to the [GitHub repository](https://github.com/jinchiniao/LSHUC).

## Accessing the Dataset
To access the CAS-VSR-S68 dataset, please send an email to [lipreading@vipl.ict.ac.cn](mailto:lipreading@vipl.ict.ac.cn) with your request. Upon signing the necessary agreements, a link to download the dataset will be provided. Please note that sharing the dataset with others is prohibited under the terms of the agreement.
## File Structure and Contents

### `lip_imgs` (Lip Images) 
**After obtaining access and unzipping**, this directory contains folders of lip region images. Each folder is named with the unique identifier (UUID) of the video clip and contains a sequence of ``.jpg` images.


Example:
```
lip_imgs/
├── 0a1ddef8-20e6-2e4b-c002-6cb6c5923585.zip
│ ├── 00000.jpg
│ ├── 00001.jpg
│ └── ...
```
### `utterance` (Corresponding Text) 
**After obtaining access and unzipping**, this directory Includes transcription files corresponding to the lip images. Each transcription file is associated with a specific image and is named using a combination of the UUID and image sequence number.

Example:
```
utterance/
├── 0a1ddef8-20e6-2e4b-c002-6cb6c5923585_00000
│ ├── 0001.txt
│ ├── 0002.txt
│ └── ...
```
### `uuid2spk.csv` (UUID to Speaker Mapping)
A CSV file that maps each utterance identifier (UUID) to a speaker identifier.
This layout gives users a clear picture of the dataset's organization and how to locate specific pieces of information within it.

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
