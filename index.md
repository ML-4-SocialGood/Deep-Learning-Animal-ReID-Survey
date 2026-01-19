---
layout: splash
permalink: /
title: "From Closed-Set Biometrics to Open-World Animal ReID: A Survey of Deep Learning for Animal Re-Identification"
header:
  overlay_color: "#44308dff"  
  overlay_filter: "0.1"
  caption: "A living repository accompanying our survey."
excerpt: "A Survey of Deep Learning for Animal Re-Identification"
---

<style>
  table {
    margin-left: auto;
    margin-right: auto;
    display: table;
  }
  
  .back-to-top {
    text-align: right;
    font-size: 0.8em;
    color: #999;     
    margin-top: 5px;
    margin-bottom: 5px; 
  }
  .back-to-top a {
    text-decoration: none;
    color: #999;
    border-bottom: 1px dotted #ccc;
  }
  .back-to-top a:hover {
    color: #44308dff;
  }
</style>

<div style="text-align: center; margin-bottom: 40px;">
  <h1>Deep Learning for Animal Re-Identification</h1>
  
  <p style="font-size: 1.1em; color: #555;">
    The official living repository for the survey:<br>
    <strong>From Closed-Set Biometrics to Open-World Animal ReID: A Survey of Deep Learning for Animal Re-Identification</strong>
  </p>

  <div style="margin: 30px auto; max-width: 800px;">
    <img src="assets/fig/publication_trend_updated.png" alt="Survey Overview" style="width: 70%; border-radius: 6px; box-shadow: 0 2px 10px rgba(0,0,0,0.1);">
    <p style="color: #888; font-size: 0.85em; margin-top: 10px;">Figure 1: Publication trend and keyword evolution in Animal ReID.</p>
  </div>

  <!-- <p>
    <a href="https://arxiv.org/abs/xxxx.xxxxx" class="btn btn--light-outline btn--small"><i class="fas fa-file-pdf"></i> Read Paper</a>
    <a href="#citation" class="btn btn--light-outline btn--small"><i class="fas fa-quote-right"></i> Cite Us</a>
  </p> -->
</div>

## 📖 Abstract
Animal ReID enables individual-level monitoring for wildlife conservation and precision agriculture, yet reliable deployment in real-world settings remains challenging.
Recent advances in foundation models have improved generalization, extending Animal ReID beyond species-specific, closed-set recognition to unseen individuals and species.
However, practical deployments in open-world environments impose multiple requirements, including robustness to non-stationary appearance distributions, accommodation of evolving populations, and recognition of observations outside known identity and species spaces.

This survey provides a systematic review of appearance-based Animal ReID from a generalization perspective, clarifying how modern deep learning paradigms have reshaped the problem landscape.
Based on an analysis of **204 representative studies**, we propose a method-centric taxonomy that organizes prior work by the mechanisms used to achieve performance gains. 
We also examine existing **evaluation protocols** through a principled zero-shot benchmark analysis.
Beyond algorithmic advances, we adopt an **ecosystem-level perspective** that spans data acquisition, model training, decision-making, and deployment feedback, discussing ethical risks, and releasing open resources, including a standardized toolkit and a living repository, to support reproducible research and long-term community use.

---


## 🚀 Released Resources
To support reproducibility and long-term community use, this repository serves as a living companion to the survey and provides:

- **📚 Paper List**: A continuously updated paper list covering representative Animal ReID research;
- **🛠️ ReWildID Toolkit**: A standardized evaluation library designed for open-world settings.  
  👉 [**Get Started with Toolkit**](./tool/)
- **🏆 Benchmark Results**: Detailed performance analysis and zero-shot baselines extracted from the survey.  
  👉 [**View Leaderboard & Analysis**](./results/)

---

<!-- ## Overview Figure
<div style="text-align: center; margin: 20px 0;">
  <img src="assets/fig/publication_trend_updated.png" alt="Survey Overview" style="width: 60%; max-width: 800px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  <p style="color: #666; font-size: 0.9em;"><em>Figure 1: Publication trend and keyword evolution in Animal ReID.</em></p>
</div> -->

