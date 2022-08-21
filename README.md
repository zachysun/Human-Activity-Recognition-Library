# Table of Contents

 - [Table of Contents](#table-of-contents)
 - [Reference Survey Paper](#reference-survey-paper)
 - [Other Survey Paper](#other-survey-paper)
 - [Challenges and Techniques](#challenges-and-techniques)
    - [Feature Extraction](#feature-extraction)
	   - [Temporal Feature Extraction](#temporal-feature-extraction)
	   - [Multimodal Feature Extraction](#multimodal-feature-extraction)
    - [Weakly Annotation](#weakly-annotation)
	   - [Self-supervised learning](#self-supervised-learning)
	   - [Semi-supervised learning](#semi-supervised-learning)
	   - [Unsupervised learning](#unsupervised-learning)
	- [Class Imbalanced](#class-imbalanced)
	- [Transfer Learning](#transfer-learning)
	   - [Distribution Discrepancy](#distribution-discrepancy)
	   - [Zero/One/Few-Shot Learning](#zeroonefew-shot-learning)
	- [User Features Privacy](#user-features-privacy)
	- [Data Augmentation](#data-augmentation)
	- [Federated learning](#federated-learning)
 - [Datasets](#datasets)
 - [Github Repositories](#github-repositories)

# Reference Survey Paper
:star: **Deep Learning for Sensor-based Human Activity Recognition: Overview, Challenges and Opportunities (ACM Computing Surveys, 2021)** [[**paper**](https://arxiv.org/pdf/2001.07416.pdf)]

Some of papers and the main structure of this repository are inspired by this paper!!

# Other Survey Paper

  - A Survey on Deep Learning for Human Activity Recognition(ACM Computing Surveys, 2022)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3472290)]

  - Multi-sensor information fusion based on machine learning for real applications in human activity recognition: State-of-the-art and research challenges(Information Fusion, 2022)[[**paper**](https://www.sciencedirect.com/science/article/abs/pii/S1566253521002311)]

  - Deep Learning in Human Activity Recognition with Wearable Sensors: A Review on Advances(Sensors, 2022)[[**paper**](https://www.mdpi.com/1424-8220/22/4/1476)]

# Challenges and Techniques

### Feature Extraction

#### *Temporal Feature Extraction* 

  - ***Mainly Handcraft:***

  - A-Wristocracy: Deep Learning on Wrist-worn Sensing for Recognition of User Complex  Activities(BSN, 2015)[[**paper**](https://ieeexplore.ieee.org/document/7299406)]

    - [*deep learning(mlp-based)*] [*mean, variance*] [*fine-gained*] [*wrist-worn*] [*multi-sensors*]

  - Human Activity Recognition using Wearable Sensors by Deep Convolutional Neural Networks(ACM MM, 2015)[[**paper**](https://dl.acm.org/doi/abs/10.1145/2733373.2806333)]
	- [*deep learning(cnn-based)*] [*novel activity image(stack, 2D DFT)*] [*multi-sensors*]

  - TagFree Activity Identification with RFIDs(IMWUT, 2018)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3191739)]

	 - [*deep learning(cnn-lstm-based)*] [*RFID signals*] [spectrum(with time-angle)]

  - Sensing Fine-Grained Hand Activity with Smartwatches(CHI, 2019)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3290605.3300568)]

	- [*deep learning(cnn-based)*]  [*time frequency spectral(FFT)*] [*fine-gained*]

  - ***Autoencoder-Based:***

  - An ensemble of autonomous auto-encoders for human activity recognition(Neurocomputing, 2021)[[**paper**](https://www.sciencedirect.com/science/article/pii/S0925231221001454)] [[**code**](https://github.com/Keh/EAE)]

	 - [*Ensemble model*]

  - ***End to End(CNN/RNN-Based):***

  - Deep convolutional neural networks on multichannel time series for human activity recognition(AAAI, 2015)[[**paper**](https://www.aaai.org/ocs/index.php/IJCAI/IJCAI15/paper/viewFile/10710/11297)]

	 - [*end-to-end deep learning(Temporal CNN)*]

  - Convolutional Neural Networks for Human Activity Recognition using Multiple Accelerometer and Gyroscope Sensors(IJCNN, 2016)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7727224)]

	 - [*modality specific(tricks: zero padding,partial and full weight sharing)*]

  - Human activity recognition from accelerometer data using Convolutional Neural Network(BigComp, 2017)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7881728)]

	 - [*multi-scale 1D-CNN*]

  - Towards reading trackers in the wild: detecting reading activities by EOG glasses and deep neural networks(UbiComp, 2017)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3123024.3129271)]

	 - [*end-to-end deep learning(bilstm)*]

  - Ensembles of Deep LSTM Learners for Activity Recognition using Wearables(UbiComp, 2017)[[**paper**](https://arxiv.org/abs/1703.09370)]

	 - [*end-to-end deep learning(ensemble-lstm)*] [*ensemble trick: epoch-wise bagging*]

  - DeepSense: A Unified Deep Learning Framework for Time-Series Mobile Sensing Data Processing(WWW, 2017)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3038912.3052577)] [[**code**](https://github.com/yscacaca/DeepSense)]

	 - [*end-to-end deep learning(cnn, gru)*] 

  - Deep Neural Network based Human Activity Recognition for the Order Picking Process(iWOAR, 2017)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3134230.3134231)] [[**code**](https://github.com/wilfer9008/CNN_IMU)]

	 - [*end-to-end deep learning(Temporal/1D CNN)*] [*sliding window*] [*IMUs-based fusion and share weights each IMU*]

  - Deep dilated convolution on multimodality time series for human activity recognition(IJCNN, 2018)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8489540)]

	 - [*dilated cnn, lstm*]

  - Activity Recognition Using Dual-ConvLSTM Extracting Local and Global Features for SHL Recognition Challenge(UbiComp, 2018)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3267305.3267533)]

	 - [*dual-cnn-lstm(one small kernel size, one large)*] [*axis-based Fusion*]

  - Making sense of spatio-temporal preserving representations for EEG-based human intention recognition(IEEE Transactions on Cybernetics, 2020)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8698218)]

	 - [*end-to-end deep learning(cnn-lstm-based)*] [*spatio-temporal(EEG signals, EEG electrode map)*] 

  - Prototype Similarity Learning for Activity Recognition(PAKDD, 2020)[[**paper**](https://link.springer.com/chapter/10.1007/978-3-030-47426-3_50)]

	 - [*end-to-end deep learning(Temporal/1D CNN, Spatial CNN*] [*Tricks: Distance-Based Classification Module(based on prototypical network), Cross-Subject Training*] 

  - Push the Limit of Acoustic Gesture Recognition(INFOCOM, 2020)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9229520)]

	 - [*cnn-lstm*] [*acoustic data*] [*frequency transmit*]

  - Improving Deep Learning for HAR with shallow LSTMs (ISWC, 2021)[[**paper**](https://dl.acm.org/doi/10.1145/3460421.3480419)] [[**code**](https://github.com/mariusbock/dl-for-har)]

	 - [*backbone: DeepConvLSTM*]

  - Deep Neural Networks for Sensor-Based Human Activity Recognition Using Selective Kernel Convolution(TIM, 2021)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9507456)]

	 - [*novel conv: Selective Kernel Convolution*]

  - ***End to End(Transformer-Based):***

  - IF-ConvTransformer: A Framework for Human Activity Recognition Using IMU Fusion and ConvTransformer(Ubicomp, 2022)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3534584)]

	 - [*transformer-based(ConvTransformer)*] [*novel IMU fusion*]

  - Transformer Networks for Data Augmentation of Human Physical Activity Recognition(Arxiv, 2021)[[**paper**](https://arxiv.org/abs/2109.01081)] [[**code**](https://github.com/sandeep-189/data-augmentation)]

	 - [*backbone: Transformer-based*] [*augmentation tricks: GAN-based*] 

#### *Multimodal Feature Extraction*

  - ***Feature Fusion:***

  - Multi-modal convolutional neural networks for activity recognition(TMC, 2015)[[**paper**](https://ieeexplore.ieee.org/abstract/document/7379657)]

	 - [*Early Fusion(2D vector)*]

  - Human Activity Recognition Using Wearable Sensors by Deep Convolutional Neural Networks(ACM MM, 2015)[[**paper**](https://dl.acm.org/doi/abs/10.1145/2733373.2806333)]

	 - [*Early Fusion(every signal to signal)*]

  - Locomotion activity recognition using stacked denoising autoencoders(JIOT, 2018)[[**paper**](https://ieeexplore.ieee.org/abstract/document/8331081)]

	 - [*Early Fusion(1D vector)*] [*stack denoising autoencoder*]

  - Confidence-based Deep Multimodal Fusion for Activity Recognition(UbiComp, 2018)[[**paper**](https://dl.acm.org/doi/10.1145/3267305.3267522)]

	 - [*Sensor-based Fusion*] [*tricks: sensors confidence score*]

  - ***Classifier Ensemble:***

| [back to top](#table-of-contents) |
| --------------------------------: |

### Weakly Annotation 

#### *Self-supervised learning*

  - Contrastive Self-supervised Learning for Sensor-based Human Activity Recognition(IJCB, 2021)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9484410)]

	 - [*self-supervised learning*] [*contrastive learning*] [*tricks: five random augmentation*]

  - SelfHAR: Improving Human Activity Recognition through Self-training with Unlabeled Data(IMWUT, 2021)[[**paper**](https://arxiv.org/abs/2102.06073)] [[**code**](https://github.com/iantangc/SelfHAR)]

	 - [*self-supervised learning*] [*teacher-student*] [*multi-task learning*]

  - Contrastive Predictive Coding for Human Activity Recognition(IMWUT, 2021)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3463506)]

	 - [*encoder*] [*pretext: former predict latter*]

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

	 - [*Survey*]

  - A survey on unsupervised learning for wearable sensor-based activity recognition(Applied Soft Computing, 2022)[[**paper**](https://www.sciencedirect.com/science/article/pii/S1568494622005191)]

	 - [*Survey*]

  - Towards deep clustering of human activities from wearables(ISWC, 2020)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3410531.3414312)]

	 - [*Deep Clustering*] [*for pretrain: multi-task autoencoder*] [*for clustering: single layer network, cluster assignment hardening*]

| [back to top](#table-of-contents) |
| --------------------------------: |

### Class Imbalanced

| [back to top](#table-of-contents) |
| --------------------------------: |

### Transfer Learning

#### *Distribution Discrepancy*

  - ***Cross person:***

  - Cross-subject transfer learning in human activity recognition systems using generative adversarial networks(Neurocomputing, 2021)[[**paper**](https://www.sciencedirect.com/science/article/abs/pii/S0925231220316313)]

	 - [*GAN*] [*Semi-supervised learning*]

  - Latent Independent Excitation for Generalizable Sensor-based Cross-Person Activity Recognition(AAAI, 2021)[[**paper**](https://ojs.aaai.org/index.php/AAAI/article/view/17416)]

	 - [*Transfer Learning*]

  - SALIENCE: An Unsupervised User Adaptation Model for Multiple Wearable Sensors Based Human Activity Recognition(TMC, 2022)[[**paper**](https://ieeexplore.ieee.org/abstract/document/9765741)] [[**code**](https://github.com/wdkhuans/SALIENCE)]

	 - [*Unsupervised domain adaptation*] [*Transfer Learning*]

  - ***Cross multi-discrepancy:***

  - Learning Disentangled Behaviour Patterns for Wearable-based Human Activity Recognition(Ubicomp, 2022)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3517252)] [[**code**](https://github.com/Jie-su/BPD)]

	 - [*Disentangle Learning*]

  - ***Others:***

  - CALDA: Improving Multi-Source Time Series Domain Adaptation with Contrastive Adversarial Learning(TPAMI, 2021)[[**paper**](https://arxiv.org/abs/2109.14778)] [[**code**](https://github.com/floft/calda)]

	 - [*Cross HAR data and other domain data*] [*Unsupervised domain adaptation*] [*Contrastive Learning*] [*adversarial learning*]

#### *Zero/One/Few-Shot Learning*

  - Few-Shot Human Activity Recognition on Noisy Wearable Sensor Data(DASFAA, 2020)[[**paper**](https://link.springer.com/chapter/10.1007/978-3-030-59416-9_4)]

	 - [*Multiple Instance Learning*] [*Weakly supervised*] [*Prototype Networks*]

  - RF-Net: A Unified Meta-Learning Framework for RF-enabled One-Shot Human Activity Recognition(Sensys, 2020)[[**paper**](https://arxiv.org/abs/2111.04566)] [[**code**](https://github.com/di0002ya/rfnet)]

	 - [*device-free HAR(RF signal)*] [*Transfer Learning*] [*Meta Learning*] 

| [back to top](#table-of-contents) |
| --------------------------------: |

### User Features Privacy


| [back to top](#table-of-contents) |
| --------------------------------: |

### Data Augmentation

  - Transformer Networks for Data Augmentation of Human Physical Activity Recognition(Arxiv, 2021)[[**paper**](https://arxiv.org/abs/2109.01081)] [[**code**](https://github.com/sandeep-189/data-augmentation)]

	 - [*backbone: Transformer-based*] [*augmentation tricks: GAN-based*] 

# Federated learning

  - ClusterFL: a similarity-aware federated learning system for human activity recognition(MobiSys, 2021)[[**paper**](https://dl.acm.org/doi/abs/10.1145/3458864.3467681)]

| [back to top](#table-of-contents) |
| --------------------------------: |

# Datasets

  - Opportunity[[link](https://archive.ics.uci.edu/ml/datasets/opportunity+activity+recognition#:~:text=Data%20Set%20Information%3A-,The%20OPPORTUNITY%20Dataset%20for%20Human%20Activity%20Recognition%20from%20Wearable%2C%20Object,%2C%20feature%20extraction%2C%20etc)]
  - UCI HAR[[link](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones)]
  - MotionSense[[link](https://github.com/mmalekzadeh/motion-sense)]
  - PAMPA2[[link](https://archive.ics.uci.edu/ml/datasets/pamap2+physical+activity+monitoring)]

| [back to top](#table-of-contents) |
| --------------------------------: |

# Github Repositories

 - Awesome-Human-Activity-Recognition(own by haoranD)[[link](https://github.com/haoranD/Awesome-Human-Activity-Recognition)]
 - Awesome_Human_Activity_Recognition(own by jie-su)[[link](https://github.com/Jie-su/Awesome_Human_Activity_Recognition)]
 - LSTM-Human-Activity-Recognition(own by guillaume-chevalier)[[link](https://github.com/guillaume-chevalier/LSTM-Human-Activity-Recognition)]
 - activityrecognition(own by jindongwang)[[link](https://github.com/jindongwang/activityrecognition)]
 - Human-Activity-Recognition-using-CNN(own by aqibsaeed)[[link](https://github.com/aqibsaeed/Human-Activity-Recognition-using-CNN)]

| [back to top](#table-of-contents) |
| --------------------------------: |
