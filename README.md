# Clustering-to-Classification

Context: Oftentimes we receive a data set that is not yet suited for supervised machine learning because it lacks the necessary target. In these cases, we can sometimes use clustering to extrapolate categories and then use the cluster labels for downstream classification.

'User Knowledge.xls' contains data about student's knowledge status about the subject of Electrical DC Machines. It was colelcted in 2009 as part of research thesis of Dr. Hamdi Tolga Kahraman of Turkey. The data has 5 columns in the first sheet named Main and the second sheet contains metadata about the data in Main.

'Data Science Code Challenge.ipynb' is a notebook containing steps of application of Machine Learning techniques to the above data for clustering and classification.

'Pipeline.png' shows the sketched-out diagram (made using Google Draw) of a pipeline that integrates the above steps so that the model could be rebuilt on demand in a production environment. The steps are listed below:

1) Clustering is performed on the historical data and the data is labelled with clusters.
2) Multiclass classification Machine Learning models are applied on the training data (larger subset of historical data).
3) The models are evaluated on test data (rest of the historical data).
4) The best model is selected and implemented for predicting the class of new data.
5) The new data is added to the historical data and the existing models are updated.