### Scope and Coverage
The paper list below covers representative research on appearance-based Animal Re-Identification, spanning closed-set, open-set, and open-world settings. 
It includes works on data-centric methods, representation learning, multimodal and foundation-model-based approaches, as well as evaluation protocols and deployment considerations.
This list is curated to accompany the survey and will be continuously updated as the field evolves.

## Quick Links
**Papers sorted by year:** | [2025](#papers-2025) | [2024](#papers-2024) | [2023](#papers-2023) | [2022](#papers-2022) | [2021](#papers-2021) | [2020](#papers-2020) | [2019](#papers-2019) | [2018](#papers-2018) | [2017](#papers-2017) | [2016](#papers-2016) | [2015](#papers-2015) | [2014](#papers-2014) | [2013](#papers-2013) | [2012](#papers-2012) | [2011](#papers-2011) | [2010](#papers-2010) | [2009](#papers-2009) | [2008](#papers-2008) | [2007](#papers-2007) | [2006](#papers-2006) | [2005](#papers-2005) | [2004](#papers-2004) | [2003](#papers-2003) | [2002](#papers-2002) | [2001](#papers-2001) | [2000](#papers-2000) | [1999](#papers-1999) | [1998](#papers-1998) | [1990](#papers-1990)

## Paper List
> **Notes on Columns:**
> * **Unseen**: Indicates whether the method explicitly addresses settings with unseen identities or species (e.g., Open-Set, Zero-Shot, or Any-Animal scenarios).
> * **Venue**: We prioritize listing top-tier Computer Science / Computer Vision conferences (e.g., CVPR, ICCV, ECCV, NeurIPS). For brevity, venues for some interdisciplinary or biological journals may be leave blank.

### 2025 <a id="papers-2025"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2025 | Adapting the Re-ID Challenge for Static Sensors | Zebra | No |  |  |
| 2025 | Animal Re-Identification in Video Through Track Clustering | Koi Fish, Pig, Pigeon | No |  | [Link](https://github.com/frankmnb/Animal-ReIDentification-in-Video-through-Track-Clustering) |
| 2025 | Animal Re-Identification via Multiview Spatio-Temporal Track Clustering | Zebra | No | CVPRw |  |
| 2025 | Dynamic Multi-Behaviour, Orientation-Invariant Re-Identification of Holstein-Friesian Cattle | Cattle | No | Sensors |  |
| 2025 | Enhanced Multi-Breed Cattle Face Recognition in Complex Environments using Attention-based Deep Learning | Cattle | No |  | [Link](https://github.com/xindw211/cattle-face-recognition) |
| 2025 | GloPER: Unsupervised Animal Pattern Extraction from Local Reconstruction | Multiple | No | ICCV | [Link](https://github.com/Bob-blip-boop/GloPER) |
| 2025 | Housed Pig Identification and Tracking for Precision Livestock Farming | Pig | No |  | [Link](https://github.com/yudong888/FaroPig-Datasets) |
| 2025 | MetaWild: A Multimodal Dataset for Animal Re-Identification with Environmental Metadata | Multiple | Yes | MM | [Link](https://jim-lyz1024.github.io/MetaWild/) |
| 2025 | OpenAnimals: Revisiting Person Re-Identification for Animals Towards Better Generalization | Hyena, Leopard, Shark, Turtle | No | ICCV | [Link](https://github.com/hshustc/OpenAnimals) |
| 2025 | Re-Identification for Long-Term Tracking and Management of Health and Welfare Challenges in Pigs | Pig | No |  |  |
| 2025 | Re-Identification of Patterned Animals by Multi-Image Feature Aggregation and Geometric Similarity | Seal, Shark | No |  |  |
| 2025 | Wildlife Target Re-Identification Using Self-supervised Learning in Non-Urban Settings | Multiple | Yes |  | [Link](https://github.com/pxpana/) |
| 2025 | WildlifeReID-10k: Wildlife Re-Identification Dataset with 10k Individual Animals | Multiple | No | CVPRw | [Link](https://www.kaggle.com/datasets/wildlifedatasets/wildlifereid-10k) |

<div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2024 <a id="papers-2024"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2024 | AI-Enhanced Real-Time Cattle Identification System Through Tracking Across Various Environments | Cattle | No |  |  |
| 2024 | Biometric Identification of Dairy Cows via Real-Time Facial Recognition | Cattle | No |  |  |
| 2024 | Cattle Identification based on Multiple Feature Decision Layer Fusion | Cattle | No |  |  |
| 2024 | Exploiting Facial Side Similarities to Improve AI-Driven Sea Turtle Photo-Identification Systems | Turtle | No |  | [Link](https://github.com/sadda/sides-matching) |
| 2024 | NORPPA: NOvel Ringed seal re-identification by Pelage Pattern Aggregation | Seal | No | WACVw |  |
| 2024 | SeaTurtleID2022: A Long-Span Dataset for Reliable Sea Turtle Re-Identification | Turtle | No | WACV | [Link](https://github.com/WildlifeDatasets/wildlife-datasets/tree/main) |
| 2024 | Species-Agnostic Patterned Animal Re-identification by Aggregating Deep Local Features | Seal, Shark | Yes | IJCV | [Link](https://github.com/kwadraterry/Norppa) |
| 2024 | WildFusion: Individual Animal Identification with Calibrated Similarity Fusion | Multiple | No | ECCVw | [Link](https://github.com/WildlifeDatasets/wildlife-tools) |
| 2024 | WildlifeDatasets: An Open-Source Toolkit for Animal Re-Identification | Multiple | Yes | WACV | [Link](https://github.com/WildlifeDatasets/wildlife-datasets) |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2023 <a id="papers-2023"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2023 | A Contrastive Learning Approach for Individual Re-Identification in a Wild Fish Population | Fish | No |  | [Link](https://github.com/orilan93/SiameseFish) |
| 2023 | A Deep Learning Approach to Photo–Identification Demonstrates High Performance on Two Dozen Cetacean Species | Dolphin, Whale | No |  | [Link](https://github.com/knshnb/kaggle-happywhale-1st-place) |
| 2023 | A Purely Visual Re-ID Approach for Bumblebees | Bee | No |  |  |
| 2023 | An Intelligence Cattle Reidentification System Over Transport by Siamese Neural Networks and YOLO | Cattle | No |  |  |
| 2023 | Animal Re-Identification Algorithm for Posture Diversity | Dog, Tiger | No | ICASSP | [Link](https://github.com/hezhimin7028/MPFNet) |
| 2023 | Finding Nemo’s Giant Cousin: Keypoint Matching for Robust Re-Identification of Giant Sunfish | Giant Sunfish | No |  |  |
| 2023 | Giant Panda Identification | Panda | No | TIP | [Link](https://github.com/iPandaDateset/iPanda-50) |
| 2023 | Individual Identification of Endangered Amphibians using Deep Learning and Smartphone Images: Case Study of the Japanese Giant Salamander | Salamander | No |  |  |
| 2023 | PolarBearVidID: A Video-Based Re-Identification Benchmark Dataset for Polar Bears | Polar Bear | No |  | [Link](https://doi.org/10.5281/zenodo.7564528) |
| 2023 | Re-Identification of Fish Individuals of Undulate Skate via Deep Learning within a Few-Shot Context | Undulate Skate | No |  | [Link](https://github.com/nuriagomv/Application-of-Deep-Learning-techniques-for-the-photo-identification-of-fish-individuals) |
| 2023 | Re-identification of Saimaa Ringed Seals from Image Sequences | Seal | No |  | [Link](https://github.com/kwadraterry/Norppa) |
| 2023 | Toward Re-Identifying Any Animal | Giraffe, Seal, Tiger, Zebra | Yes | NeurIPS | [Link](https://github.com/JiaoBL1234/wildlife) |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2022 <a id="papers-2022"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2022 | Automated Blue Whale Photo-Identification Using Local Feature Matching | Whale | No | ICPRw |  |
| 2022 | Feasibility of Using Convolutional Neural Networks for Individual-Identification of Wild Asian Elephants | Elephant | No |  | [Link](https://github.com/AsithaIndrajith/cnn-ele) |
| 2022 | Fish Face Identification Based on Rotated Object Detection: Dataset and Exploration | Fish | No |  |  |
| 2022 | Flukebook: An Open-Source AI Platform for Cetacean Photo Identification | Multiple | No |  | [Link](https://github.com/WildMeOrg/Wildbook) |
| 2022 | Matching Individual Ladoga Ringed Seals across Short-Term Image Sequences | Seal | No |  |  |
| 2022 | Rise of the Machines: Best Practices and Experimental Evaluation of Computer-Assisted Dorsal Fin Image Matching Systems for Bottlenose Dolphins | Dolphin | No |  | [Link](https://github.com/haimeh/finFindR) |
| 2022 | SealID: Saimaa Ringed Seal Re-Identification Dataset | Seal | No | Sensors | [Link](https://github.com/kwadraterry/Norppa) |
| 2022 | Similarity Learning Networks for Animal Individual Re-Identification: An Ecological Perspective | Fly, Primate, Tiger, Whale | No |  |  |
| 2022 | Towards Re-Identification for Long-Term Tracking of Group Housed Pigs | Pig | No |  |  |
| 2022 | Wild Terrestrial Animal Re-Identification Based on an Improved Locally Aware Transformer with a Cross-Attention Mechanism | Multiple | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2021 <a id="papers-2021"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2021 | Advanced Image Recognition: A Fully Automated, High-Accuracy Photo-Identification Matching System for Humpback Whales | Whale | No |  | [Link](https://happywhale.com/home) |
| 2021 | Automated Individual Cattle Identification Using Video Data: A Unified Deep Learning Architecture Approach | Cattle | No |  | [Link](https://github.com/yongliang-qiao/beefidentify) |
| 2021 | Comparing Class-Aware and Pairwise Loss Functions for Deep Metric Learning in Wildlife Re-Identification | Lion, Nyala, Panda, Primate, Tiger, Zebra | No | Sensors | [Link](https://github.com/tvanzyl/wildlife_reidentification) |
| 2021 | EDEN: Deep Feature Distribution Pooling for Saimaa Ringed Seals Pattern Matching | Seal | No |  |  |
| 2021 | ElephantBook: A Semi-Automated Human-in-the-Loop System for Elephant Re-Identification | Elephant | No |  |  |
| 2021 | Estimating Population Abundance of Burying Beetles Using Photo-Identification and Mark-Recapture Methods | Insect | No |  |  |
| 2021 | FIN-PRINT: A Fully-Automated Multi-Stage Deep-Learning-based Framework for the Individual Recognition of Killer Whales | Whale | No |  | [Link](https://github.com/ChristianBergler/FIN-PRINT) |
| 2021 | HotSpotter: Using a Computer-Driven Photo-ID Application to Identify Sea Turtles | Turtle |  |  |  |
| 2021 | Individual Detection and Tracking of Group Housed Pigs in Their Home Pen Using Computer Vision | Pig | No |  |  |
| 2021 | Keypoint-Aligned Embeddings for Image Retrieval and Re-Identification | Bird | No | WACV |  |
| 2021 | Robust Re-identification of Manta Rays from Natural Markings by Learning Pose Invariant Embeddings | Manta Ray, Whale | No |  |  |
| 2021 | Visual Identification of Individual Holstein-Friesian Cattle via Deep Metric Learning | Cattle | No |  | [Link](https://github.com/dataset-ninja/opencows2020) |
| 2021 | YakReID-103: A Benchmark for Yak Re-Identification | Yak | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2020 <a id="papers-2020"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2020 | A Study on Giant Panda Recognition based on Images of a Large Proportion of Captive Pandas | Panda | No |  |  |
| 2020 | ATRW: A Benchmark for Amur Tiger Re-identification in the Wild | Tiger | No | MM | [Link](https://cvwc2019.github.io/challenge.html) |
| 2020 | Deep Learning-based Methods for Individual Recognition in Small Birds | Bird | No |  | [Link](https://github.com/AndreCFerreira/Bird_individualID) |
| 2020 | Detection Features as Attention (DeFAt): A Keypoint-Free Approach to Amur Tiger Re-Identification | Tiger | No |  |  |
| 2020 | Extracting Identifying Contours for African Elephants and Humpback Whales using a Learned Appearance Model | Elephant, Whale | No | WACV |  |
| 2020 | Identifying Individual Jaguars and Ocelots via Pattern‐Recognition Software: Comparing HotSpotter and Wild‐ID | Jaguar, Ocelot | No |  |  |
| 2020 | Learning Landmark Guided Embeddings for Animal Re-identification | Manta Ray | No | WACVw |  |
| 2020 | Re-Identification of Zebrafish using Metric Learning | Zebrafish | No | WACVw | [Link](https://bitbucket.org/aauvap/zebrafish-re-identification/src/master/) |
| 2020 | Revisiting Animal Photo-Identification using Deep Metric Learning and Network Analysis | Giraffe | No |  | [Link](https://plmlab.math.cnrs.fr/vmiele/animal-reid/) |
| 2020 | Siamese Network Based Pelage Pattern Matching for Ringed Seal Re-identification | Seal | No | WACVw |  |
| 2020 | Similarity Learning Networks for Animal Individual Re-Identification - Beyond the Capabilities of a Human Observer | Fly, Primate, Tiger, Whale | No | WACVw |  |
| 2020 | System for Elephant Ear-pattern Knowledge (SEEK) to Identify Individual African Elephants | Elephant | No |  |  |
| 2020 | Unique Animal Identification using Deep Transfer Learning For Data Fusion in Siamese Networks | Nyala, Zebra | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2019 <a id="papers-2019"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2019 | A Hybrid Approach for Tiger Re-Identification | Tiger | No | ICCVw |  |
| 2019 | A SIFT-based Software System for the Photo-Identification of the Risso's Dolphin | Dolphin | No |  |  |
| 2019 | Aerial Animal Biometrics: Individual Friesian Cattle Recovery and Visual Identification via an Autonomous UAV with Onboard Deep Inference | Cattle | No | IROS |  |
| 2019 | Automatic Individual Pig Detection and Tracking in Pig Farms | Pig | No | Sensors |  |
| 2019 | Chimpanzee Face Recognition from Videos in the Wild using Deep Learning | Primate | No |  |  |
| 2019 | Classification and Re-Identification of Fruit Fly Individuals Across Days with Convolutional Neural Networks | Fly | No | WACV | [Link](https://github.com/uoguelph-mlrg/fly_re_identification) |
| 2019 | Distinguishing Individual Red Pandas from Their Faces | Red Panda | No |  |  |
| 2019 | ELPephants: A Fine-Grained Dataset for Elephant Re-Identification | Elephant | No | ICCVw |  |
| 2019 | Image-Based Recognition of Individual Trouts in the Wild | Brown Trout | No |  |  |
| 2019 | Individual Identification of Holstein Dairy Cows based on Detecting and Matching Feature Points in Body Images | Cattle | No |  |  |
| 2019 | Part-Pose Guided Amur Tiger Re-Identification | Tiger | No | ICCVw | [Link](https://github.com/LcenArthas/CVWC2019-Amur-Tiger-Re-ID) |
| 2019 | Pose-Guided Complementary Features Learning for Amur Tiger Re-Identification | Tiger | No | ICCVw |  |
| 2019 | Primate Face Identification in the Wild | Primate | No | PRICAI |  |
| 2019 | Where to Spot: Individual Identification of Leopard Cats (Prionailurus Bengalensis Euptilurus) in South Korea | Cat | No |  |  |
| 2019 | idtracker.ai: Tracking all Individuals in Small or Large Collectives of Unmarked Animals | Agnostic | No |  | [Link](https://gitlab.com/polavieja_lab/idtrackerai) |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2018 <a id="papers-2018"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2018 | A Hybrid Rolling Skew Histogram-Neural Network Approach to Dairy Cow Identification System | Cattle | No |  |  |
| 2018 | Applying Deep Learning to Right Whale Photo Identiﬁcation | Whale | No |  | [Link](https://github.com/robibok/whales) |
| 2018 | Automated Face Recognition of Rhesus Macaques | Primate | No |  | [Link](https://github.com/clwitham/MacaqueFaces) |
| 2018 | Cow Individual Identification Based on Convolutional Neural Network | Cattle | No |  |  |
| 2018 | Deep Learning Framework for Recognition of Cattle using Muzzle Point Image Pattern | Cattle | No |  |  |
| 2018 | DolFin: An Innovative Digital Platform for Studying Risso’s Dolphins in the Northern Ionian Sea (North-Eastern Central Mediterranean) | Dolphin | No |  |  |
| 2018 | Face Recognition: Primates in the Wild | Primate | No |  | [Link](https://github.com/ronny3050/PrimateFaceRecognition) |
| 2018 | Identification of Saimaa Ringed Seal Individuals Using Transfer Learning | Seal | No |  |  |
| 2018 | Image Technology based Cow Identification System Using Deep Learning | Cattle | No |  |  |
| 2018 | Individual Common Dolphin Identification via Metric Embedding Learning | Dolphin | No | IVCNZ |  |
| 2018 | Individual Minke Whale Recognition Using Deep Learning Convolutional Neural Networks | Whale | No |  |  |
| 2018 | Multi-views Embedding for Cattle Re-identification | Cattle | No |  |  |
| 2018 | Towards Automatic Identification of Elephants in the Wild | Elephant | No | IJCAIw |  |
| 2018 | Towards On-Farm Pig Face Recognition using Convolutional Neural Networks | Pig | No |  |  |
| 2018 | Tracking and Re-Identification System for Multiple Laboratory Animals | Ants, Sowbugs, Zebrafish | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2017 <a id="papers-2017"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2017 | Animal Population Censusing at Scale with Citizen Science and Photographic Identification | Giraffe, Zebra | No | AAAI |  |
| 2017 | Automated Visual Fin Identification of Individual Great White Sharks | Shark | No | IJCV |  |
| 2017 | Automatic Detection and Recognition of Individuals in Patterned Species | Jaguar, Tiger, Zebra | No | ECML |  |
| 2017 | Automatic Individual Identification of Holstein Dairy Cows using Tailhead Images | Cattle | No |  |  |
| 2017 | Automatic Individual Identification of Saimaa Ringed Seals | Seal | No |  |  |
| 2017 | Comparison of Photo‐Matching Algorithms Commonly used for Photographic Capture–Recapture Studies | Salamander, Toad |  |  |  |
| 2017 | Integral Curvature Representation and Matching Algorithms for Identification of Dolphins and Whales | Dolphin, Whale | No | ICCVw |  |
| 2017 | LemurFaceID: A Face Recognition System to Facilitate Individual Identification of Lemurs | Primate | No |  | [Link](https://biometrics.cse.msu.edu/Publications/Databases/MSU_LemurFaceID/) |
| 2017 | Muzzle Point Pattern based Techniques For Individual Cattle Identification | Cattle | No |  |  |
| 2017 | Photo-id of Blue Whale by Means of the Dorsal Fin using Clustering Algorithms and Color Local Complexity Estimation for Mobile Devices | Whale | No |  |  |
| 2017 | Towards Automated Visual Monitoring of Individual Gorillas in the Wild | Primate | No | ICCVw |  |
| 2017 | Visual Localisation and Individual Identification of Holstein Friesian Cattle via Deep Learning | Cattle | No | ICCVw |  |
| 2017 | Where is My Puppy? Retrieving Lost Dogs by Facial Features | Dog | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2016 <a id="papers-2016"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2016 | A Fast Cattle Recognition System using Smart Devices | Cattle | No |  |  |
| 2016 | Automatic Individual Holstein Friesian Cattle Identification via Selective Local Coat Pattern Matching in RGB-D Imagery | Cattle | No | ICIP |  |
| 2016 | Biometric Cattle Identification Approach based on Weber’s Local Descriptor and AdaBoost Classifier | Cattle | No |  |  |
| 2016 | Chimpanzee Faces in the Wild: Log-Euclidean CNNs for Predicting Identities and Attributes of Primates | Primate | No | GCPR | [Link](https://github.com/cvjena) |
| 2016 | Computer-assisted Recognition Of Dolphin Individuals Using Dorsal Fin Pigmentations | Dolphin | No |  |  |
| 2016 | Face Recognition of Cattle: Can it be Done? | Cattle | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2015 <a id="papers-2015"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2015 | Face Recognition for Cattle | Cattle | No |  |  |
| 2015 | Muzzle-Based Cattle Identification Using Speed up Robust Feature Approach | Cattle | No |  |  |
| 2015 | Segmentation of Saimaa Ringed Seals for Identification Purposes | Seal | No |  |  |
| 2015 | Sloop: A Pattern Retrieval Engine for Individual Animal Identification | Salamander, Shark | No | PR |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2014 <a id="papers-2014"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2014 | A New Cow Identification System based on Iris Analysis and Recognition | Cattle | No |  |  |
| 2014 | Automated Marine Turtle Photograph Identification using Artificial Neural Networks, with Application to Green Turtles | Turtle | No |  |  |
| 2014 | Cattle Identification Using Muzzle Print Images Based on Texture Features Approach | Cattle | No |  |  |
| 2014 | Genetic Fingerprinting Proves Cross-Correlated Automatic Photo-Identification of Individuals as Highly Efficient in Large Capture–Mark–Recapture Studies | Salamander | No |  |  |
| 2014 | Pattern Recognition Algorithm Reveals How Birds Evolve Individual Egg Pattern Signatures | Bird Egg | No | NC | [Link](https://www.naturepatternmatch.org/) |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2013 <a id="papers-2013"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2013 | A Robust Cattle Identification Scheme Using Muzzle Print Images | Cattle | No |  |  |
| 2013 | An Automated Chimpanzee Identification System Using Face Detection and Recognition | Primate | No |  |  |
| 2013 | Beef Cattle Identification based on Muzzle Pattern using a Matching Refinement Technique in the SIFT Method | Cattle | No |  |  |
| 2013 | Cattle Face Recognition Using Local Binary Pattern Descriptor | Cattle | No |  |  |
| 2013 | Computer-Assisted Photo Identification Outperforms Visible Implant Elastomers in an Endangered Salamander | Salamander | No |  |  |
| 2013 | Dolphin Fin Pose Correction using ICP in Application to Photo-Identification | Dolphin | No |  |  |
| 2013 | HotSpotter - Patterned Species Instance Recognition | Zebra | No | WACV |  |
| 2013 | Manta Matcher: Automated Photographic Identification of Manta Rays using Keypoint Features | Manta Ray | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2012 <a id="papers-2012"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2012 | A Computer-assisted System for Photographic Mark–Recapture Analysis | Giraffe | No |  |  |
| 2012 | A New Classification Method to Simplify Blue Whale Photo-Identification Technique | Whale | No |  |  |
| 2012 | A Registration Algorithm for the Identification of Individual Parrots Based on the Patterns of Filing Ridges on the Internal Surface of Their Upper Bill Tip | Parrot | No |  |  |
| 2012 | Automatic Cattle Identification based on Muzzle Photo Using Speed-Up Robust Features Approach | Cattle | No |  |  |
| 2012 | Detection and Identification of Chimpanzee Faces in the Wild | Primate | No |  |  |
| 2012 | Identification of Great Apes Using Gabor Features and Locality Preserving Projections | Primate | No |  |  |
| 2012 | Towards Automated Visual Identification of Primates Using Face Recognition | Primate | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2011 <a id="papers-2011"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2011 | Biometric Animal Databases from Field Photographs: Identification of Individual Zebra in the Wild | Zebra | No | ICMR |  |
| 2011 | Identification of Great Apes Using Face Recognition | Primate | No |  |  |
| 2011 | ZOOMETRICS – Biometric Identification of Wildlife Using Natural Body Marks | Salamander | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2010 <a id="papers-2010"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2010 | Computer-Aided Photo-Identification System with an Application to Polar Bears based on Whisker Spot Patterns | Polar Bear | No |  |  |
| 2010 | Spotting the Difference: Towards Fully-Automated Population Monitoring of African Penguins Spheniscus Demersus | Penguin | No |  |  |
| 2010 | Vision Based Elephant Recognition for Management and Conservation | Elephant | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2009 <a id="papers-2009"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2009 | Estimating Population Size, Structure, and Residency Time for Whale Sharks Rhincodon Typus Through Collaborative Photo-Identification | Shark | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2008 <a id="papers-2008"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2008 | Identifying Elephant Photos by Multi-Curve Matching | Elephant | No | PR |  |
| 2008 | Photographic Identification of Sea Turtles: Method Description and Validation, with an Estimation of Tag Loss | Turtle | No |  |  |
| 2008 | Towards Automatic Model-Based Identification of Individual Sharp-Tailed Snakes from Natural Body Markings | Snake | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2007 <a id="papers-2007"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2007 | A Computer-Aided Program for Pattern-Matching of Natural Marks on the Spotted Raggedtooth Shark Carcharias Taurus | Shark | No |  | [Link](https://reijns.com/i3s/) |
| 2007 | Individual Animal Identification using Visual Biometrics on Deformable Coat-Patterns | Penguin | No |  |  |
| 2007 | Multi-Scale Features for Identifying Individuals in Large Biological Databases: An Application of Pattern Recognition Technology to the Marbled Salamander | Salamander | No |  |  |
| 2007 | Spot the Match – Wildlife Photo-Identification using Information Theory | Shark | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2006 <a id="papers-2006"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2006 | Iterative 3-D Pose Correction and Content-Based Image Retrieval for Dorsal Fin Recognition | Dolphin | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2005 <a id="papers-2005"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2005 | An Affine Invariant Curve Matching Method for Photo-Identification of Marine Mammals | Dolphin, Sea Lion, Whale | No | PR |  |
| 2005 | An Astronomical Pattern-Matching Algorithm for Computer-Aided Identification of Whale Sharks | Whale |  |  |  |
| 2005 | Recognition of Individual Holstein Cattle by Imaging Body Patterns | Cattle | No |  |  |
| 2005 | Saliency Detection and Matching for Photo Identification of Humpback Whales | Whale | No |  |  |
| 2005 | The Identification of Japanese Black Cattle by Their Faces | Cattle | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2004 <a id="papers-2004"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2004 | Automated Visual Recognition of Individual African Penguins | Penguin | No |  |  |
| 2004 | On Recognizing Individual Salamanders | Salamander | No | ACCV |  |
| 2004 | Towards Computer-assisted Photo-Identification of Humpback Whales | Whale | No | ICIP |  |
| 2004 | Zernike Moment Invariants Based Photo-identification Using Fisher Discriminant Model | Whale | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2003 <a id="papers-2003"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2003 | Photo-Identification of Humpback and Gray Whales Using Affine Moment Invariants | Whale | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2002 <a id="papers-2002"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2002 | Finscan: a Computer System for Photographic Identification of Marine Animals | Dolphin, Shark, Whale |  |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2001 <a id="papers-2001"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2001 | A Note on a Prototype System for Simple Computer-Assisted Matching of Individually Identified Southern Right Whales | Whale | No |  |  |
| 2001 | Computer-aided Photogram Matching in Studies Using Individual Identification: An Example from Serengeti Cheetahs | Cheetah | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 2000 <a id="papers-2000"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 2000 | A String Matching Computer-Assisted System for Dolphin Photo Identification | Dolphin | No |  |  |
| 2000 | Finding Similar Trailing Edges in Large Collections of Photographs of Sperm Whales | Whale | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 1999 <a id="papers-1999"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 1999 | Assisting Manual Dolphin Identification by Computer Extraction of Dorsal Ratio | Dolphin | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 1998 <a id="papers-1998"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 1998 | Identification of Individual Sperm Whales by Wavelet Transform of the Trailing Edge of the Flukes | Whale | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---

### 1990 <a id="papers-1990"></a>

| Year | Title | Species | Unseen | Venue | Code |
|---|---|---|---|---|---|
| 1990 | Computer Aided Matching of Natural Markings: A Prototype System for Grey Seals | Seal | No |  |  |
| 1990 | Computer Assisted Individual Identification of Sperm Whale Flukes | Whale | No |  |  |
| 1990 | Computer Assisted Photo-Identification of Humpback Whales | Whale | No |  |  |

 <div class="back-to-top"><a href="#quick-links">↑ Back to top</a></div>

---


