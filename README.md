## Welcome to Samuel Petrosyan's Page

### Խնդիր 154

![image](https://user-images.githubusercontent.com/62112092/133244133-000429cf-a600-4934-97d9-b7d16dff05ab.png)

![image](https://user-images.githubusercontent.com/62112092/133244164-c1392a82-70cc-4ea6-83e7-c9402bc96739.png)

```import math
from tkinter import *

root = Tk()
root.title("Սամուել - Խնդիր 154")
root.resizable(False, False)
root.attributes("-toolwindow", 1)


def only_numbers(char):
    return char.isdigit()


def button_click():
    if e.get() != '':
        n = int(e.get())
        message = []
        for i in range(1, n):
            if math.remainder(n, i) == 3.0:
                message.append(i)
    else:
        return

    listbox = Listbox(root, relief=GROOVE, listvariable=StringVar(value=message))
    listbox.grid(row=1, column=0, columnspan=3, padx=10, pady=10)


validation = root.register(only_numbers)

e = Entry(root, relief=GROOVE, width=20, borderwidth=1, validate="key", validatecommand=(validation, '%S'))
e.grid(row=0, column=0, columnspan=3, padx=10, pady=10)

button_sum = Button(root, relief=RIDGE, borderwidth=1, text="Submit", padx=3, pady=0, fg='#fff', bg='#a74a6d', command=lambda: button_click())
button_sum.grid(row=0, column=4, padx=10, pady=10)

root.mainloop()```
