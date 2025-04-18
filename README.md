You want to create polynominal and interaction features, Even though some choose to create polynomial and interaction features manually, scikit-learn offers a
built-in method, The degree parameter determines the maximum degree of the polynomial. For example, degree=2 will
create new features raised to the second power, while degree=3 will create new features raised to the second and third power, Furthermore, by default PolynomialFeatures
includes interaction features, We can restrict the features created to only interaction features by setting interaction_only to True, Polynomial features are often created 
when we want to include the notion that there exists a nonlinear, relationship between the features and the target. For example, we might suspect that the effect of age on
the probability of having a major medical condition is not constant over time but increases as age
increases. We can encode that nonconstant effect in a feature, x, by generating that feature’s higherorder forms (x
2
, x
3
, etc.).
Additionally, often we run into situations where the effect of one feature is dependent on another
feature. A simple example would be if we were trying to predict whether or not our coffee was sweet
and we had two features: 1) whether or not the coffee was stirred and 2) if we added sugar. Individually,
each feature does not predict coffee sweetness, but the combination of their effects does. That is, a
coffee would only be sweet if the coffee had sugar and was stirred. The effects of each feature on the
target (sweetness) are dependent on each other. We can encode that relationship by including an
interaction feature that is the product of the individual features
