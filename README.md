# On Demographic Group Fairness Guarantees in Deep Learning

The code for our paper published in IEEE Transactions on Pattern Analysis and Machine Intelligence entitled **On Demographic Group Fairness Guarantees in Deep Learning**. If you have any questions, please email <harvardophai@gmail.com> and <harvardairobotics@gmail.com>.

## Dataset

### [FairVision](https://ophai.hms.harvard.edu/datasets/harvard-fairvision30k)
FairVision contains 30,000 2D scanning laser ophthalmoscopy (SLO) fundus images from 30,000 patients, with six demographic identity attributes available for each patient. This dataset features three common ophthalmic diseases: Diabetic Retinopathy (DR), Age-related Macular Degeneration (AMD), and Glaucoma, with 10,000 samples for each disease. According to the official configuration, for each disease, 6,000 samples are used for training, 1,000 for validation, and 3,000 for testing. In this study, we focus on three demographic attributes—race, gender, and ethnicity—along with SLO fundus images.

### [CheXpert](https://stanfordmlgroup.github.io/competitions/chexpert/)
CheXpert is a large dataset of chest X-rays labeled for 14 common chest pathologies based on radiologist reports. It provides three demographic identity attributes: age, gender, and race. Following the split setting in prior studies, we use a total of 42,884 patients with 127,118 chest X-ray scans: 76,205 for training, 12,673 for validation, and 38,240 for testing. Our experiments focus on pleural effusion detection across race and gender demographic attributes.

### [HAM10000](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)
HAM10000 consists of 10,015 dermatoscopic images collected over 20 years from the Medical University of Vienna and a dermatology practice in Queensland, Australia. After filtering images with missing sensitive attributes, we obtained 9,948 images and grouped the original seven diagnostic labels into two categories: benign and malignant. This binary classification task is designed to simplify the analysis. In this study, we focus on gender and age as demographic attributes in the context of skin cancer detection.

### [FairFace](https://chalearnlap.cvc.uab.cat/dataset/36/description/)
FairFace is a newly curated dataset containing approximately 13,000 images from 3,000 new subjects combined with a reannotated version of the IJB-C dataset, resulting in a total of 152,917 facial images from approximately 6,100 unique identities. The dataset is divided into three subsets: 100,186 images for training, 17,138 for validation, and 35,593 for testing. It is comprehensively annotated for protected attributes such as gender and skin color, as well as additional features including age group, eyeglasses, head pose, image source, and face size. In this study, we address glasses detection as a binary classification task, distinguishing images with and without eyeglasses, while focusing on age, skin color, and gender as demographic attributes.

## Experiments

### AMD Detection on FairVision
To run the experiments with the baseline models (e.g., ViT) on the task of AMD detection, execute:
```bash
python train_amd_vit_fea.py
```
Or using the EfficientNet model:
```
python train_amd_efficientnet_fea.py
```

### DR Detection on FairVision
To run the experiments with the baseline models (e.g., ViT) on the task of DR detection, execute:
```bash
python train_dr_vit_fea.py
```
Or using the EfficientNet model:
```
python train_dr_efficientnet_fea.py
```

### Glaucoma Detection on FairVision
To run the experiments with the baseline models (e.g., ViT) on the task of Glaucoma detection, execute:
```bash
python train_glaucoma_vit_fea.py
```
Or using the EfficientNet model:
```
python train_glaucoma_efficientnet_fea.py
```

### Pleural Effusion Detection on Chexpert
To run the experiments with the EfficientNet on the task of Pleural Effusion detection, execute:
```bash
python train_chexpert_efficientnet_fea.py
```

### Skin Cancer Detection on HAM
To run the experiments with the EfficientNet on the task of Skin Cancer detection, execute:
```bash
python train_ham_efficientnet_fea.py
```

### Glasses Detection on FairFace
To run the experiments with the EfficientNet on the task of Glasses detection, execute:
```bash
pythontrain_fairface_efficientnet_fea.py
```
## Acknowledgement & Citation

If you find this repository useful for your research, please consider citing our [paper](https://ieeexplore.ieee.org/abstract/document/11435296):

```bibtex
@article{luo2026demographic,
  title={On Demographic Group Fairness Guarantees in Deep Learning},
  author={Luo, Yan and Wen, Congcong and Shi, Min and Huang, Hao and Fang, Yi and Wang, Mengyu},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year={2026},
  publisher={IEEE}
}
