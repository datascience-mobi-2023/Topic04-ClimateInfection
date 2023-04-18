Topic 04: Climate-sensitive infectious diseases: Dengue case
============================================================

### *Project overview and guidelines*

-   [Introduction](#introduction)
-   [Objective](#objective)
-   [Description of datasets](#description-of-datasets)
-   [Literature review](#literature-review)
-   [How to structure your project](#how-to-structure-your-project)
    -   [Project proposal](#project-proposal)
    -   [Project](#project)

Supervisor
----------

* Dr. Marina Treskova (supervisor/tutor) (marina.treskova@uni-heidelberg.de)
* Dr. Stella Dafka (supervisor/tutor) (stella.dafka@uni-heidelberg.de)
* Luise Nottmeyer (tutor) (luise.nottmeyer@gmail.com)


Introduction
------------

Climate change-driven environmental changes are expected to exacerbate the burden of climate-sensitive infectious diseases such as dengue and malaria in the absence of healthcare adaptation strategies. Changing seasonality, accelerated urbanization and increasing density of the population are expected to impact the incidence of the infections and emergence in new geographical locations. Dengue virus is transmitted from people to people by mosquito of Aedes genera.They are also known as vectors of dengue. Dengue virus causes dengue fever and dengue hemorrhagic fever particularly in children. Dengue is expected to expand its geographical range due to the warming climate. It is driven by habitat suitability changes for the vectors. The vectors are highly adapted to living and moving with humans and their lifestyle is known to depend on climate parameters such as temperature and precipitation. Strengthening of the current surveillance and public health response systems is crucial. Inclusion of forecasting tools into the early warning system can facilitate a more effective planning and timely allocation of healthcare resources. Most of the forecasting tools are based on assessing the risk and model-based predictions of expected trends in epidemiology of infectious diseases.Understanding of the epidemiology of dengue and impact of climate change on the incidence of infections requires spatial analysis along with temporal and socio-economic considerations. Data preprocessing, extraction, visualization and representation of spatial and temporal trends are initial steps in building models. 
This project leverages the data on dengue obtained from infectious disease database GIDEON (https://www.gideononline.com/) and ERA5 reanalysis data to shed light on climate-driven spatio-temporal patterns of dengue in the recent past.


Objectives and work plan
------------------------

The project objectives are: 

1. understand infectious disease data
2. use data analytics and visualization methods to represent links between climate and dengue spatio-temporal presence
3. try regression methods to establish statistical associations.

**Sub-projects** can focus on a detailed analysis of **specific countries** depending on the number of dengue outbreaks and conduct spatio-temporal modelling and or on understanding and working with NetCDF data.


Description of datasets
-----------------------

* **ERA5 Reanalysis data**: Hourly estimates of total precipitation and 2m temperature from 2008 to 2022 are retrieved from the interpolated European Centre for Medium-Range Weather Forecasts (ECMWF) 5th Re-Analysis (ERA5) dataset. The ERA5 is the latest generation of ECMWF global atmospheric reanalysis, covering the period from 1959 onwards (Hersbach et al. 2020). It combines model data with measurements from satellites and in situ instruments and provides hourly estimates of a large number of atmospheric, land and oceanic climate variables. The data cover the earth on a 30km grid and resolve the atmosphere using 137 levels from the surface up to a height of 80km. ERA5 data are available on the Copernicus Climate Change Service (C3S) Climate Data Store (CDS; https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=overview) on a regular latitude-longitude grid at 0.25° x 0.25° horizontal resolution. In this project, the hourly accumulated precipitation fields are summed to form the 24 hr precipitation totals. Daily mean values are computed for temperature. The daily values for both ERA5 fields (Total Precipitation and Temperature) have been aggregated for different countries over Southeast Asia region across 2008-2022 (15 years).  Although, reanalyses pose challenges in reconstructing variables such as precipitation which varies largely in time and space, Hersbach et al. (2018) and identified improvements in the representation of global-mean rainfall in ERA5 compared to its predecessor ERA-Interim (using the global monthly gridded precipitation dataset GPCP as reference). More recently,  Hassler and Lauer (2021) evaluated the performance of eleven different precipitation datasets and identified a clear improvement of ERA5 and ERA5-Land over other reanalysis datasets in the tropics.

* **Dengue dataset**: The dengue dataset contains information on dengue outbreaks, year, country and latitude/longitude. The data are curated as case reports of confirmed outbreaks in the Global Infectious Disease and Epidemiology Online Network (GIDEON) and are accessible via the link https://www.gideononline.com/. The GIDEON is a Global Infectious disease knowledge management tool that maintains up to date information on the latest trends in epidemiology and treatment. 


Both datasets present a large amount of data (Dengue in csv format and ERA5 is NetCDF but will be extracted and prepared for specific latitude longitude)


Literature 
----------
### ERA5 Reanalysis data
* Hersbach, H. et al. (2020). The ERA5 Global Reanalysis. Quarterly Journal of the Royal Meteorological Society, 146, 1999-2049. https://doi.org/10.1002/qj.3803
* Hersbach, H. et al (2018). Operational global reanalysis: progress, future directions and synergies with NWP. ERA Report Series no. 27, ECMWF, Reading, UK
* Hassler, B. and Lauer, A. (2021) Comparison of Reanalysis and Observational Precipitation Datasets Including ERA5 and WFDE5. Atmosphere, 12, 1462. https://doi.org/10.3390/ atmos12111462

### Dengue
* Phanitchat T, Zhao B, Haque U, Pientong C, Ekalaksananan T, Aromseree S, Thaewnongiew K, Fustec B, Bangs MJ, Alexander N, Overgaard HJ. Spatial and temporal patterns of dengue incidence in northeastern Thailand 2006-2016. BMC Infect Dis. 2019 Aug 23;19(1):743. doi: 10.1186/s12879-019-4379-3 
* Tsheten T, Clements ACA, Gray DJ, Wangchuk S, Wangdi K. Spatial and temporal patterns of dengue incidence in Bhutan: a Bayesian analysis. Emerg Microbes Infect. 2020 Dec;9(1):1360-1371. doi: 10.1080/22221751.2020.1775497
* Atique S, Chan TC, Chen CC, Hsu CY, Iqtidar S, Louis VR, Shabbir SA, Chuang TW. Investigating spatio-temporal distribution and diffusion patterns of the dengue outbreak in Swat, Pakistan. J Infect Public Health. 2018 Jul-Aug;11(4):550-557. doi: 10.1016/j.jiph.2017.12.003
* Faruk MO, Jannat SN, Rahman MS. Impact of environmental factors on the spread of dengue fever in Sri Lanka. Int J Environ Sci Technol (Tehran). 2022;19(11):10637-10648. doi: 10.1007/s13762-021-03905-y

How to structure your project
-----------------------------

### Project proposal

You first task will we to define a **project proposal**, which should
include

-   summary of literature on this dataset
-   questions you want to address
-   approximate timetable

You will present this project proposal together with a literature review
on the subject 3 week after the beginning of the semester (10 minute
presentation + 5 minutes discussion).

### Project

You project should contain the following elements:
- **descriptive statistics** about the datasets
- **graphical representations**
- **dimension reduction** analysis (PCA, clustering or k-means)
- **statistical tests** (t-test, proportion tests etc)
- **linear regression** analysis, either uni- or multivariate

#### Data cleanup

You will be analyzing multiple data sets together. It is
essential that you explore each dataset and clean it. Cleaning can refer
to many things:

-   Removing/Imputing missing values
-   Removing low variance columns/rows
-   Removing batch effects
-   Removing outlier samples (only if it is due to technical issues !!)
-   Making sure that data is in the correct format, for example, numbers
    should be encoded as numeric and not as characters. Categorical
    variables should be factors etc.
-   Re-ordering rows/columns in meaningful and useful ways

#### Data exploration

Now that you have cleaned data, explore your data to understand its
structure. Perform basic exploratory data analysis.

-   Look at the distribution of the overall data, specific samples or
    features.
-   Visualize the data distribution
-   Visualize the inter-dependencies (e.g. correlations) among specific samples/features of
    interest
-   Check some of your hypothesis like - is something high/low between
    two conditions etc

#### Data reduction

You have a high dimension matrix, that is, you have way more features
 than observations.

-   Try out methods to reduce the dimensionality of this data.
-   Cluster your samples to identify similar and dis-similar groups
-   Check how well the groups separate based on the features of your
    interest

#### Data modelling

Use linear regression to evaluate the relation between variables and predicting one using others.
