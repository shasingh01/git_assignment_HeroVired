# git_assignment_HeroVired

# Git Assignment: Hero Vired

This repository is a part of the Hero Vired Git assignment. It contains a simple Python application called `CalculatorPlus` that performs basic arithmetic operations and calculates areas for geometric shapes. The project also demonstrates the use of Git features such as branching, merging, Git LFS, and stashing.

## Table of Contents

1. [CalculatorPlus](#calculatorplus)
    - [Features](#features)
    - [Usage](#usage)
2. [Git LFS Integration](#git-lfs-integration)
    - [Steps to Use Git LFS](#steps-to-use-git-lfs)
3. [Geometry Calculator](#geometry-calculator)
    - [Features](#geometry-calculator-features)
    - [Workflow Steps](#workflow-steps)
4. [Contributing](#contributing)
5. [License](#license)

## CalculatorPlus

`CalculatorPlus` is a Python application that provides basic arithmetic operations: addition, subtraction, multiplication, and division. Additionally, it includes a feature to calculate the square root of a number.

### Features

- Addition
- Subtraction
- Multiplication
- Division (with division by zero handling)
- Square root calculation

### Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/git_assignment_HeroVired.git
    cd git_assignment_HeroVired
    ```

2. Run the `calculator.py` script:
    ```bash
    python3 calculator.py
    ```

Example output:
```plaintext
16 + 4 = 20
16 - 4 = 12
16 * 4 = 64
16 / 4 = 4.0
The square root of 25 = 5.0


2. Git LFS Integration
This project demonstrates the use of Git LFS (Large File Storage) for handling large binary files efficiently.

Steps to Use Git LFS
Install Git LFS:

Follow the installation instructions from Git LFS.
Initialize Git LFS in the repository:
git lfs install

git lfs track "*.bin"
git add .gitattributes
git commit -m "Track binary files with Git LFS"

git add largefile.bin
git commit -m "Add large binary file using Git LFS"
git push origin lfs

Clone the repository on another machine and verify the large files are downloaded:

git clone https://github.com/shasingh01/git_assignment_HeroVired.git
cd git_assignment_HeroVired
git checkout lfs


3.Geometry Calculator
The GeometryCalculator class provides methods to calculate the area of a circle and a rectangle. This section also demonstrates how to use Git stash to manage incomplete changes for multiple features.

Geometry Calculator Features
Calculate the area of a circle
Calculate the area of a rectangle
Workflow Steps
Create a new branch for the geometry calculator:

git checkout -b geometry-calculator

import math

class GeometryCalculator:
    def calculate_circle_area(self, radius):
        return math.pi * radius ** 2

    def calculate_rectangle_area(self, length, width):
        return length * width

if __name__ == "__main__":
    calculator = GeometryCalculator()

    # TODO: Implement the feature to calculate the area of a circle
    # radius = 5
    # print(f"The area of the circle with radius {radius} = {calculator.calculate_circle_area(radius)}")

    # TODO: Implement the feature to calculate the area of a rectangle
    # length = 10
    # width = 6
    # print(f"The area of the rectangle with length {length} and width {width} = {calculator.calculate_rectangle_area(length, width)}")
Work on the Circle Area Feature:

git checkout -b feature/circle-area

Uncomment and implement the circle area calculation

git stash

Work on the Rectangle Area Feature:

git checkout -b feature/rectangle-area

Uncomment and implement the rectangle area calculation
if __name__ == "__main__":
    calculator = GeometryCalculator()

    # Implement the feature to calculate the area of a rectangle
    length = 10
    width = 6
    print(f"The area of the rectangle with length {length} and width {width} = {calculator.calculate_rectangle_area(length, width)}")
git stash

Complete and Push Circle Area Feature:

git checkout feature/circle-area
git stash pop

git add geometry_calculator.py
git commit -m "Complete circle area feature"
git push origin feature/circle-area
Complete and Push Rectangle Area Feature:
Create Pull Requests:

Create pull requests for feature/circle-area and feature/rectangle-area branches to the dev branch on GitHub.
Request code reviews from team members.
Merge Approved Pull Requests:

After receiving approval, merge the pull requests into the dev branch.
Merge the dev branch into the main branch.
Contributing
Fork the repository.
Create a new branch (git checkout -b feature/new-feature).
Make your changes and commit them (git commit -m 'Add some feature').
Push to the branch (git push origin feature/new-feature).
Create a new Pull Request.

Conclusion
This project demonstrates the fundamental concepts of Git, including branching, merging, stashing, and integrating Git LFS for handling large binary files. By working through the CalculatorPlus and GeometryCalculator applications, you have seen how to manage different features and fix critical bugs while keeping the workflow organized and efficient.

The key takeaways from this project include:

Branching and Merging: Efficiently managing different features and changes using branches and pull requests.
Git LFS: Handling large files without clogging up the repository and maintaining performance.
Stashing: Temporarily saving incomplete changes to switch contexts without losing progress.
Collaboration: Engaging in code reviews and collaborative development to ensure code quality and integrity.


