# Protein-comparison
Given a list consisting of data about the amount of protein in different cereals i.e. list[i] represents the amount of protein in ith cereal.

Interpret the number of cereals for different amounts of protein available in any cereal using a bar graph.

The label of the x-axis should be "Protein amount in grams".
The label of the y-axis should be "Number of cereals".
The title should be "Protein comparison".
The color of the bars should be green 'g'.
Note: The output is verified by using the attributes of the created plot like labels and all the requirements that are mentioned above. No need to show() the plot. Here the backend will automatically print the heights of the first and last bars of the created bar plot and the string representing your solution's status.

Input Format:

A list

Output Format:

Multiple strings.

Two numbers represeting the heights of first and last bar

The output generated will be ‘Woo-hoo the plot is perfect.’ along with the heights of first and last bars, if the created plot satisfies all the mentioned conditions.
If in case any of the required characteristics is not followed by the created scatter plot a sentence representing the error will be printed.
Sample Input:

[4, 3, 4, 4, 2, 2, 2, 3, 2, 3, 1, 6, 1, 3, 1, 2, 2, 1, 1, 3, 3, 2, 2, 2, 2, 1, 3, 3, 3, 1, 2, 1, 3, 3, 3, 1, 3, 1, 2, 3, 2, 4, 2, 4, 4, 4, 3, 2, 2, 3, 3, 3, 3, 3, 1, 2, 4, 5, 3, 3, 2, 1, 2, 2, 3, 3, 2, 6, 2, 2, 3, 3, 2, 1, 3, 3, 2] 

![image](https://github.com/user-attachments/assets/74f44a85-3b32-4b5a-b082-9b561508c009)


Source Code: 
import numpy as np
import matplotlib.pyplot as plt

protein = eval(input())

fig = plt.figure()

# Count the frequency of each protein value
unique, counts = np.unique(protein, return_counts=True)

# Create the bar plot
bars = plt.bar(unique, counts, color='g')

# Add the xlabel
plt.xlabel("Protein amount in grams")

# Add the ylabel
plt.ylabel("Number of cereals")

# Add the title
plt.title("Protein comparison")
