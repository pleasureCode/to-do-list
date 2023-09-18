# to-do-list
A new repository created via Python script


---

Sure! Here's an example code in Python to create a simple to-do list:

```python
# Create an empty list to store the tasks
tasks = []

# Function to add a task to the list
def add_task():
    task = input("Enter the task: ")  # Get task from user
    tasks.append(task)  # Add task to the list
    print("Task added successfully!")

# Function to remove a task from the list
def remove_task():
    task = input("Enter the task to remove: ")  # Get task from user
    if task in tasks:
        tasks.remove(task)  # Remove task from the list
        print("Task removed successfully!")
    else:
        print("Task not found in the list.")

# Function to print the current tasks in the list
def print_tasks():
    print("Current tasks:")
    if tasks:
        for index, task in enumerate(tasks, start=1):
            print(f"{index}. {task}")
    else:
        print("No tasks found.")

# Main program loop
while True:
    print("\n--- TO-DO LIST ---")
    print("1. Add task")
    print("2. Remove task")
    print("3. Print tasks")
    print("4. Exit")

    choice = input("Enter your choice (1-4): ")

    if choice == "1":
        add_task()
    elif choice == "2":
        remove_task()
    elif choice == "3":
        print_tasks()
    elif choice == "4":
        print("Exiting program...")
        break
    else:
        print("Invalid choice. Please try again.")
```

Explanation step by step:
1. We start by creating an empty list called `tasks` to store the tasks.
2. Next, we define three functions - `add_task()`, `remove_task()`, and `print_tasks()` - to perform the corresponding operations.
3. The `add_task()` function prompts the user to enter a task and adds it to the `tasks` list.
4. The `remove_task()` function asks the user to enter a task to remove and checks if it exists in the `tasks` list. If found, it removes the task; otherwise, it displays a message indicating that the task was not found.
5. The `print_tasks()` function displays the current tasks in the `tasks` list. If there are no tasks, it displays a message indicating that no tasks were found.
6. The main program loop repeatedly displays a menu of options for the user to choose from.
7. Based on the user's choice, the corresponding function is called to perform the desired operation.
8. If the user chooses option 4, the program displays a goodbye message and breaks out of the loop, thus ending the program.
9. If the user enters an invalid choice, an appropriate message is displayed.
10. The program continues to loop until the user chooses to exit.

That's it! You now have a basic to-do list program in Python.