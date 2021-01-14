#Predict the percentage of an student based on the no. of study hours.
Hours <- c(2.5,5.1,3.2,8.5,3.5,1.5,9.2,5.5,8.3,2.7,7.7,5.9,4.5,3.3,1.1,8.9,2.5,1.9,6.1,7.4,2.7,4.8,3.8,6.9,7.8)

Scores <- c(21,47,27,75,30,20,88,60,81,25,85,62,41,42,17,95,30,24,67,69,30,54,35,76,86)

relation <- lm(Scores~Hours)
StudyTable <- data.frame(Hours=9.25)
result <- predict(relation,StudyTable)
print(result)
plot(Scores,Hours,col="blue",main = "Relation between Hours and Scores", abline(lm(Hours ~ Scores),cex =1.3, pch = 16, xlab = "Hours", ylab = "Scores"))
