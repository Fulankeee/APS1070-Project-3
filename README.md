# APS1070 Project 3 - PCA and SVD
-	Use of Panda: pd.DataFrame; pd.read_csv; pd.merge
-	Use of Numpy: np.dot; np.arange; np.linalg.eigh
-	Use of matplotlib.pyplot: plt.plot; matplotlib.gridspec (bar and line plot); plt.Circle
-	Use of sklearn:
sklearn.model_selection - mean_squared_error
sklearn.preprocessing – StandardScaler - inverse_transform
sklearn.metrics - roc_auc_score - f1_score - precision_score - recall_score
-	Python Basics: .iloc; .loc; .argsort (tell the order to arrange the elements to achieve a sorted array)

Part 1 - Data Cleaning and Visualization
-	Plot time series of the selected countries with standardized and non-standardized data.
-	Deal with the date where the index column is necessary (e.g. Country name here): 
	Create a new column and let it be df.index
	Reset/Remove the index by df.reset_index (drop = T)

Part 2 – PCA Application (Need standardization)
-	Write a function get_sorted_eigen() that gets the covariance matrix
-	Plot the first 16 principal components (Eigenvectors) as a time series.

Part 3 – Reconstruction
-	Plot of origin time series for a specific country
-	Plot the incremental reconstruction of the original time-series for the specified country in a single plot. (compute the reconstruction for the standardized time-series first, and then scale it back to the original using the StandardScaler)
-	Plot the residual error for your best reconstruction with respect to the original time-series.
-	Plot the RMSE of the reconstruction as a function of the number of included components.

Part 4 – SVD (No need for standardization)
-	Repeat the operation in part 3 using SVD
-	SVD directly decomposes a matrix into its constituent parts without requirments to scale the data.

Part 5 – PCA and SVD comparison on a new dataset
-	SVD reaches satisfactory accuracy with fewer components compared to PCA. 
-	PCA requires calculating the covariance matrix and thus benefits from standardization to ensure the data is well-scaled and results are unbiased. In contrast, SVD doesn’t rely on the covariance matrix and can operate without standardization, making it computationally simpler.
