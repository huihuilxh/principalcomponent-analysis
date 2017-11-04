# principalcomponent-analysis
### 主成分分析 ########### 

student=data.frame(
X1=c(148, 139, 160, 149, 159, 142, 153, 150, 151, 139, 
140, 161, 158, 140, 137, 152, 149, 145, 160, 156, 
151, 147, 157, 147, 157, 151, 144, 141, 139, 148), 
X2=c(41, 34, 49, 36, 45, 31, 43, 43, 42, 31, 
29, 47, 49, 33, 31, 35, 47, 35, 47, 44,
42, 38, 39, 30, 48, 36, 36, 30, 32, 38),
X3=c(72, 71, 77, 67, 80, 66, 76, 77, 77, 68, 
64, 78, 78, 67, 66, 73, 82, 70, 74, 78, 
73, 73, 68, 65, 80, 74, 68, 67, 68, 70),
X4=c(78, 76, 86, 79, 86, 76, 83, 79, 80, 74, 
74, 84, 83, 77, 73, 79, 79, 77, 87, 85, 
82, 78, 80, 75, 88, 80, 76, 76, 73, 78)
)



#### 作主成分分析

student.pr=princomp(student, cor=TRUE)

#student.pr=princomp(~X1+X2+X3+X4, data=student, cor=TRUE) 



#### 并显示分析结果

summary(student.pr, loadings=TRUE)



#### 作预测

predict(student.pr)



#### 画碎石图

screeplot(student.pr)

screeplot(student.pr,type="lines")



biplot(student.pr)


