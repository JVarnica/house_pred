# Ames House Prediction Dataset.

In this first project I have used the Ames housing dataset which is from a rolling kaggle competition to predict house prices. The goal of this study is to try and get the best performance possible but to also check whther MLPs perform better than other models such as decision trees and ensemble models.

## Data Exploration

This dataset has 1460 different samples and 81 features, with 38 being integers and 43 of object type so mostly categorical features. There are a total of 6617 missing values, luckily most are in a few features; as saleprice has no missing values no rows will be removed. PoolQC for pool quality has 1453 missing features, so only has 7 non-missing values! All features which have more than 10 percent missing values will be removed, as cannot impute missing values when most are missing would be an absolutely biased feature.

Therefore the following features have been removed: Alley, FireplaceQu, PoolQC, Fence, LotFrontage and MiscFeature. This leaved us with 75 features. Now there are the garage features which all have 5.548% missing values, in order to keep them I just made the assumption that all should be placed in the NA category. This made sense as whenever a row had all garage related features empty it just indicates an absence of a garage. The same logic was applied to some of the basement features such as BsmtFinType2, BsmtExposure and BsmtQual which all had 38 (2.5%) missing values. 

Next for features where one category dominates the others such as electrical the missing values will be imputed using the mode. 

