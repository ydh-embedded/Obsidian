# Compile each source file

```python

import os
import glob



working_directory = os.getcwd()
output_directory = r"C:\working-directory\jdk\output"
source_root = r"C:\working-directory\jdk"
java_root = r"C:\working-directory\jdk\JDK21\jdk-21.0.2\bin"


os.environ["PATH"] = java_root + ";" + os.environ["PATH"]   # Add java_root to the PATH environment variable


os.chdir(source_root)                                       # Change to the source root directory


source_files = glob.glob("**/*.java", recursive=True)       # Find all java files in all subdirectories


for file in source_files:                                   # Compile each source file
    print(f"Compiling file {file}...")
    # Replace 'javac' with the full path to the javac.exe if necessary
    # os.system(f'javac.exe "{file}" -d "{output_directory}"')
```