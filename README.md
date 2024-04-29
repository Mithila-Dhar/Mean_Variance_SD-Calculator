import math

def mean(numbers):
    return sum(numbers) / len(numbers)

def variance(numbers):
    mean_val = mean(numbers)
    return sum((x - mean_val) ** 2 for x in numbers) / len(numbers)

def standard_deviation(numbers):
    return math.sqrt(variance(numbers))

# Function to take input from the user
def take_input():
    data = []
    n = int(input("Enter the number of elements: "))
    print("Enter the elements:")
    for i in range(n):
        element = float(input())
        data.append(element)
    return data

# Example usage:
data = take_input()
print("Mean:", mean(data))
print("Variance:", variance(data))
print("Standard Deviation:", standard_deviation(data))
