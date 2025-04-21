# Week-4-Python-Assignment
This is my Python assignment solution
def file_read_write():
    try:
        # 🧪 Ask for input file
        input_file = input("Enter the name of the file to read: ")

        # 🗂 Try opening and reading the file
        with open(input_file, "r") as file:
            content = file.read()
            print("\nOriginal content:")
            print(content)

        # 🛠 Modify content (make it uppercase)
        modified_content = content.upper()

        # 📝 Write to new file
        output_file = "modified_" + input_file
        with open(output_file, "w") as file:
            file.write(modified_content)

        print(f"\nModified content written to '{output_file}'.")

    except FileNotFoundError:
        print("❌ Error: The file does not exist.")
    except IOError:
        print("❌ Error: Could not read/write the file.")
    except Exception as e:
        print(f"⚠️ An unexpected error occurred: {e}")

# ▶ Run the function
file_read_write()
