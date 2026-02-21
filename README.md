Project Overview

This project investigates whether heart disease risk naturally emerges through unsupervised learning.

Using cardiometabolic patient data containing biomarker measurements and behavioral risk factors, I systematically evaluated multiple clustering paradigms to determine:

	•	Do stable latent patient subgroups exist?
	•	Do those subgroups align with diagnosed heart disease outcomes?
	•	Is heart disease risk cluster-separable in feature space?

Rather than assuming clustering would succeed, this study rigorously tests that assumption.

⸻

Methodological Approach

Preprocessing

	•	Continuous features standardized using StandardScaler
	•	Binary indicators retained as encoded variables
	•	Target label excluded from clustering procedures

Algorithms Evaluated

	•	K-Means
	•	Agglomerative (Ward linkage)
	•	DBSCAN
	•	Fuzzy C-Means
	•	Gaussian Mixture Models (multiple covariance types)
	•	CURE (Clustering Using Representatives)

Validation Metrics

	•	Silhouette Score (internal cohesion & separation)
	•	Davies–Bouldin Index (cluster compactness)
	•	Adjusted Rand Index (alignment with heart disease labels)
	•	Normalized Mutual Information (external agreement)

⸻

Key Findings

	•	All clustering paradigms consistently identified two dominant latent segments.
	•	The dominant structure reflects lifestyle and metabolic variation, not clinical diagnosis.
	•	External validation (ARI ≈ 0 across methods) indicates that heart disease status does not align with geometric or density-based partitions.
	•	Clustering is insufficient for diagnostic prediction in this dataset.

⸻

Interpretation

The results suggest that:

	•	Cardiometabolic features exhibit stable latent structure.
	•	However, heart disease risk is not cluster-separable.
	•	Disease outcomes likely depend on nonlinear interactions among risk factors rather than Euclidean similarity.
