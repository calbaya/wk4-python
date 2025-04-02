# wk4-python

# Question 1
# Error handling

filename = ("Enter filename: ")

try:
    with open("filename", "r") as file:
        content = file.read()
        print(content)

except FileNotFoundError:
    print("Error: File does not exist")
except PermissionError:
    print("Error: You have no acces to this file")


# File Read & Write Challenge 
# Question 2

with open("input.txt", "r") as input_file:
    content = input_file.read()

modified = content.upper()
with open("output.txt", "w") as output_file:
   output_file.write(modified)

print("Operation complete. check 'output.txt'.")
