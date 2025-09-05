tasks = []

def show_tasks():
    print("\nYour Tasks:")
    for i, task in enumerate(tasks, 1):
        print(f"{i}. {task}")

def add_task():
    task = input("Enter task: ")
    tasks.append(task)
    print("Task added.")

def delete_task():
    show_tasks()
    task_num = int(input("Enter task number to delete: "))
    if 0 < task_num <= len(tasks):
        removed = tasks.pop(task_num-1)
        print(f"Removed task: {removed}")
    else:
        print("Invalid task number.")

while True:
    print("\nTo-Do List Menu: show, add, delete, quit")
    choice = input("Enter choice: ").lower()
    if choice == 'show':
        show_tasks()
    elif choice == 'add':
        add_task()
    elif choice == 'delete':
        delete_task()
    elif choice == 'quit':
        break
    else:
        print("Invalid choice.")

