# Open the input file and read its contents
with open("input.txt", "r") as file:
    content = file.read()

# Modify the content (e.g., convert to uppercase)
modified_content = content.upper()

# Write the modified content to a new file
with open("modified_input.txt", "w") as new_file:
    new_file.write(modified_content)

print("Modified file created: modified_input.txt")
# File-Read

Error Handling Program
filename = input("Enter the filename to read: ")

try:
    with open(filename, 'r') as file:
        content = file.read()
        print("File content:\n")
        print(content)

except FileNotFoundError:
    print("Error: File not found.")

except PermissionError:
    print("Error: You do not have permission to read this file.")

except IOError:
    print("Error: An unexpected error occurred while reading the file.")
