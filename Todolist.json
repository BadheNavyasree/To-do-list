import tkinter as tk

def add_task():
    task = entry.get()
    if task != "":
        listbox.insert(tk.END, task)
        entry.delete(0, tk.END)

def delete_task():
    try:
        selected = listbox.curselection()[0]
        listbox.delete(selected)
    except:
        pass

def toggle_done():
    try:
        selected = listbox.curselection()[0]
        task = listbox.get(selected)

        if task.startswith("✅ "): 
            task = task[2:]          
        else:                       
            task = "✅ " + task

        listbox.delete(selected)    
        listbox.insert(selected, task)
    except:
        pass


root = tk.Tk()
root.title("To-Do List")
root.geometry("300x400")


entry = tk.Entry(root, width=25, font=("Arial", 14))
entry.pack(pady=10)


add_btn = tk.Button(root, text="Add Task", command=add_task)
add_btn.pack(pady=5)


listbox = tk.Listbox(root, width=30, height=10, font=("Arial", 12))
listbox.pack(pady=10)


btn_frame = tk.Frame(root)
btn_frame.pack(pady=5)

del_btn = tk.Button(btn_frame, text="Delete Task", command=delete_task)
del_btn.grid(row=0, column=0, padx=5)

done_btn = tk.Button(btn_frame, text="Mark/Unmark Done", command=toggle_done)
done_btn.grid(row=0, column=1, padx=5)

root.mainloop()
