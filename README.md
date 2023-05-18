# Write-a-Python-program-to-read-first-n-lines-of-a-file
def read_first_n_lines(file_path, n):
    try:
        with open(file_path, 'r') as file:
            lines = file.readlines()
            for line in lines[:n]:
                print(line.strip())
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while reading the file.")

# Example usage
file_path = 'path/to/your/text/file.txt'  # Replace with the actual file path
num_lines = 5  # Number of lines to read
read_first_n_lines(file_path, num_lines)

