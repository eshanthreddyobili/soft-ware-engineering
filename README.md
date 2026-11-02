
import tkinter as tk
from tkinter import messagebox

def login():
    user = username.get()
    pwd = password.get()
    if user == "admin" and pwd == "12345":
        messagebox.showinfo("Success", "Login Successful!")
    else:
        messagebox.showerror("Error", "Invalid Login Details")

root = tk.Tk()
root.title("Login Page")
root.geometry("300x250")

tk.Label(root, text="Welcome to Login").pack(pady=15)
tk.Label(root, text="Username").pack()
username = tk.Entry(root)
username.pack()
tk.Label(root, text="Password").pack()
password = tk.Entry(root, show="*")
password.pack()
tk.Button(root, text="Login", command=login).pack(pady=15)
root.mainloop()
