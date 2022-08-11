# Table of Contents

 - [Table of Contents](#table-of-contents)
 - [Reference Survey Paper](#reference-survey-paper)
 - [Other Survey Paper](#other-survey-paper)
 - [Challenges and Techniques](#challenges-and-techniques)
    - [Feature Extraction](#feature-extraction)
	   - [Temporal Feature Extraction](#temporal-feature-extraction)
	   - [Multimodal Feature Extraction](#multimodal-feature-extraction)
    - [Annotation Scarcity](#annotation-scarcity)
	   - [Self-supervised learning](#self-supervised-learning)
	   - [Semi-supervised learning](#semi-supervised-learning)
	   - [Unsupervised learning](#unsupervised-learning)
	- [Class Imbalanced](#class-imbalanced)
	- [Distribution Discrepancy](#distribution-discrepancy)
	- [User Features Privacy](#user-features-privacy)
 - [Datasets](#datasets)
 - [Github Repositories](#github-repositories)

# Reference Survey Paper
:star: **Deep Learning for Sensor-based Human Activity Recognition: Overview, Challenges and Opportunities (ACM Computing Surveys, 2021)** [[**paper**](https://arxiv.org/pdf/2001.07416.pdf)]

Some of papers and the main structure of this repository are inspired by this paper!!

# Other Survey Paper

  - A Survey on Deep Learning for Human Activity Recognition(ACM Computing Surveys, 2022)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3472290)]

# Challenges and Techniques

### Feature Extraction

#### *Temporal Feature Extraction* 

  - ***Handcraft:***

  - A-Wristocracy: Deep Learning on Wrist-worn Sensing for Recognition of User Complex  Activities(BSN, 2015)[[**paper**](https://ieeexplore.ieee.org/document/7299406)]

    - [*deep learning(mlp-based)*] [*mean, variance*] [*fine-gained*] [*wrist-worn*] [*multi-sensors*]

  - Human Activity Recognition using Wearable Sensors by Deep Convolutional Neural Networks(ACM MM, 2015)[[**paper**](https://dl.acm.org/doi/abs/10.1145/2733373.2806333)]
	- [*deep learning(cnn-based)*] [*novel activity image(stack, 2D DFT)*] [*multi-sensors*]

  - TagFree Activity Identification with RFIDs(IMWUT, 2018)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3191739)]

	 - [*deep learning(cnn-lstm-based)*] [*RFID signals*] [spectrum(with time-angle)]

  - Sensing Fine-Grained Hand Activity with Smartwatches(CHI, 2019)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3290605.3300568)]

	- [*deep learning(cnn-based)*]  [*time frequency spectral(FFT)*] [*fine-gained*]

  - ***End to End(CNN,RNN-Based):***

  - Towards reading trackers in the wild: detecting reading activities by EOG glasses and deep neural networks(UbiComp, 2017)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3123024.3129271)]

	 - [*end-to-end deep learning(bilstm)*]

  - Ensembles of Deep LSTM Learners for Activity Recognition using Wearables(UbiComp, 2017)[[**paper**](https://arxiv.org/abs/1703.09370)]

	 - [*end-to-end deep learning(ensemble-lstm)*] [*ensemble trick: epoch-wise bagging*]

  - DeepSense: A Unified Deep Learning Framework for Time-Series Mobile Sensing Data Processing(WWW, 2017)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3038912.3052577)] [[**code**](https://github.com/yscacaca/DeepSense)]

	 - [*end-to-end deep learning(cnn, gru)*] 

  - Making sense of spatio-temporal preserving representations for EEG-based human intention recognition(IEEE Transactions on Cybernetics, 2020)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8698218)]

	 - [*end-to-end deep learning(cnn-lstm-based)*] [*spatio-temporal(EEG signals, EEG electrode map)*] 

  - Deep convolutional neural networks on multichannel time series for human activity recognition(AAAI, 2015)[[**paper**](https://www.aaai.org/ocs/index.php/IJCAI/IJCAI15/paper/viewFile/10710/11297)]

	 - [*end-to-end deep learning(Temporal CNN)*]

  - Deep Neural Network based Human Activity Recognition for the Order Picking Process(iWOAR, 2017)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3134230.3134231)] [[**code**](https://github.com/wilfer9008/CNN_IMU)]

	 - [*end-to-end deep learning(Temporal/1D CNN)*] [*sliding window*] [*IMUs-based fusion and share weights each IMU*]

  - Prototype Similarity Learning for Activity Recognition(PAKDD, 2020)[[**paper**](https://link.springer.com/chapter/10.1007/978-3-030-47426-3_50)]

	 - [*end-to-end deep learning(Temporal/1D CNN, Spatial CNN*] [*Tricks: Distance-Based Classification Module(based on prototypical network), Cross-Subject Training*] 

  - Convolutional Neural Networks for Human Activity Recognition using Multiple Accelerometer and Gyroscope Sensors(IJCNN, 2016)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7727224)]

	 - [*modality specific(tricks: zero padding,partial and full weight sharing)*]

  - Human activity recognition from accelerometer data using Convolutional Neural Network(BigComp, 2017)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7881728)]

	 - [*multi-scale 1D-CNN*]

  - Deep dilated convolution on multimodality time series for human activity recognition(IJCNN, 2018)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8489540)]

	 - [*dilated cnn, lstm*]

  - Activity Recognition Using Dual-ConvLSTM Extracting Local and Global Features for SHL Recognition Challenge(UbiComp, 2018)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3267305.3267533)]

	 - [*dual-cnn-lstm(one small kernel size, one large)*] [*axis-based Fusion*]

  - Push the Limit of Acoustic Gesture Recognition(INFOCOM, 2020)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9229520)]

	 - [*cnn-lstm*] [*acoustic data*] [*frequency transmit*]

  - ***End to End(Transformer-Based):***

  - IF-ConvTransformer: A Framework for Human Activity Recognition Using IMU Fusion and ConvTransformer(Ubicomp, 2022)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3534584)]

	 - [*transformer-based(ConvTransformer)*] [*novel IMU fusion*]

#### *Multimodal Feature Extraction*

  - ***Feature Fusion:***

  - Multi-modal convolutional neural networks for activity recognition(TMC, 2015)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7379657)]

	 - [*Early Fusion(2D vector)*]

  - Human Activity Recognition Using Wearable Sensors by Deep Convolutional Neural Networks(ACM MM, 2015)[[**paper**](https://dl.acm.org/doi/abs/10.1145/2733373.2806333)]

	 - [*Early Fusion(every signal to signal)*]

  - Locomotion activity recognition using stacked denoising autoencoders(JIOT, 2018)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8331081)]

	 - [*Early Fusion(1D vector)*] [*stack denoising autoencoder*]

  - Confidence-based Deep Multimodal Fusion for Activity Recognition(UbiComp, 18)[[**paper**](https://dl.acm.org/doi/10.1145/3267305.3267522)]

	 - [*Sensor-based Fusion*] [*tricks: sensors confidence score*]

  - ***Classifier Ensemble:***

| [back to top](#table-of-contents) |
| --------------------------------: |

### Annotation Scarcity

#### *Self-supervised learning*

  - Contrastive Self-supervised Learning for Sensor-based Human Activity Recognition(IJCB, 2021)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9484410)]

	 - [*self-supervised learning*] [*contrastive learning*] [*tricks: five random augmentation*]

  - SelfHAR: Improving Human Activity Recognition through Self-training with Unlabeled Data(IMWUT, 2021)[[**paper**](https://arxiv.org/abs/2102.06073)] [[**code**](https://github.com/iantangc/SelfHAR)]

	 - [*self-supervised learning*] [*teacher-student*] [*multi-task learning*]

  - Self-supervised Learning for Human Activity Recognition Using 700,000 Person-days of Wearable Data(Arxiv, 2022)[[**paper**](https://arxiv.org/abs/2206.02909)] [[**code**](https://github.com/OxWearables/ssl-wearables)]

	 - [*self-supervised learning*] [*multi-task learning(invert, permute,time warp)*]

  - ColloSSL: Collaborative Self-Supervised Learning for Human Activity Recognition(IMWUT, 2022)[[**paper**](https://arxiv.org/abs/2202.00758)]

	 - [*self-supervised learning*] [*contrastive learning(novel: use nature transformations)*] [*backbone: 1D-CNN*]

#### *Semi-supervised learning*

  - Semi-Supervised Convolutional Neural Networks for Human Activity Recognition(BigData, 2017)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8257967/)]

	 - [*semi-supervised learning(CNN-Ladder)*]

  - Semi-supervised Learning for Human Activity Recognition Using Adversarial Autoencoders(UbiComp/ISWC, 2019)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3341162.3344854)]

	 - [*semi-supervised learning(Adversarial Autoencoders)*]

  - Deep-Learning-Enhanced Human Activity Recognition for Internet of Healthcare Things(JIOT, 2020)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9055403/)]

	 - [*semi-supervised learning(Autolabeling)*] [*reinforcement learning(DQN)*] [*backbone: LSTM*]

#### *Unsupervised learning*

  - Unsupervised Human Activity Recognition Using the Clustering Approach: A Review(Sensors, 2020)[[**paper**](https://europepmc.org/article/pmc/pmc7249206)]

  - A survey on unsupervised learning for wearable sensor-based activity recognition(Applied Soft Computing, 2022)[[**paper**](https://www.sciencedirect.com/science/article/pii/S1568494622005191)]

| [back to top](#table-of-contents) |
| --------------------------------: |

### Class Imbalanced


| [back to top](#table-of-contents) |
| --------------------------------: |

### Distribution Discrepancy


| [back to top](#table-of-contents) |
| --------------------------------: |

### User Features Privacy


| [back to top](#table-of-contents) |
| --------------------------------: |

# Datasets


# Github Repositories

 - Awesome-Human-Activity-Recognition(own by haoranD)[[link](https://github.com/haoranD/Awesome-Human-Activity-Recognition)]
 - Awesome_Human_Activity_Recognition(own by jie-su)[[link](https://github.com/Jie-su/Awesome_Human_Activity_Recognition)]
 - LSTM-Human-Activity-Recognition(own by guillaume-chevalier)[[link](https://github.com/guillaume-chevalier/LSTM-Human-Activity-Recognition)]
 - activityrecognition(own by jindongwang)[[link](https://github.com/jindongwang/activityrecognition)]
 - Human-Activity-Recognition-using-CNN(own by aqibsaeed)[[link](https://github.com/aqibsaeed/Human-Activity-Recognition-using-CNN)]
