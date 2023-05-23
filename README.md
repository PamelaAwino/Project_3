Tanzania_water_wells_project

BUSINESS UNDERSTANDING

![image](https://github.com/PamelaAwino/Project_3/assets/124348072/2c3a5a5c-aafe-4786-9edf-dc2da1b4f322)


Overview:

Water is a very essential part of both human and animal life. Water bodies are not just beautiful additions to our planet's scenery; but also play a crucial role in our survival. Water is used for domestic purposes, economic activities (such as production of electricity in the energy sector) and in health and hygiene. Based on Worldometer elaboration of the latest United Nations, Republic of Tanzania population is estimated to be at 64,614,354 as of Wednesday, May 17, 2023. There is definately an increase in the population as compared to the number found during the last census with 59 million in 2020 as per United Nations findings. Nsemwa (2022) many Tanzanians continue to struggle with insufficient or limited access to clean and safe water. Only 30.6% of Tanzanian households use recommended water treatment methods, and only 22.8% have adequate hand-washing facilities (Ministry of Health report, 2019). Poor sanitation is estimated to cause 432,000 diarrhea-related deaths per year and is a major contributor to several Neglected Tropical Diseases (NTDs) such as intestinal worms, schistosomiasis, and trachoma. Malnutrition is also made worse by poor sanitation (WHO, 2019).

Problem:

Tanzania is currently failing to meet the potable water requirements for its population. Despite already building water wells to offset this problem, many are unfortunately non-functional and others are in need of repair. As a result, our stakeholder, WHO, has narrowed down their interest to drilling more water wells and maintaining/ revamping existing ones within the country, in an effort to ensure availability of quality and quantity drinking water countrywide .

Our role as the data scientist in this project will be to identify patterns in non-functional wells, with the aim of influencing how new ones are built. Furthermore, using these patterns, we will enable our stakeholder to accurately predict existing water points in need of intervention ensuring the people of Tanzania have access to clean potable water

Specific Objectives

To identify non-functioning wells using a simple analysis, and predict the functionality of a well based on available variables

To determine the functionality status concerning payment type

To determine if functionality varies by quantity.

To predict the condition of a waterpoint pump based on the geographical location

Research Questions

Does water quality affect the functionality of a waterpoint pump?

Does extraction type affect the functionality of a waterpoint pump?

Does Region have an effect on functionality?

Do different water sources have an effect on well functionality?

Goal:

The major objective of this study is to build a model that classifies the functional status of water wells in Tanzania. With this predictive model, the ministry can understand which water points are functional and non-functional, give useful information for future wells, and identify areas at risk of water shortage.

Project Metric of Success:

To ensure that newly constructed wells are of good quality water for the communities.

To correctly identify functionality of a well and determine its viability.

Generating a model that will be able to correctly predict the quality status of the wells in Tanzania with an accuracy of 70-75 %

DATA UNDERSTANDSING

Data:

The original data was obtained from the DrivenData 'Pump it Up: Data Mining the Water Table' competition. Basically, there are 4 different data sets; submission format, training set, test set and train labels set which contains status of wells. With given training set and labels set, competitors are wanted to build predictive model and apply it to test set to determine status of the wells and submit. In this project, we used train set and train label set which have 59400 water points data with 40 features.

Plan:

Understanding Data

Cleaning and Exploring Data

Preparing Data to Modeling

Finding Binary Model & Baseline

Ternary Target Modeling

Understanding Data:

The data has a 59,400 rows and 41 columns. Of those 41 columns, 10 were numeric columns and the remaining 31 were string columns; known as object in pandas. After clearly observing the data through the .info method and the descriptive statistics of the numerical columns, we made some critical observations that will assist us in analyzing the data and coming up with an efficient model. These observations include: After going through the variable description of the data and performing the preliminary data inspection, we discovered that there are some columns that provide the same information which makes theme irrelevant in this study. The study discovered that 21 columns will not be used in this investigation and thus were deemed ‘repititve and unuseful’

Data Preparation

It is vital for data to be prepared before being staged for modelling to enhance the model's efficiency and prevent the generation of misleading insights. In this phase of the investigation, the study will look at missing values, duplicated entries, inconsistencies and invalid data. In this section, we first dropped the irrelevant columns mentioned in data understanding since we do not have to prepare columns that will not be used in the study.

Exploratory Data Analysis

In this phase of the investigation, the study will look at the trends, patterns using visualizations and statistics to show the relationships between the variables within the data

Univariate, Bivariate and Multivariate analysis were performed on the data.

EDA Conclusion

For extraction type, submersible has the most amount of water available in the data despite not registering some of the highest heights. Motorpumps and submersible are generally located in low altitude areas, possibly because while there it is nearer to the water table than at a higher altitude. For a handpump to have water available above the median amount of total static head, it needs to be above a height of 500 meters above sea level

The observations made through this analysis can be used to provide recommendations to the government on where more wells ae needed, the requirement of the locatiIn conclusion, the entity that funds most of the waterpoints going by the analysis is the Government of Tanzania and they are also the second most installers of the waterpoints thus it makes sense that they are the chosen stakeholders for this investigation.

The anlaysis also discovers that communal standpipe seems to be the most popular waterpoint type around the country. Most of the wells that are never paid for were discovered to be non functional.

![image](https://github.com/PamelaAwino/Project_3/assets/124348072/25e75e85-0246-4e60-95cc-a41be93cf0b2)



##Preparing Data to Modeling:

To prepare our data to machine learning, we did some feature engineering, encoding and scaling.

Findings:

The final model was selected as the KNeighborsClassifier

Most functional waterpoint pumps are those that have soft water

Waterpoints with enough water are the most functional

Iringa, Kilimanjaro and Shinyanga are the top 3 regions with most functional pumps

Kilimanjaro and Mbeya have the regions with the most non-functional pumps

Kigoma has the highest number of waterpoints that need repair

Water drawn from springs and shallow wells have the highest number of functional pumps

Water drawn from Springs have the highest number of functional pumps that need repair

Water drawn from Shallow wells and boreholes have the highest number of non functional wells

Those waterpoints with insufficient water have very few functional pumps

Recommendation

In summary, it is recommended that the government gives priority to sourcing water from springs rather than shallow wells or boreholes during the construction of water points. This is because water drawn from springs is less likely to cause quick damage to the pumps.

Additionally, water points with ample water supply should be carefully monitored due to the high usage, which can potentially lead to their failure. By implementing these practices, the government can enhance the longevity and effectiveness of water points while ensuring that those with sufficient water are adequately monitored to prevent any operational issues.

Future Improvements:

Further monitoring of the model to ensure that the accuracy is increased
