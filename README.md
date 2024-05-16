# python-date
# 1.3 Function to measure the runtime of the algorithm
def measure_runtime(problem_size):
    start_time = time.time()  # Start the timer

    work = 1
    for x in range(problem_size):
        work += 5
        work -= 5

    end_time = time.time()  # End the timer
    return end_time - start_time  # Calculate the runtime

def main():
    problem_sizes = [1000000, 3000000, 9000000, 27000000]  # Define problem sizes
    print("Problem Size\t\tSeconds")  # Print header

    # Iterate over each problem size
    for size in problem_sizes:
        runtime = measure_runtime(size)  # Measure the runtime
        print(f"{size:12,}\t{runtime:.4f}")  # Print the results

if __name__ == "__main__":
    main()
