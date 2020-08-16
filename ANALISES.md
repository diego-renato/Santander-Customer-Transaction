## Table of contents
- [1. The problem](#1-the-problem)
- [2. The data](#2-the-data)
- [3. Comparing different scaler functions](#3-comparing-scaler)
    -[3.1. Normalization scaler: scatter and hist (01-06-2020 to 08-06-2020)](#3-normalization-scaler)
    -[3.2. Standard scaler: scatter and hist (01-06-2020 to 08-06-2020)](#3-standard-scaler)
    -[3.3. Max abs scaler: scatter and hist (01-06-2020 to 08-06-2020)](#3-max-abs-scaler)
    -[3.4. Min max scaler: scatter and hist (01-06-2020 to 08-06-2020)](#3-min-max-scaler)
    -[3.5. Power transformer: scatter and hist (01-06-2020 to 08-06-2020)](#3-power-transformer-scaler)
    -[3.6. Robust scaler: scatter and hist (01-06-2020 to 08-06-2020)](#3-robust--scaler)

- [4. The optimal number of clusters](#4-cluster-optimal)

# 1. The problem

# 2. The data

# 3. Comparing different scaler functions
After scaling the data, is important to see the behavior of the scaled or transformed data.
In this section I compared the different scaler jobs from the considered in this project for the week 01-06-2020 to 08-06-2020 and
the week 24/07/2020 - 31/08/2020 by scatter plots and histograms. The variables selected are <b>longitude</b>, <b>latitude</b> and <b>preço</b> because are variables
to be considered to obtain clusters in the next section.  

* I considered in the scatter plot the variables <b>longitude</b> and <b>latitude</b>, because this variables generate a map.
* And <b>preço</b> for the histogram.

#### Normalization scaler: scatter and hist (01-06-2020 to 08-06-2020)

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 1.1: Longitude vs latitude dos visitantes antes e depois de <b>normalization</b> .</p>
</div>
<br>
<br>
<br>

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 1.2: Frequency histogram of preço dos produtos considerados antes e depois de <b>normalization</b>.</p>
</div>
<br>
<br>
<br>

#### Standard scaler: scatter and hist (01-06-2020 to 08-06-2020)

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 2.1: Longitude vs latitude dos visitantes antes e depois de <b>standard scaler</b> .</p>
</div>
<br>
<br>
<br>

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 2.2: Frequency histogram of preço dos produtos considerados antes e depois de <b>standard scaler</b>.</p>
</div>
<br>
<br>
<br>

#### Max abs scaler: scatter and hist (01-06-2020 to 08-06-2020)

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 3.1: Longitude vs latitude dos visitantes antes e depois de <b>max abs scaler</b> .</p>
</div>
<br>
<br>
<br>

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 3.2: Frequency histogram of preço dos produtos considerados antes e depois de <b>max abs scaler</b>.</p>
</div>
<br>
<br>
<br>

#### Min max scaler: scatter and hist (01-06-2020 to 08-06-2020)

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 4.1: Longitude vs latitude dos visitantes antes e depois de <b>min max scaler</b> .</p>
</div>
<br>
<br>
<br>

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 4.2: Frequency histogram of preço dos produtos considerados antes e depois de <b>min max scaler</b>.</p>
</div>
<br>
<br>
<br>

#### Power transformer: scatter and hist (01-06-2020 to 08-06-2020)

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 5.1: Longitude vs latitude dos visitantes antes e depois de <b>power transformer</b> .</p>
</div>
<br>
<br>
<br>

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 5.2: Frequency histogram of preço dos produtos considerados antes e depois de <b>power transformer</b>.</p>
</div>
<br>
<br>
<br>

#### Robust scaler: scatter and hist (01-06-2020 to 08-06-2020)

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 6.1: Longitude vs latitude dos visitantes antes e depois de <b>robust scaler</b> .</p>
</div>
<br>
<br>
<br>

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 6.2: Frequency histogram of preço dos produtos considerados antes e depois de <b>robust scaler</b>.</p>
</div>
<br>
<br>
<br>

Scatter plots an histograms from the other week considered can be founded in [plots from the last week]().

The questions to be answered are:
* Usando uma semana de dados como entrada e vendo os gráficos, o que você pode dizer sobre cada uma das transformações?
* Use uma semana diferente, o que você viu mudando?
* Quais colunas escolheu para gerar suas análises, e por quê?
* Quais colunas sofreram maiores efeitos e quai sofretam menos?


# 4. The optimal number of cluster
The number of cluster is considered a hyperparameter, in the literature there are different ways to find the optimal number of cluster. 
For example from short datasets the hierarchical clustering is a good option(not in our case), the elbow method(graphics method) or 
the GAP statistic(ca be used in any clustering method), but there is another and powered method using a distribution probability actually a 
finite mixture distribution and computing some information criterion like AIC or BIC, it is the finite gaussian mixture. The gaussian mixture 
is a parametric probability distribution from *K* gaussian or normal random variables. For short explanation let see the equation above
 
<img src=https://wikimedia.org/api/rest_v1/media/math/render/svg/2f13843df7f69545e27b06c4b59f1d8fe9690ce1>

The *N(.)* denote a multivariate normal distribution with a vector of means and matrix of covariance, the 
phi denote the probability for a *latent variable* belong a one population, the *latent variable* is actually the cluster and
the number *K* is the number of cluster or populations. Please see [gaussian mixture](http://leap.ee.iisc.ac.in/sriram/teaching/MLSP_16/refs/GMM_Tutorial_Reynolds.pdf)
if you want to see more details.

The benefit of using the gaussian mixture is that the dataset belows a multivariate distribution, they don´t need to be scaled
 and the log likelihood can be computed and also be compared for different k values (clusters). And also, we can predict the cluster from a given
 vector of observation with their respective probability.
 
So, for our case, it is considered a grid of values, *K = 2,3,...,15* ,to compute the AIC (Akaike information criterion) using train-test split. Then,
the optimal number of cluster is the value of *K* that minimize the AIC in the test data (30% of original data). This is important because we can evaluate in a
unobserved dataset(Observation: The AIC penalizes the -2 log likelihood by the number of parameters.). The following graph shows the results obtained.

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 7: AIC values from validation set using finite gaussian mixture .</p>
</div>
<br>
<br>
<br>

Also we can see the behaviour of the data by dimensional reduction for data visualization, in this context the PCA can be useful,
keep in main that the data have to be standard scaled or have the same variance because the PCA works with the covariance matrix. 
The following graph shows the results obtained from 2 component that represent more than the 50% of the total variability explained. 

<div align="center">
    <img width="750" src="./doc/source/dataset/lagarta/lagarta.jpeg" />
    <p>Figure 8: Principal components scatter plot from 2 components .</p>
</div>
<br>
<br>
<br>

