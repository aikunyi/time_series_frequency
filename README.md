# Neural Time Series Analysis with Fourier Transform: A Survey

In this paper, we provide a comprehensive review of studies on neural time series analysis with Fourier transform. We aim to systematically investigate and summarize the latest research progress. Accordingly, we propose a novey taxonomy to categorize existing neural time series analysis methods from four perspectives, including characteristics, usage paradigms, network design, and applications. We also share some new research directions in this vibrant area.

## Taxonomy 
![[taxonomy]](https://github.com/BIT-Yi/time_series_frequency/blob/main/pictures/taxonomy.png)
## Characteristics
In this section, we analyze the advantaged characteristics of Fourier Transform, including decomposition, global view, sparse representation, and efficiency.

### Decomposition
### Global view
### Sparse representation
### Efficiency
![[relationship]](https://github.com/BIT-Yi/time_series_frequency/blob/main/pictures/relationship.png)
## Usage paradigms
In this section, we systematically summarize and discuss the research categorization and progress in terms of how to utilize the Fourier transform to enhance time series analysis, i.e., usage paradigms. 
### Feature engineering
ATFN [[paper]](https://ieeexplore.ieee.org/document/9120214) proposes a frequency-domain block to capture dynamic and complicated periodic patterns of time series data, and integrates deep learning networks with frequency patterns. <br>

TFAD [[paper]](https://arxiv.org/abs/2210.09693) utilizes a frequency domain analysis branch to detect complex pattern anomalies, e.g., periodic anomaly. <br>

CoST [[paper]](https://arxiv.org/abs/2202.01575) learns the trend representations in the time domain, whereas the seasonal representations are learned by a Fourier layer in the frequency domain. 

SFM [[paper]](https://dl.acm.org/doi/10.1145/3097983.3098117) explicitly decomposes trading patterns into various frequency components and each component models a particular frequency of latent trading pattern underlying the fluctuation of stock price. <br>

mWDN [[paper]](https://arxiv.org/abs/1806.08946) proposes a wavelet-based neural network structure for building frequency-aware deep learning models for time series analysis.<br>

RobustPeriod [[paper]](https://dl.acm.org/doi/abs/10.1145/3448016.3452779) applies maximal overlap discrete wavelet transform to decouple time series into multiple levels of wavelet coefficients and then detect single periodicity at each level.<br>

FEDformer [[paper]]()https://arxiv.org/abs/2201.12740) combines Fourier analysis with the Transformer which helps Transformer better capture global properties of time series. <br>

FFC [[paper]](https://papers.nips.cc/paper/2020/file/2fd5d41ec6cfab47e32164d5624269b1-Paper.pdf) harnesses the Fourier spectral theory and designs an operation unit to leverage frequency information for enlarging the receptive field of vanilla convolutions. <br>

### Compression

FiLM [[paper]](https://openreview.net/forum?id=zTQdHSQUQWc) view time series forecasting from the sequence compression perspective and applies Fourier analysis to keep the part of the representation related to low-frequency Fourier components to remove the impact of noises. <br>

FcaNet [[paper]](https://arxiv.org/abs/2012.11879) generalizes the compression of the channel attention mechanism in the DCT frequency domain and proposes a multi-spectral channel attention for frequency components selection. <br>

### Data Augmentation
CoST [[paper]](https://arxiv.org/abs/2202.01575) incorporates a novel frequency domain contrastive loss which encourages discriminative seasonal representations and side steps the issue of determining the period of seasonal patterns present in the time series data. <br>
BTSF [[paper]](https://arxiv.org/abs/2202.04770) fuses the temporal and spectral features to enhance the discriminativity and expressiveness of the representations. <br>
TF-C [[paper]](https://openreview.net/forum?id=OJ4mMfGKLN) introduces frequency domain augmentations that it directly perturbs the frequency spectrum. <br> 
### Fourier neural operator learning
FNO [[paper]](arxiv.org/abs/2010.08895) parameterize the integral kernel directly in the Fourier space, allowing for an expressive and efficient architecture for partial differential equations. <br>
AFNO [[paper]](https://arxiv.org/abs/2111.13587) frames token mixing as operator learning and proposes an efficient token mixer that learns to mix in the Fourier domain. <br>
FEDformer [[paper]](https://arxiv.org/abs/2201.12740) proposes Fourier enhanced blocks and Wavelet enhanced blocks to capture important structures in time series through frequency domain mapping.<br>
EV-FGN [[paper]](https://arxiv.org/abs/2210.03093) reformulates the graph convolution operator in the frequency domain and efficiently computes graph convolutions over a supra-graph which represents non-static correlations between any two variables at any two timestamps.<br>
## Network design
### complex-value
### real-value
## Applications
### Forecasting
Stock Price Prediction via Discovering Multi-Frequency Trading Patterns, In KDD, 2017. [[paper]](https://dl.acm.org/doi/10.1145/3097983.3098117) <br>
Spectral temporal graph neural network for multivariate time-series forecasting. In NeurIPS, 2020. [[paper]](https://arxiv.org/abs/2103.07719)  <br>
Autoformer: Decomposition transformers with auto-correlation for long-term series forecasting. In NeurIPS, 2020. [[paper]](https://openreview.net/forum?id=I55UqU-M11y) <br>
FEDformer: Frequency enhanced decomposed transformer for long-term series forecasting. In ICML, 2022. [[paper]](https://arxiv.org/abs/2201.12740
) <br>
Cost: Contrastive learning of disentangled seasonal-trend representations for time series forecasting. In ICLR, 2022. [[paper]](https://arxiv.org/abs/2202.01575) <br>
Film: Frequency improved legendre memory model for long-term time series forecasting. In NIPS, 2022. [[paper]](https://openreview.net/forum?id=zTQdHSQUQWc) <br>
Edge-Varying Fourier Graph Networks for Multivariate Time Series Forecasting. In arXiv, 2022. [[paer]](https://arxiv.org/abs/2210.03093) <br>
### Anomaly Detection
Time-series anomaly detection service at microsoft. In KDD, 2019. [[paper]](https://arxiv.org/abs/1906.03821) <br>
Robusttad: Robust time series anomaly detection via decomposition and convolutional neural networks. In arXiv, 2020. [[paper]](https://arxiv.org/abs/2002.09545) <br>
Fast and accurate partial fourier transform for time series data. In KDD, 2021. [[paper]](https://dl.acm.org/doi/10.1145/3447548.3467293) <br>
TFAD: A decomposition time series anomaly detection architecture with time-frequency analysis. In CIKM, 2022. [[paper]](https://arxiv.org/abs/2210.09693) <br>
### Classification
Multilevel wavelet decomposition network for interpretable time series analysis. In KDD, 2018. [[paper]](https://arxiv.org/abs/1806.08946) <br>
Learning filter widths of spectral decompositions with wavelets. In NeurIPS, 2018. [[paper]](https://dl.acm.org/doi/10.5555/3327345.3327371) <br>
Unsupervised time-series representation learning with iterative bilinear temporal-spectral fusion. In ICML, 2022. [[paper]](https://arxiv.org/abs/2202.04770) <br>
Self-Supervised Contrastive Pre-Training For Time Series via Time-Frequency Consistency, in NIPS 2022, [[paper]](https://openreview.net/forum?id=OJ4mMfGKLN) <br>
## Discussion for Future Opportunities
### Leveraging New Orthogonal Transform Technology
### Combination of Fourier Transform with Deep Learning
### Combination of Learning in the Time and Frequency Domain




