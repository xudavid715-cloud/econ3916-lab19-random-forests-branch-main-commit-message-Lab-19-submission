Tree-Based Models: Random Forests

Objective

I compared four ways to predict median house values in California and examined which features the random forest relied on most.

Methodology

I trained a single decision tree, OLS, scaled Ridge regression and a random forest on the same training rows and evaluated them on the same held-out rows.

I compared the importance each feature earned from training splits with the loss in test R² when I shuffled that feature.

I used cross-validation on the training set to choose the forest's maximum depth and the number of features available at each split.

I tested an AI-generated chart function over two rounds. I compared its rankings and unrounded scores with the lab's calculations, then repeated the check with a different tree, different rows and reversed columns.

Key findings

The single tree scored 0.6228 on test R², Ridge scored 0.5758 and the original forest scored 0.8046. Averaging trees improved predictions on unseen rows. The tuned forest had the best test R² at 0.8094.

Latitude earned 0.0890 of the forest's total impurity reduction. Shuffling it lowered test R² by 0.4427 on average. The first number measures its share of the training splits' error reductions. The second shows how much prediction suffered when the forest received the wrong latitude for each test row.

In both rounds, the chart function reproduced the reference rankings and scores without fitting another forest. The chart placed the largest decrease in test R² at the top.
