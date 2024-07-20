class Task:
def _init_(self, name, due_date):
self.name = name,self,due_date = due_date,self.completed = False

def complete(self):
self.completed = True

class ToDoList:
def _init_(self):
self.tasks = []

def add_task(self, task):
self.tasks.append(task)

def complete_task(self, task_name):
for task in self.tasks:
if task.name == task_name:
task.complete()
return True
return False

def list_tasks(self):
for task in self.tasks:
status = 'completed' if task.completed else 'Not Completed'
print(f"{task.name} (Due: {task.due_date}) - {status}")
