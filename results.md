---
layout: splash
title: "Benchmark Results"
permalink: /results/
header:
  overlay_filter: 0.1
  overlay_color: "#44308dff"
  caption: "Benchmark Analysis of Animal Re-Identification (Animal ReID)"
excerpt: "Detailed zero-shot results of Foundation Models (CLIP, SigLIP) across diverse Animal ReID datasets."
---

<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

<style>
  .table-hover tbody tr:hover {
    background-color: #f5f5f5;
  }
  .table-striped tbody tr:nth-of-type(odd) {
    background-color: rgba(0,0,0,.02);
  }
  .dataset-name {
    font-weight: bold; 
    color: #44308d;
    vertical-align: middle !important;
    background-color: #fff !important;
  }
  .metric-val {
    vertical-align: middle !important;
    text-align: center;
  }

  .table-wrapper {
    width: 100%;
    overflow-x: auto; 
    margin-bottom: 1em;
    text-align: center;   
  }

  table {
    margin-left: auto;
    margin-right: auto;
    border-collapse: collapse;
    width: auto !important; 
    max-width: 100%;
    display: table;
  }

  .math-block {
    background: #fdfdfd;
    border: 1px solid #eee;
    padding: 15px;
    border-radius: 8px;
    margin: 20px 0;
    overflow-x: auto;
  }
</style>

## 🏆 Zero-Shot Evaluation Results
We report zero-shot evaluation results on representative Animal Re-Identification (Animal ReID) benchmarks.
All models are evaluated without dataset-specific fine-tuning.
In addition to standard retrieval metrics, we report **Rand R1** and the **Normalized Gain Rate (NGR)** to explicitly account for dataset structure and chance-level performance.

## 📊 Evaluation & Analysis Framework

