## 0.Table of Contents

  - [0.Table of Contents](#0.table-of-contents)
  - [1.Reference Survey Paper](#1.reference-survey-paper)
  - [2.Other Survey Paper](#2.other-survey-paper)
  - [3.Challenges and Techniques](#3.challenges-and-techniques)
     - [3.1.Feature Extraction](#3.1.feature-extraction)
	    - [3.1.1.Temporal Feature Extraction](#3.1.1.temporal-feature-extraction)
	    - [3.1.2.Multimodal Feature Extraction](#3.1.2.multimodal-feature-extraction)
     - [3.2.Annotation Scarcity](#3.2.annotation-scarcity)
	    - [3.2.1.Self-supervised learning](#3.2.1.self-supervised-learning)
	    - [3.2.2.Semi-supervised learning](#3.2.2.semi-supervised-learning)
  - [4.Datasets](#4.datasets)


---

## 1.Reference Survey Paper
:star: **Deep Learning for Sensor-based Human Activity Recognition: Overview, Challenges and Opportunities (ACM Computing Surveys)** [[**paper**](https://arxiv.org/pdf/2001.07416.pdf)]

Some of papers and the main structure of this repository are inspired by this paper!!

---

## 2.Other Survey Paper

  - A Survey on Deep Learning for Human Activity Recognition(ACM Computing Surveys)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3472290)]

---

## 3.Challenges and Techniques

### 3.1.Feature Extraction

#### 3.1.1.Temporal Feature Extraction 

---

  - A-Wristocracy: Deep Learning on Wrist-worn Sensing for Recognition of User Complex  Activities(BSN2015)[[**paper**](https://ieeexplore.ieee.org/document/7299406)]

    - [*deep learning(mlp-based)*] [*mean, variance*] [*fine-gained*] [*wrist-worn*] [*multi-sensors*]

  - Human Activity Recognition using Wearable Sensors by Deep Convolutional Neural Networks(ACM MM2015)[[**paper**](https://dl.acm.org/doi/abs/10.1145/2733373.2806333)]
	- [*deep learning(cnn-based)*] [*novel activity image(stack, 2D DFT)*] [*multi-sensors*]

  - TagFree Activity Identification with RFIDs(ACM IMWUT2018)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3191739)]

	 - [*deep learning(cnn-lstm-based)*] [*RFID signals*] [spectrum(with time-angle)]

  - Sensing Fine-Grained Hand Activity with Smartwatches(CHI2019)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3290605.3300568)]

	- [*deep learning(cnn-based)*]  [*time frequency spectral(FFT)*] [*fine-gained*]

---

  - Towards reading trackers in the wild: detecting reading activities by EOG glasses and deep neural networks(UbiComp17)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3123024.3129271)]

	 - [*end-to-end deep learning(bilstm)*]

  - Ensembles of Deep LSTM Learners for Activity Recognition using Wearables(UbiComp2017)[[**paper**](https://arxiv.org/abs/1703.09370)]

	 - [*end-to-end deep learning(ensemble-lstm)*] [*ensemble trick: epoch-wise bagging*]

  - DeepSense: A Unified Deep Learning Framework for Time-Series Mobile Sensing Data Processing(WWW17)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3038912.3052577)] [[**code**](https://github.com/yscacaca/DeepSense)]

	 - [*end-to-end deep learning(cnn, gru)*] 

  - Making sense of spatio-temporal preserving representations for EEG-based human intention recognition(IEEE Transactions on Cybernetics2020)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8698218)]

	 - [*end-to-end deep learning(cnn-lstm-based)*] [*spatio-temporal(EEG signals, EEG electrode map)*] 

---

  - Deep convolutional neural networks on multichannel time series for human activity recognition(AAAI2015)[[**paper**](https://www.aaai.org/ocs/index.php/IJCAI/IJCAI15/paper/viewFile/10710/11297)]

	 - [*end-to-end deep learning(Temporal CNN)*]

  - Deep Neural Network based Human Activity Recognition for the Order Picking Process(iWOAR17)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3134230.3134231)] [[**code**](https://github.com/wilfer9008/CNN_IMU)]

	 - [*end-to-end deep learning(Temporal/1D CNN)*] [*sliding window*] [*IMUs-based fusion and share weights each IMU*]

  - Prototype Similarity Learning for Activity Recognition(PAKDD2020)[[**paper**](https://link.springer.com/chapter/10.1007/978-3-030-47426-3_50)]

	 - [*end-to-end deep learning(Temporal/1D CNN, Spatial CNN*] [*Tricks: Distance-Based Classification Module(based on prototypical network), Cross-Subject Training*] 

---

  - Convolutional Neural Networks for Human Activity Recognition using Multiple Accelerometer and Gyroscope Sensors(IJCNN2016)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7727224)]

	 - [*modality specific(tricks: zero padding,partial and full weight sharing)*]


  - Human activity recognition from accelerometer data using Convolutional Neural Network(BigComp2017)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7881728)]

	 - [*multi-scale 1D-CNN*]

  - Deep dilated convolution on multimodality time series for human activity recognition(IJCNN2018)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8489540)]

	 - [*dilated cnn, lstm*]

---

  - Activity Recognition Using Dual-ConvLSTM Extracting Local and Global Features for SHL Recognition Challenge(UbiComp2018)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3267305.3267533)]

	 - [*dual-cnn-lstm(one small kernel size, one large)*] [*axis-based Fusion*]

  - Push the Limit of Acoustic Gesture Recognition(INFOCOM2020)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9229520)]

	 - [*cnn-lstm*] [*acoustic data*] [*frequency transmit*]

---

  - IF-ConvTransformer: A Framework for Human Activity Recognition Using IMU Fusion and ConvTransformer(Ubicomp2022)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3534584)]

	 - [*transformer-based(ConvTransformer)*] [*novel IMU fusion*]

---

#### 3.1.2.Multimodal Feature Extraction

##### Feature Fusion

---

  - Multi-modal convolutional neural networks for activity recognition(TMC2015)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7379657)]

	 - [*Early Fusion(2D vector)*]

  - Human Activity Recognition Using Wearable Sensors by Deep Convolutional Neural Networks(ACM MM2015)[[**paper**](https://dl.acm.org/doi/abs/10.1145/2733373.2806333)]

	 - [*Early Fusion(every signal to signal)*]

  - Locomotion activity recognition using stacked denoising autoencoders(JIOT2018)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8331081)]

	 - [*Early Fusion(1D vector)*] [*stack denoising autoencoder*]

