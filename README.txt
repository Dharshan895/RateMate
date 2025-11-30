Restaurant Rating Predictor

Predict the aggregate ratings of restaurants based on location, cuisines, and other key features. This model uses machine learning techniques to handle high-cardinality and multi-label categorical data, producing accurate predictions of restaurant ratings.

Dataset Features

The dataset contains the following columns:

Restaurant ID, Restaurant Name – Identifiers (not used for modeling)

Country Code, City, Locality, Locality Verbose, Address, Longitude, Latitude – Geographic features

Cuisines – Types of food offered (multi-label)

Average Cost for two, Currency, Price range – Pricing features

Has Table booking, Has Online delivery, Is delivering now, Switch to order menu – Service features

Aggregate rating, Rating color, Rating text, Votes – Target and descriptive ratings

Preprocessing Highlights

City – Target encoded using historical ratings

Locality – First two sub-localities extracted and multi-label encoded or target encoded

Cuisines – Multi-label TF-IDF encoding

Numeric & Boolean features – Used directly after cleaning

Dropped features – Restaurant Name, Restaurant ID, Address (too noisy or identifiers)

Modeling

Algorithm: Random Forest Regressor (tree-based, robust to sparse/high-cardinality features)

Target: Aggregate rating

Evaluation Metrics: R² score, Mean Squared Error (MSE)

Designed to avoid data leakage, with proper train/test splitting and encoding.

Purpose

Predict ratings for existing or new restaurants

Analyze which features (location, cuisine, services) influence ratings most

Can support restaurant recommendation systems or business analysis
