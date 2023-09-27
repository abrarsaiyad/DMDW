# DMDW
#Program 1
# Plot a boxplot for ͞price͟ vs ͞cut͟ from 
the dataset ͞diamond.csv͟ ͘͟ Which of the categories 
under ͞cut͟ have the highest median price?
import pandas as pd
import matplotlib.pyplot as plt
# Read the dataset
df = pd.read_csv("diamonds.csv")
print(df.head())
# Create the boxplot
plt.figure(figsize=(8, 6))
df.boxplot(column='price', by='cut')
plt.xlabel('Cut')
plt.ylabel('Price')
plt.title('Price vs Cut')
plt.suptitle('') # Remove the default title
plt.show()
#Program 2
'''Create a frequency table (one-way table) for the variable ͞cut͟ from 
the dataset ͞diamond.csv͟ ͘͟ What is the frequency for 
the cut type ͞Ideal͟'͍͟''
import pandas as pd
# Read the dataset
df = pd.read_csv("diamonds.csv")
# Create the frequency table
frequency_table = df['cut'].value_counts()
# Print the frequency table
print(frequency_table)
# Access the frequency for the cut type "Ideal"
ideal_frequency = frequency_table['Ideal']
print("Frequency for cut type 'Ideal':", ideal_frequency)
#Program 3
# Show the subplot of the diamond carat weight distribution.
import pandas as pd
import matplotlib.pyplot as plt
# Read the dataset
df = pd.read_csv("diamonds.csv")
print(df['carat'])
# Create a subplot with 1 row and 2 columns
fig, axs = plt.subplots(1, 2, figsize=(12, 6))
# Plot the histogram of carat weight on the first subplot
axs[0].hist(df['carat'], bins=30, edgecolor='black')
axs[0].set_xlabel('Carat Weight')
axs[0].set_ylabel('Frequency')
axs[0].set_title('Carat Weight Distribution')
# Plot the boxplot of carat weight on the second subplot
axs[1].boxplot(df['carat'], vert=False)
axs[1].set_yticklabels('')
axs[1].set_xlabel('Carat Weight')
axs[1].set_title('Carat Weight Distribution')
# Adjust the spacing between subplots
plt.subplots_adjust(wspace=0.3)
# Show the plot
plt.show()
#Program 4
# Show the subplot of diamond depth distribution.
import pandas as pd
import matplotlib.pyplot as plt
# Read the dataset
df = pd.read_csv("diamonds.csv")
print(df['depth'])
# Create a subplot with 1 row and 2 columns
fig, axs = plt.subplots(1, 2, figsize=(12, 6))
# Plot the histogram of diamond depth on the first subplot
axs[0].hist(df['depth'], bins=30, edgecolor='black')
axs[0].set_xlabel('Depth')
axs[0].set_ylabel('Frequency')
axs[0].set_title('Diamond Depth Distribution')
# Plot the boxplot of diamond depth on the second subplot
axs[1].boxplot(df['depth'], vert=False)
axs[1].set_yticklabels('')
axs[1].set_xlabel('Depth')
axs[1].set_title('Diamond Depth Distribution')
# Adjust the spacing between subplots
plt.subplots_adjust(wspace=0.4)
# Show the plot
plt.show()
