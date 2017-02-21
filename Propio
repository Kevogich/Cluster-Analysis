library(factoextra)

## Loading required package: ggplot2

library(ggplot2)

hr=read.csv(file="../input/HR_comma_sep.csv")
hr$salary = as.numeric(hr$salary)
hr = subset(hr,hr$left==1)
#Seperate out independent variables and classifications.
X = hr[,c(1:6,8,10)]
Y = hr[,7]

X.pca = prcomp(X,center=TRUE,scale.=TRUE)
print(X.pca$rotation)

##                                PC1         PC2          PC3          PC4
## satisfaction_level     0.064628267 -0.85224822  0.016021655 -0.019640149
## last_evaluation        0.521943681 -0.06383544 -0.004857218  0.009770547
## number_project         0.493159461  0.31697635 -0.016260338  0.038547889
## average_montly_hours   0.509569613  0.19366210 -0.012422868  0.030903059
## time_spend_company     0.467461848 -0.35953682  0.007656490  0.008706459
## Work_accident         -0.003387737 -0.03546264 -0.732948831 -0.041315585
## promotion_last_5years -0.035064037 -0.01497552 -0.570889688  0.576800585
## salary                 0.027730745  0.02950254 -0.368935416 -0.814000103
##                                 PC5          PC6          PC7          PC8
## satisfaction_level     0.0348582891 -0.351894292  0.146968444 -0.349584477
## last_evaluation        0.0038691794 -0.432447504 -0.584454099  0.441325692
## number_project        -0.0009213276  0.016447295 -0.197847810 -0.784317720
## average_montly_hours   0.0055250211 -0.253158467  0.773013623  0.200136642
## time_spend_company    -0.0018937000  0.790241032 -0.002489855  0.166095151
## Work_accident         -0.6780279210 -0.007393919  0.004389222 -0.003763101
## promotion_last_5years  0.5826792451  0.011527072 -0.009384210  0.014009186
## salary                 0.4466519943  0.011463331  0.002517338 -0.003917679

print(summary(X.pca))

## Importance of components:
##                           PC1    PC2    PC3    PC4    PC5     PC6     PC7
## Standard deviation     1.8167 1.1428 1.0310 1.0033 0.9621 0.41426 0.36134
## Proportion of Variance 0.4125 0.1633 0.1329 0.1258 0.1157 0.02145 0.01632
## Cumulative Proportion  0.4125 0.5758 0.7087 0.8345 0.9502 0.97166 0.98798
##                            PC8
## Standard deviation     0.31011
## Proportion of Variance 0.01202
## Cumulative Proportion  1.00000
