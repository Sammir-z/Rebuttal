<img src=".\fig_1(a).png" alt="fig_1(a)" style="zoom:25%;" />

(a) Adaptive-Margin Modality Identification

<img src=".\fig_1(b).png" alt="fig_1(a)" style="zoom:25%;" />


(b) Restoration Strategy

**Figure 1** (a)Adaptive-Margin Modality Identification, where left is quantified modality laziness via incorrectness and uncertainty, and right is a soft margin $\gamma$ used to distinguish dominated (white) vs. lazy (black) modality by considering ambiguous samples (gray).(b)Restoration Strategy: The framework **epoch-level periodically alternates** between full joint optimization and adaptive masking. Masking (white blocks) decouples the gradient flow of dominated modalities to force the exploitation of lazy ones. The objects with the **same shape represent the same instance** with features from different modalities.

<br/><br/>



**Table 1.**  Results(%) of unimodal performance.

| **Datase**    | **Concat** | **Random** | **OGM**   | **OPM**   | **MLA**   | **Resample** | **Remix** | **AMST_joint** | **AMRe (Ours)** |
| --------------- | ---------- | ---------- | --------- | --------- | --------- | ------------ | --------- | -------------- | --------------- |
| **CREMA-D (V)** | 68.95      | 60.89      | **69.22** | 67.33     | 58.87     | 68.95        | 64.11     | 58.36          | 66.13           |
| **CREMA-D (A)** | 63.17      | 63.84      | 62.10     | **65.05** | 65.34     | 63.31        | 58.47     | 64.27          | 61.96           |
| **AVE (V)**     | 37.56      | 37.56      | 38.64     | 39.30     | 42.51     | 38.06        | 37.31     | 36.66          | **42.54**       |
| **AVE (A)**     | 64.68      | 62.94      | 62.83     | 65.67     | 66.85     | 66.42        | 63.95     | 64.41          | **67.66**       |
| **MVSA (I)**    | 60.08      | 59.04      | 59.67     | 57.92     | 60.09     | **61.95**    | 61.33     | 56.76          | 59.88           |
| **MVSA (T)**    | 70.27      | 71.72      | 71.93     | 72.35     | 71.13     | 72.56        | 70.89     | 68.43          | **72.77**       |
| **IEMOCAP (V)** | 28.85      | 27.81      | 30.62     | -         | **46.45** | 26.04        | 45.12     | 29.91          | 34.17           |
| **IEMOCAP (A)** | 48.52      | 43.49      | 44.97     | -         | 47.93     | 49.26        | 46.30     | **52.76**      | 50.59           |
| **IEMOCAP (T)** | 58.14      | 60.79      | 60.36     | -         | 57.40     | 59.47        | 58.73     | 53.80          | **61.69**       |



<br/><br/>

**Table 5**.  Result(\%) of different laziness evaluation metrics. Specifically, CE Loss and Brier Score are utilized to measure incorrectness, whereas KL divergence and Entropy are employed to evaluate uncertainty.

|     Method      |    AVE    |   MVSA    |  IEMOCAP  |
| :-------------: | :-------: | :-------: | :-------: |
|     CE loss     |   75.12   |   74.01   |   65.83   |
|      Brier      |   75.87   |   74.84   |   66.42   |
|       KL        |   72.39   |   73.60   |   66.72   |
|     Entropy     |   74.88   |   71.93   |   66.12   |
|   CE loss+KL    | **76.37** | **75.68** | **68.93** |
| CE loss+Entropy |   74.88   |   74.22   |   67.75   |
|    Brier+KL     |   74.13   |   74.22   |   66.72   |
|  Brier+Entropy  |   73.88   |   74.84   |   65.38   |
|                 |           |           |           |





