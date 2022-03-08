```python
def some_sorting_function(arr):
  pass
  # DEFINITELY doing sorting


def conduct_experiment(sizes, sort, filename):
  # TODO: open file
  for size in sizes:
    arr = random_arr(size)
    # TODO: begin "stopwatch"
    sort(arr)
    # TODO: end stopwatch
    # TODO: record time
  # TODO: close file

def main():
  sizes = [10, 30, 100, 300, 1000]
  conduct_experiment(sizes, some_sorting_function, "sort0.tab")
```