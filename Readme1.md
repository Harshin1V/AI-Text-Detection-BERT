## Oversampling Subsets:

For each label, it extracts a subset (label_subset) from the original DataFrame (df) that contains only rows where the label_column value matches the current label.
To address the imbalance, it creates an oversampled subset (oversampled_subset) using the sample function:
The desired number of samples (n) is calculated as the difference between the maximum count (max_count) and the current label's count (count). This ensures enough samples are added for the current label to reach the maximum count.
The replace=True argument allows sampling with replacement, meaning the same data point can be selected multiple times.
random_state=42 sets a seed for the random number generator, ensuring reproducibility of the oversampling process if you run the code again.
