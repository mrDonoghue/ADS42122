# Bare minimum experiment for comparing algorithms:
* test each algorithm on a range of input sizes that spans several orders of magnitude (the longest input size should take *at least* 10 seconds for the slower of the algorithms)
* Compare the algorithms across all of these input sizes, often easiest with a plot
* Note that later in this file, I provide code for generating plots given files with data
# General plan
* make a function/method that conducts the whole experiment for a single algorithm when given:
  - a list/array of the input sizes
  - the function/method to time
  - where to record the data
* this experiment function/method will need to iterate through the array/list of sizes and:
  - make a random array of the right size
  - start a "stopwatch"
  - run the given sorting function/method
  - immediately stop the "stopwatch"
  - record this datapoint as "SIZE TIME" (replacing SIZE and TIME with the actual numbers) in a file
* this plan involves using a function/method as an argument to a function/method. Since you've never done this, I'm providing an example/skeleton to build off of: See [this file for the Java version](JavaSortingExample.md)  or [this file for the Python version](PythonSortingExample.md)


# Plotting
Make a new file named `plot.py` and paste the below code in it:
```python
from matplotlib import pyplot as plt

plt.show()
def plot_files(files):
  for file in files:
    name = file.split(".")[0]
    with open(file, "r") as f:
      ns, times = list(zip(*
        [
          [
            float(num) 
            for num in line.split()
          ]
          for line in f.readlines()
        ]
      ))
    plt.plot(ns, times,label=name)
  plt.title("Sorting time vs array size")
  plt.legend()
  plt.show()


def main():
  print("Input the name of each file. Enter a blank line when done.")
  done = False
  files =[]
  while not done:
    file = input()
    if len(file) == 0:
      done = True
    else:
      files.append(file)
  plot_files(files)


if __name__ == "__main__":
  main()
```


# How to use my plotting code
* Create a file for each line you want in the plot
  * the name of the file before the extension will be used as the label in the legend of the plot
  * the file should have a series of lines where each line corresponds to a single data-point for a single sorting algorithm
  * each line should be two numbers separated by a space
  * the first number should be the array size
  * the second number should be the time it took to sort
Open the Shell tab and input this command:
`python plot.py`