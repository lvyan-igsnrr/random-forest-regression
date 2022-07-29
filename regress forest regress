## Loading packages and data------------------------------------------------------------

library(randomForest)
library(pheatmap)

library(extrafont)

library(corrplot)

library(car)

setwd("C:/Users/ly/Desktop/") # Setting up the work path

Data_resistance <- read.csv("regress forest.csv") # Reading data

## Random forest regression--------------------------------------------------------------

set.seed() # Setting up random number seeds

Rf_resistance <- randomForest(resistance ~ c("MAT", "MAP", "MAR", "Species richness"), data = Data_resistance, ntree = 500, importance = TRUE) # Modelling

# Results of random forest regression

forest.pred_Airbnb <- predict(Rf_resistance, Data_resistance) # Predicted results

forest.pred_Airbnb1 <- data.frame(forest.pred_resistance, Data_resistance) # Comparison of predicted and actual results

# Variable importance - %lncMSE

importance(Rf_resistance)
