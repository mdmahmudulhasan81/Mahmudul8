#Python code about CV (GUI Application) 


import tkinter as tk
from tkinter import messagebox


def display_cv():
    cv_text = (
        f"Name: {entry_name.get()}\n"
        f"Email: {entry_email.get()}\n"
        f"Phone: {entry_phone.get()}\n\n"
        f"Education:\n {entry_education.get('1.0', tk.END)}\n"
        f"Experience:\n {entry_experience.get('1.0', tk.END)}\n"
        f"Skills:\n {entry_skills.get('1.0', tk.END)}"
    )
    
    messagebox.showinfo("Your CV Information", cv_text)


root = tk.Tk()
root.title("CV Builder")
root.geometry("500x600")


header = tk.Label(root, text="CV Builder", font=("Arial", 16))
header.pack(pady=10)


label_name = tk.Label(root, text="Name:")
label_name.pack(anchor="w", padx=10)
entry_name = tk.Entry(root, width=50)
entry_name.pack(pady=5, padx=10)


label_email = tk.Label(root, text="Email:")
label_email.pack(anchor="w", padx=10)
entry_email = tk.Entry(root, width=50)
entry_email.pack(pady=5, padx=10)


label_phone = tk.Label(root, text="Phone:")
label_phone.pack(anchor="w", padx=10)
entry_phone = tk.Entry(root, width=50)
entry_phone.pack(pady=5, padx=10)


label_education = tk.Label(root, text="Education:")
label_education.pack(anchor="w", padx=10)
entry_education = tk.Text(root, height=5, width=50)
entry_education.pack(pady=5, padx=10)


label_experience = tk.Label(root, text="Experience:")
label_experience.pack(anchor="w", padx=10)
entry_experience = tk.Text(root, height=5, width=50)
entry_experience.pack(pady=5, padx=10)


label_skills = tk.Label(root, text="Skills:")
label_skills.pack(anchor="w", padx=10)
entry_skills = tk.Text(root, height=5, width=50)
entry_skills.pack(pady=5, padx=10)


submit_button = tk.Button(root, text="Submit", command=display_cv)
submit_button.pack(pady=20)


root.mainloop()
