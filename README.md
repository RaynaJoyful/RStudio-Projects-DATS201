# RStudio-Projects-DATS201
This repository is full of a bunch of projects and assignments I created throughout my DATS201 course. 

knitr::opts_chunk$set(echo = TRUE)

library(dplyr)
library(readr)
library(GGally)
library(caret)
library(knitr)
library(InformationValue)

path<-'/Users/RaynaAbraham/Desktop/RStudio Projects/insurance.csv'
ins_data<-read_csv(path)
glimpse(ins_data)
kable(summary(ins_data))

ins_data %>%
  dplyr::select(age,bmi,charges) %>%
  ggpairs(title = "", axisLabels = "show")