---

  - Confidence-based Deep Multimodal Fusion for Activity Recognition(UbiComp18)[[**paper**](https://dl.acm.org/doi/10.1145/3267305.3267522)]

	 - [*Sensor-based Fusion*] [*tricks: sensors confidence score*]

---

##### Classifier Ensemble

---

[back to top](#0.table-of-contents)

### 3.2.Annotation Scarcity

#### 3.2.1.Self-supervised learning

  - SelfHAR: Improving Human Activity Recognition through Self-training with Unlabeled Data(IMWUT2021)[[**paper**](https://arxiv.org/abs/2102.06073)] [[**code**](https://github.com/iantangc/SelfHAR)]

	 - [*self-supervised learning*] [*teacher-student*] [*multi-task learning*]

  - Contrastive Self-supervised Learning for Sensor-based Human Activity Recognition(IJCB2021)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9484410)]

	 - [*self-supervised learning*] [*contrastive learning*] [*tricks: five random augmentation*]

  - Self-supervised Learning for Human Activity Recognition Using 700,000 Person-days of Wearable Data(Arxiv2022)[[**paper**](https://arxiv.org/abs/2206.02909)] [[**code**](https://github.com/OxWearables/ssl-wearables)]

	 - [*self-supervised learning*] [*multi-task learning(invert, permute,time warp)*]

  - ColloSSL: Collaborative Self-Supervised Learning for Human Activity Recognition(IMWUT2022)[[**paper**](https://arxiv.org/abs/2202.00758)]

	 - [*self-supervised learning*] [*contrastive learning(novel: use nature transformations)*] [*backbone: 1D-CNN*]

---

#### 3.2.2.Semi-supervised learning

  - Deep-Learning-Enhanced Human Activity Recognition for Internet of Healthcare Things(JIOT2020)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9055403/)]

	 - [*semi-supervised learning(autolabeling based on RL)*] [*reinforcement learning(DQN)*] [*lstm*]

---

[back to top](#0.table-of-contents)

## 4.Datasets



