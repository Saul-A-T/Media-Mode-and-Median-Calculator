# Media-Mode-and-Median-Calculator
A simple calculator for the Media, Mode and Median

print("Welcome to Mean, Median, and Mode Calculator")
print(" Please enter the numbers to calculate")

numbers = input("Please enter the numbers separated by spaces: ")

numbers = [float(num) for num in numbers.split()]

mean = sum(numbers) / len(numbers)

sorted_numbers = sorted(numbers)
n = len(sorted_numbers)

if n % 2 == 1:
    median = sorted_numbers[n // 2]
else:
    median = (sorted_numbers[n // 2 - 1] + sorted_numbers[n // 2]) / 2

counts = Counter(numbers)
highest = max(counts.values())

if highest == 1:
    mode = "There is no mode"
else:
    mode = [num for num, count in counts.items() if count == highest]

# Add Results

print("\nResults")
print("----------------")
print("----------------")
print(f"Numbers : {sorted_numbers}")
print(f"Mean : {mean:.2f}")
print(f"Median : {median}")
print(f"Mode : {mode}")
print("----------------")
print("----------------")