Motivated by the evaluation analysis in the preceding section of our survey, we examine a total of **45 Animal ReID benchmarks** and analyze their shared limitations in capturing the generalization challenges inherent to the task. The datasets used in this analysis are curated from the [**WildlifeDatasets**](https://github.com/WildlifeDatasets/wildlife-datasets) library, covering a wide spectrum of species and capture conditions.

While these benchmarks cover a wide range of scenarios, our analysis reveals that many of them exhibit increasing saturation under modern foundation models, limiting their ability to meaningfully discriminate generalization capability when assessed using conventional retrieval metrics alone.


### The Normalized Gain Rate (NGR)

Beyond identifying limitations in existing protocols, we introduce the **Normalized Gain Rate (NGR)** as a principled measure of benchmark difficulty. This metric enables a systematic assessment of whether existing benchmarks remain sufficiently challenging to meaningfully discriminate among modern foundation models.

The NGR adjusts the standard Rank-1 accuracy by accounting for the **structural bias** (random chance) inherent in each dataset's gallery composition. It is defined as:

$$
\mathrm{NGR} = \frac{R_1^{\mathrm{ZS}} - R_1^{\mathrm{rand}}}{100 - R_1^{\mathrm{rand}}}
$$

Where $$R_1^{\mathrm{ZS}}$$ represents the Zero-Shot Rank-1 accuracy, and $$R_1^{\mathrm{rand}}$$ denotes the expected random accuracy, calculated as:

$$
R_1^{\mathrm{rand}} = 100 \cdot \mathbb{E}_{x^q} \left[ \frac{n_+(x^q)}{|\mathcal{G}|} \right]
$$

Here, $$n_+(x^q)$$ is the number of positive matches for query $$x^q$$ in the gallery, and $$\lvert \mathcal{G} \rvert$$ is the gallery size. An NGR close to 1 indicates the model has solved the task, while an NGR close to 0 (or negative) implies performance is indistinguishable from (or worse than) random guessing.

---

### Reported Metrics
  - **mAP / Rank-1/5/10**: Standard retrieval metrics.
  - **Rand R1**: Expected random rank-1 accuracy induced by gallery structure.
  - **NGR**: *Normalized Gain Rate*, measuring benchmark saturation.

---

<div class="table-wrapper" style="overflow-x: auto;">
    <table class="table table-bordered table-hover">
    <thead class="thead-light">
        <tr style="background-color: #f8f9fa;">
        <th style="text-align: left; vertical-align: middle; width: 20%;">Dataset</th>
        <th style="text-align: center; vertical-align: middle; width: 10%;">Metric</th>
        <th style="text-align: center; vertical-align: middle;">CLIP-ZS (%)</th>
        <th style="text-align: center; vertical-align: middle;">SIGLIP-ZS (%)</th>
        <th style="text-align: center; vertical-align: middle;">Rand R1 (%)</th>
        <th style="text-align: center; vertical-align: middle;">NGR</th>
        </tr>
    </thead>
    <tbody>
        <tr>
        <td rowspan="4" class="dataset-name">FriesianCattle2017</td>
        <td>mAP</td>
        <td class="metric-val">64.41</td>
        <td class="metric-val">60.72</td>
        <td rowspan="4" class="metric-val">10.66</td>
        <td rowspan="4" class="metric-val">0.76</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">78.82</td>
        <td class="metric-val">71.76</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">94.12</td>
        <td class="metric-val">92.94</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">100.00</td>
        <td class="metric-val">98.82</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">MPDD</td>
        <td>mAP</td>
        <td class="metric-val">53.55</td>
        <td class="metric-val">53.58</td>
        <td rowspan="4" class="metric-val">1.08</td>
        <td rowspan="4" class="metric-val">0.73</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">73.08</td>
        <td class="metric-val">69.23</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">86.54</td>
        <td class="metric-val">87.50</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">95.19</td>
        <td class="metric-val">89.42</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">Lion</td>
        <td>mAP</td>
        <td class="metric-val">13.69</td>
        <td class="metric-val">13.51</td>
        <td rowspan="4" class="metric-val">5.40</td>
        <td rowspan="4" class="metric-val">0.10</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">14.75</td>
        <td class="metric-val">18.03</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">44.26</td>
        <td class="metric-val">32.79</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">70.49</td>
        <td class="metric-val">52.46</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">Tiger (ATRW)</td>
        <td>mAP</td>
        <td class="metric-val">40.48</td>
        <td class="metric-val">39.37</td>
        <td rowspan="4" class="metric-val">4.33</td>
        <td rowspan="4" class="metric-val">0.82</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">83.02</td>
        <td class="metric-val">76.89</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">94.10</td>
        <td class="metric-val">94.10</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">96.70</td>
        <td class="metric-val">96.70</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">AmvrakikosTurtles</td>
        <td>mAP</td>
        <td class="metric-val">15.84</td>
        <td class="metric-val">20.33</td>
        <td rowspan="4" class="metric-val">5.00</td>
        <td rowspan="4" class="metric-val">0.16</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">20.00</td>
        <td class="metric-val">20.00</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">30.00</td>
        <td class="metric-val">50.00</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">40.00</td>
        <td class="metric-val">65.00</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">AAUZebraFish</td>
        <td>mAP</td>
        <td class="metric-val">68.31</td>
        <td class="metric-val">71.69</td>
        <td rowspan="4" class="metric-val">50.02</td>
        <td rowspan="4" class="metric-val">1.00</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">100.00</td>
        <td class="metric-val">97.56</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">100.00</td>
        <td class="metric-val">100.00</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">100.00</td>
        <td class="metric-val">100.00</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">AerialCattle2017</td>
        <td>mAP</td>
        <td class="metric-val">46.24</td>
        <td class="metric-val">39.65</td>
        <td rowspan="4" class="metric-val">16.49</td>
        <td rowspan="4" class="metric-val">0.97</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">97.16</td>
        <td class="metric-val">96.59</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">98.58</td>
        <td class="metric-val">98.58</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">98.58</td>
        <td class="metric-val">99.72</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">BelugaID</td>
        <td>mAP</td>
        <td class="metric-val">15.18</td>
        <td class="metric-val">14.43</td>
        <td rowspan="4" class="metric-val">0.64</td>
        <td rowspan="4" class="metric-val">0.14</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">14.94</td>
        <td class="metric-val">14.07</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">26.86</td>
        <td class="metric-val">24.83</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">36.45</td>
        <td class="metric-val">31.22</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">BirdIndividualID</td>
        <td>mAP</td>
        <td class="metric-val">36.55</td>
        <td class="metric-val">33.31</td>
        <td rowspan="4" class="metric-val">11.15</td>
        <td rowspan="4" class="metric-val">0.49</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">54.92</td>
        <td class="metric-val">57.51</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">84.97</td>
        <td class="metric-val">85.49</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">96.89</td>
        <td class="metric-val">94.30</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">CatIndividualImages</td>
        <td>mAP</td>
        <td class="metric-val">66.72</td>
        <td class="metric-val">72.93</td>
        <td rowspan="4" class="metric-val">0.79</td>
        <td rowspan="4" class="metric-val">0.92</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">91.75</td>
        <td class="metric-val">92.95</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">96.67</td>
        <td class="metric-val">97.21</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">97.92</td>
        <td class="metric-val">97.82</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">Chicks4FreeID</td>
        <td>mAP</td>
        <td class="metric-val">44.76</td>
        <td class="metric-val">43.16</td>
        <td rowspan="4" class="metric-val">5.99</td>
        <td rowspan="4" class="metric-val">0.72</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">73.58</td>
        <td class="metric-val">72.33</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">94.97</td>
        <td class="metric-val">91.82</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">95.60</td>
        <td class="metric-val">95.60</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">CowDataset</td>
        <td>mAP</td>
        <td class="metric-val">65.43</td>
        <td class="metric-val">61.83</td>
        <td rowspan="4" class="metric-val">20.28</td>
        <td rowspan="4" class="metric-val">0.96</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">97.14</td>
        <td class="metric-val">98.57</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">99.52</td>
        <td class="metric-val">100.00</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">100.00</td>
        <td class="metric-val">100.00</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">Cows2021</td>
        <td>mAP</td>
        <td class="metric-val">12.55</td>
        <td class="metric-val">11.17</td>
        <td rowspan="4" class="metric-val">1.73</td>
        <td rowspan="4" class="metric-val">0.41</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">41.95</td>
        <td class="metric-val">38.04</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">65.39</td>
        <td class="metric-val">61.72</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">77.35</td>
        <td class="metric-val">73.68</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">CTai</td>
        <td>mAP</td>
        <td class="metric-val">20.36</td>
        <td class="metric-val">19.57</td>
        <td rowspan="4" class="metric-val">7.74</td>
        <td rowspan="4" class="metric-val">0.55</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">58.82</td>
        <td class="metric-val">54.95</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">83.64</td>
        <td class="metric-val">81.64</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">91.10</td>
        <td class="metric-val">89.10</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">CZoo</td>
        <td>mAP</td>
        <td class="metric-val">22.61</td>
        <td class="metric-val">20.94</td>
        <td rowspan="4" class="metric-val">10.32</td>
        <td rowspan="4" class="metric-val">0.59</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">62.80</td>
        <td class="metric-val">59.73</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">87.37</td>
        <td class="metric-val">83.28</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">93.52</td>
        <td class="metric-val">90.44</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">DogFaceNet</td>
        <td>mAP</td>
        <td class="metric-val">39.40</td>
        <td class="metric-val">49.20</td>
        <td rowspan="4" class="metric-val">0.27</td>
        <td rowspan="4" class="metric-val">0.66</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">66.50</td>
        <td class="metric-val">73.75</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">81.00</td>
        <td class="metric-val">87.95</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">85.50</td>
        <td class="metric-val">90.81</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">FriesianCattle2015</td>
        <td>mAP</td>
        <td class="metric-val">61.18</td>
        <td class="metric-val">71.36</td>
        <td rowspan="4" class="metric-val">11.10</td>
        <td rowspan="4" class="metric-val">0.69</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">72.73</td>
        <td class="metric-val">90.91</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">90.91</td>
        <td class="metric-val">95.45</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">90.91</td>
        <td class="metric-val">95.45</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">Giraffes</td>
        <td>mAP</td>
        <td class="metric-val">22.91</td>
        <td class="metric-val">23.55</td>
        <td rowspan="4" class="metric-val">1.77</td>
        <td rowspan="4" class="metric-val">0.46</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">46.58</td>
        <td class="metric-val">45.34</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">67.70</td>
        <td class="metric-val">66.46</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">75.16</td>
        <td class="metric-val">72.05</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">GiraffeZebraID</td>
        <td>mAP</td>
        <td class="metric-val">17.92</td>
        <td class="metric-val">18.97</td>
        <td rowspan="4" class="metric-val">0.24</td>
        <td rowspan="4" class="metric-val">0.29</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">29.09</td>
        <td class="metric-val">31.19</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">46.85</td>
        <td class="metric-val">43.36</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">54.83</td>
        <td class="metric-val">51.33</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">HyenaID2022</td>
        <td>mAP</td>
        <td class="metric-val">25.94</td>
        <td class="metric-val">22.19</td>
        <td rowspan="4" class="metric-val">2.02</td>
        <td rowspan="4" class="metric-val">0.58</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">59.29</td>
        <td class="metric-val">51.29</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">73.88</td>
        <td class="metric-val">66.35</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">80.94</td>
        <td class="metric-val">74.59</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">IPanda50</td>
        <td>mAP</td>
        <td class="metric-val">13.45</td>
        <td class="metric-val">14.61</td>
        <td rowspan="4" class="metric-val">6.48</td>
        <td rowspan="4" class="metric-val">0.52</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">55.19</td>
        <td class="metric-val">60.57</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">80.53</td>
        <td class="metric-val">84.93</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">90.12</td>
        <td class="metric-val">91.00</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">LeopardID2022</td>
        <td>mAP</td>
        <td class="metric-val">19.35</td>
        <td class="metric-val">19.75</td>
        <td rowspan="4" class="metric-val">5.17</td>
        <td rowspan="4" class="metric-val">0.62</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">63.50</td>
        <td class="metric-val">60.81</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">78.59</td>
        <td class="metric-val">80.66</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">83.97</td>
        <td class="metric-val">86.14</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">MultiCamCows2024</td>
        <td>mAP</td>
        <td class="metric-val">26.89</td>
        <td class="metric-val">28.86</td>
        <td rowspan="4" class="metric-val">4.69</td>
        <td rowspan="4" class="metric-val">0.61</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">63.07</td>
        <td class="metric-val">64.29</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">80.59</td>
        <td class="metric-val">80.05</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">85.98</td>
        <td class="metric-val">86.52</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">NDD20</td>
        <td>mAP</td>
        <td class="metric-val">8.87</td>
        <td class="metric-val">8.81</td>
        <td rowspan="4" class="metric-val">4.32</td>
        <td rowspan="4" class="metric-val">0.22</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">25.06</td>
        <td class="metric-val">21.52</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">51.65</td>
        <td class="metric-val">50.89</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">65.06</td>
        <td class="metric-val">63.29</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">NyalaData</td>
        <td>mAP</td>
        <td class="metric-val">10.00</td>
        <td class="metric-val">9.53</td>
        <td rowspan="4" class="metric-val">1.90</td>
        <td rowspan="4" class="metric-val">0.18</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">19.62</td>
        <td class="metric-val">13.08</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">41.15</td>
        <td class="metric-val">36.15</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">53.46</td>
        <td class="metric-val">55.38</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">OpenCows2020</td>
        <td>mAP</td>
        <td class="metric-val">31.43</td>
        <td class="metric-val">29.23</td>
        <td rowspan="4" class="metric-val">9.68</td>
        <td rowspan="4" class="metric-val">0.75</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">77.01</td>
        <td class="metric-val">77.42</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">93.77</td>
        <td class="metric-val">93.77</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">97.51</td>
        <td class="metric-val">96.95</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">PolarBearVidID</td>
        <td>mAP</td>
        <td class="metric-val">48.13</td>
        <td class="metric-val">42.49</td>
        <td rowspan="4" class="metric-val">20.03</td>
        <td rowspan="4" class="metric-val">0.77</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">81.82</td>
        <td class="metric-val">78.79</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">98.99</td>
        <td class="metric-val">97.47</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">100.00</td>
        <td class="metric-val">98.99</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">PrimFace</td>
        <td>mAP</td>
        <td class="metric-val">39.28</td>
        <td class="metric-val">42.52</td>
        <td rowspan="4" class="metric-val">5.44</td>
        <td rowspan="4" class="metric-val">0.76</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">77.35</td>
        <td class="metric-val">75.69</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">91.71</td>
        <td class="metric-val">90.61</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">94.48</td>
        <td class="metric-val">95.03</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">ReunionTurtles</td>
        <td>mAP</td>
        <td class="metric-val">28.44</td>
        <td class="metric-val">26.93</td>
        <td rowspan="4" class="metric-val">2.94</td>
        <td rowspan="4" class="metric-val">0.30</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">32.35</td>
        <td class="metric-val">44.12</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">67.65</td>
        <td class="metric-val">61.76</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">73.53</td>
        <td class="metric-val">76.47</td>
        </tr>
        <tr>
        <td rowspan="4" class="dataset-name">SealID</td>
        <td>mAP</td>
        <td class="metric-val">11.24</td>
        <td class="metric-val">12.24</td>
        <td rowspan="4" class="metric-val">4.86</td>
        <td rowspan="4" class="metric-val">0.27</td>
        </tr>
        <tr>
        <td>Rank-1</td>
        <td class="metric-val">30.33</td>
        <td class="metric-val">36.00</td>
        </tr>
        <tr>
        <td>Rank-5</td>
        <td class="metric-val">56.67</td>
        <td class="metric-val">59.00</td>
        </tr>
        <tr>
        <td>Rank-10</td>
        <td class="metric-val">70.67</td>
        <td class="metric-val">71.00</td>
        </tr>
    </tbody>
    </table>
</div>