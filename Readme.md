# Pump it Up: Data Mining the Water Table
## _HOSTED BY DRIVENDATA_ 

>Index Number : 170350L <br>
>Name : W. H. M. Lowe <br>
>DrivenData username : moracse_170350l

Github Link : https://github.com/hiranlowe/pumpitup

## Data Exploration

- For the EDA step **pandas-profiling** was used to have a proper understanding about the dataset. 
  - Some features have **missing** values
  - Some features have many **0** values
  - Columns with high **cardinality**
  - Columns with high **correlation**
  - **Skewed** Columns and **outliers**

There are three target classes which describes the functionality of the water pumps. They are **functional**, **non functional**, and **functional needs repair**.  <br>
The dataset was highly imbalances where functional needs repair class had only 7% data from the dataset.

| Class | Datapoints |
| ------ | ------ |
| functional | 32259 |
| non functional | 22824 |
| functional needs repair | 4317|

**Accuracy** score was selected as the evaluation metric because the competiton uses **classification rate** as the evaluation metric.
## Feature Engineering

- First after reading several articles about the pum it up challenge it was found that some columns contains same information although they have different column names. So those columns were dropped after finding out the importance of thaose features.
  - management, management_group, scheme_management
  - quantity, quantity_group
  - water_quality, quality_group
  - source, source_type, source_class
  - extraction_type, Extraction_type_group, extraction_type_class
  - payment, payment_type
  - waterpoint_type, waterpoint_type_group
  - region, region_code, subvillage
- Then missing values and 0 values were handles according to the information of the columns. 
- 'construction-year' columns was grouped to a new column 'decade' to reduce the cardinality.
-  Cardinality of several columns were reduced by creating a new category for the last groups of the categories list. 
- New columns were created for the categorical columns with high cardinality(installer, funder). 

## References

[Pum it Up forum](https://community.drivendata.org/c/pump-it-up-data-mining-the-water-table/11)

[Pump it Up Github](https://github.com/drivendataorg/pump-it-up)

[Pump it Up article](https://towardsdatascience.com/pump-it-up-predict-water-pump-condition-using-data-science-2839d26638b8)

[Ofigue github](https://github.com/ofigue/Tazmania_WaterPump)

