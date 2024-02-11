# Master thesis repository 2021-2024

Result tables output from QSVM classifier. 

### Benchmark Results on Iris data set

|*Model*|Accuracy|Recall|Precision|F1score|TT (s)|
|:---|:---:|:---:|:---:|:---:|:---:|
|QSVM| 0.9737 |**0.9762** |0.9744 |**0.9743** |1510.351|
|Ada Boost Classifier| 0.9371 |0.9371 |0.9568 |0.9354 |0.170|
|Decision Tree Classifier |0.9561 |0.9561 |0.9658 |0.9554 |0.028|
|Dummy Classifier |0.3394 |0.3394 |0.1164 |0.1731 |0.028|
|Extra Trees Classifier |**0.9742** |0.9742 |**0.9794** |0.9738 |0.165|
|Extreme Gradient Boosting |0.9553 |0.9553 |0.9671 |0.9553 |0.065|
|Gradient Boosting Classifier |0.9553 |0.9553 |0.9611 |0.9548| 0.362|
|K Neighbors Classifier| 0.9470 |0.9470 |0.9585 |0.9462 |0.043|
|Light Gradient Boosting Machine |0.9280 |0.9280 |0.9402 |0.9276| 0.141|
|Linear Discriminant Analysis| 0.9561 |0.9561 |0.9653 |0.9552 |0.029|
|Logistic Regression |0.8402 |0.8402 |0.8716 |0.8207 |0.669|
|Naive Bayes |0.9644 |0.9644 |0.9724 |0.9639 |0.030|
|Quadratic Discriminant Analysis |0.9652 |0.9652 |0.9726 |0.9647 |0.030|
|Random Forest Classifier |0.9735 |0.9735 |0.9788 |0.9728 |0.198|
|Ridge Classifier |0.7144 |0.7144 |0.6892 |0.6422 |0.027|
|SVM - Linear Kernel |0.7152 |0.7152 |0.5893 |0.6317 |0.033|

### Benchmark Results on Wine Quality data set
|*Model*|Accuracy|Recall|Precision|F1score|TT (s)|
|:---|:---:|:---:|:---:|:---:|:---:|
|QSVM| 0.7920 |0.6338 |0.8874 |0.6477 |1199.929|
|Ada Boost Classifier |0.9667 |0.9768 |0.979 |0.9777 |0.149|
|Decision Tree Classifier |0.9573| 0.9697 |0.9734 |0.9712 |0.035|
|Dummy Classifier |0.7493 |**1** |0.7493 |0.8567 |**0.023**|
|Extra Trees Classifier| 0.9720 |0.9839 |0.9790 |0.9813 |0.189|
|Extreme Gradient Boosting |**0.9800** |0.9911 |0.9825 |**0.9867** |0.121|
|Gradient Boosting Classifier |0.9720 |0.9857 |0.9773 |0.9814 |0.270|
|K Neighbors Classifier |0.9280 |0.9679 |0.9393 |0.9529 |0.045|
|Light Gradient Boosting Machine |0.9773 |0.9857 |**0.9842** |0.9849 |0.412|
|Linear Discriminant Analysis |0.9360 |**1** |0.9230 |0.9595 |0.028|
|Logistic Regression |0.8773 |0.9893 |0.8671 |0.9239 |0.653|
|Naive Bayes |0.9413 |0.9768 |0.9470 |0.9615 |0.027|
|Quadratic Discriminant Analysis |0.9587 |0.9679 |0.9770 |0.9723 |0.028|
|Random Forest Classifier |0.9707 |0.9840 |0.9772 |0.9805 |0.361|
|Ridge Classifier |0.8880 |0.9893 |0.8787 |0.9302 |0.043|
|SVM - Linear Kernel |0.9160 |0.9821 |0.9132 |0.9461 |0.044|

### Benchmark Results on MNIST data set
|*Model*|Accuracy|Recall|Precision|F1score|TT (s)|
|:---|:---:|:---:|:---:|:---:|:---:|
|QSVM |0.1640 |0.1861 |0.1158 |0.0585 |1624.068|
|Ada Boost Classifier |0.3213 |0.3213 |0.1581 |0.2070 |0.138|
|Decision Tree Classifier |0.4800 |0.4800 |0.4894 |0.4714 |0.035|
|Dummy Classifier |0.1227 |0.1227 |0.0151 |0.0268| 0.027|
|Extra Trees Classifier |0.4773 |0.4773 |0.4806 |0.4687 |0.220|
|Extreme Gradient Boosting |0.4760 |0.4760 |0.4935 |0.4703 |0.461|
|Gradient Boosting Classifier |0.4853 |0.4853 |0.4879 |0.4761 |1.474|
|K Neighbors Classifier |0.4960 |0.4960 |**0.4936** |**0.4809** |0.074|
|Light Gradient Boosting Machine |0.4787 |0.4787 |0.4859 |0.4722 |1.402|
|Linear Discriminant Analysis |0.4720 |0.4720 |0.3871 |0.3891 |0.032|
|Logistic Regression |0.4880 |0.4880 |0.3856 |0.3983 |0.077|
|Naive Bayes |0.5133 |0.5133 |0.4580 |0.4495 |0.048|
|Quadratic Discriminant Analysis |**0.5200** |**0.5200** |0.4740 |0.4625 |0.030|
|Random Forest Classifier |0.4787 |0.4787 |0.4812 |0.4697 |0.259|
|Ridge Classifier |0.4080 |0.4080 |0.2780 |0.3071 |**0.027**|
|SVM - Linear Kernel |0.3720 |0.3720 |0.2415 |0.2739 |0.044|

### Benchmark Results on Circle data set
|*Model*|Accuracy|Recall|Precision|F1score|TT (s)|
|:---|:---:|:---:|:---:|:---:|:---:|
|QSVM |0.5547 |**0.5562** |0.5658 |0.5386 |2313.797|
|Ada Boost Classifier |0.5767 |0.4985 |**0.5793** |0.5350 |0.138|
|Decision Tree Classifier |0.5473 |0.5462 |0.5362 |0.5406 |0.029|
|Dummy Classifier |0.5107 |0 |0 |0 |**0.023**|
|Extra Trees Classifier |0.5480 |0.5353 |0.5362 |0.5345 |0.335|
|Extreme Gradient Boosting |0.5493 |0.5315 |0.5410 |0.5354 |0.071|
|Gradient Boosting Classifier |**0.5773** |0.5093 |0.5785 |0.5411 |0.218|
|K Neighbors Classifier |0.5607 |0.5408 |0.5521 |**0.5459** |0.051|
|Light Gradient Boosting Machine |0.5540 |0.5204 |0.5466 |0.5328 |0.677|
|Linear Discriminant Analysis |0.4913 |0.3925 |0.4771 |0.4297 |0.046|
|Logistic Regression |0.4913 |0.3925 |0.4771 |0.4297 |0.048|
|Naive Bayes |0.4967 |0.4210 |0.4839 |0.4492 |0.029|
|Quadratic Discriminant Analysis |0.4953 |0.4306 |0.4809 |0.4535 |0.025|
|Random Forest Classifier |0.5527 |0.5489 |0.5411 |0.5440 |0.329|
|Ridge Classifier |0.4913 |0.3925 |0.4771 |0.4297 |0.025|
|SVM - Linear Kernel |0.5213 |0.3930 |0.4134 |0.3924 |0.027|