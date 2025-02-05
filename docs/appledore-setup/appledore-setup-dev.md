# Components of GraphMatrix.hpp
1. [Setting up Appledore](#1-setting-up-appledore-for-development)
2. [Building Example](#2-building-examples)
3. [Running Tests](#3-running-tests)


# 1. Setting Up **Appledore** for Development  

## 1.1 Fork the Repository  
First, create a fork of the Appledore repository:  
1. Go to the [Appledore GitHub repository](https://github.com/SharonIV0x86/Appledore).  
2. Click the **Fork** button at the top right and create your own fork.  

For more details on forking a repository, check [GitHub’s documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).  

## 1.2 Clone Your Fork  
Once you've forked the repository, clone it to your local machine:  
```sh
git clone https://github.com/your-username/Appledore.git
cd Appledore
```  
Alternatively, you can download it as a ZIP file if you prefer. Learn more about working with forks [here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo).  

## 1.3 Create a New Branch  
Always work on a separate branch when making changes. Use the following naming conventions:  

- **For bug fixes**:  
  ```sh
  git checkout -b fix/your-fix-name
  ```  
- **For new features**:  
  ```sh
  git checkout -b feat/your-feature-name
  ```  

This ensures clarity and organization in your contributions.


> **Note:** Before pushing your changes, ensure that your current branch is up to date with the ``main`` branch of the **Appledore** repository. Save your work, then run ``git pull origin upstream`` to fetch the latest changes from the main repository and avoid any conflicts.

## 1.4 Push your changes
Push the changes to your fork and open a pull request.
```sh
git pull origin name-of-your-branch
```


# 2. Building Examples  
Now that you've set up the repository, it's time to build and run some examples.

## 2.1 Navigate to the Examples Directory  
```sh
cd examples
```

## 2.2 Create a Build Directory  
To keep the build files organized, create a `build` folder and move into it:  
```sh
mkdir build && cd build
```

## 2.3 Generate Build Files Using CMake  
```sh
cmake ..
```

## 2.4 Compile the Examples  
Use `make` to compile the examples:  
```sh
make
```

## 2.5 Run the Examples  
Once compiled, you can execute the example programs as needed.

## Cleaning Up  
If you need to remove the compiled example executables, use the following command:  
```sh
make clean
```

This will remove all generated binary files while keeping the build system intact.



# 3. Running Tests  
Before contributing, it's essential to run the tests and ensure all tests pass successfully.

## 3.1 Running Tests for `GraphMatrix.hpp`  
Navigate to the `tests` directory:  
```sh
cd tests
```

### Compile the Test Suite  
To run tests for `GraphMatrix.hpp`, compile the `test_suite.cpp` file:  
```sh
g++ test_suite.cpp -o test_suite
```

### Running Specific Tests  
Once compiled, you can specify which component to test. For example, to run tests for `GraphMatrix`, use:  
```sh
./test_suite graph-matrix
```
Here, the `graph-matrix` flag indicates the component under test.

Always ensure all tests pass before submitting your contributions.
