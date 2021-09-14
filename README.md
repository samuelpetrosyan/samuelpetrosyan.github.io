# Սամուել Պետրոսյան, ՔՀԾ-88

- [Խնդիր 154](https://github.com/samuelpetrosyan/samuelpetrosyan.github.io#խնդիր-154)
- [Խնդիր 164](https://github.com/samuelpetrosyan/samuelpetrosyan.github.io#խնդիր-164)
- [Խնդիր 174](https://github.com/samuelpetrosyan/samuelpetrosyan.github.io#խնդիր-174)



### Խնդիր 154

![image](https://user-images.githubusercontent.com/62112092/133244133-000429cf-a600-4934-97d9-b7d16dff05ab.png)

![image](https://user-images.githubusercontent.com/62112092/133244164-c1392a82-70cc-4ea6-83e7-c9402bc96739.png)

Py3
```py
import math
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

root.mainloop()
```

### Խնդիր 164

![image](https://user-images.githubusercontent.com/62112092/133275773-f2f046c1-78f0-47c5-ab6e-72a7aae43f99.png)

![image](https://user-images.githubusercontent.com/62112092/133275724-cc25439c-882c-4bd1-902a-aaecec3eede0.png)

Py3
```py
import math
from tkinter import *

root = Tk()
root.title("Սամուել - Խնդիր 164")
root.resizable(False, False)
root.attributes("-toolwindow", 1)


def only_numbers(char):
    return char.isdigit()


def button_click():
    if e.get() != '':
        n = int(e.get())
        message = []
        for i in range(100, 999):
            if math.sqrt(i) > n and math.modf(math.sqrt(i))[0] == 0.0:
                message.append(i)
                break
    else:
        return

    listbox = Listbox(root, relief=GROOVE, listvariable=StringVar(value=message))
    listbox.grid(row=1, column=0, columnspan=3, padx=10, pady=10)


validation = root.register(only_numbers)

e = Entry(root, relief=GROOVE, width=20, borderwidth=1, validate="key", validatecommand=(validation, '%S'))
e.grid(row=0, column=0, columnspan=3, padx=10, pady=10)

button_sum = Button(root, relief=RIDGE, borderwidth=1, text="Submit", padx=3, pady=0, fg='#fff', bg='#a74a6d', command=lambda: button_click())
button_sum.grid(row=0, column=4, padx=10, pady=10)

root.mainloop()
```


### Խնդիր 174

![image](https://user-images.githubusercontent.com/62112092/133278494-d20b417d-06d8-473c-a06c-5d795feaa079.png)
*174
![image](https://user-images.githubusercontent.com/62112092/133278534-3c109c09-ffd1-4c45-b182-fbfdbd1dadfa.png)

Py3
```py
from tkinter import *

root = Tk()
root.title("Սամուել - Խնդիր 174")
root.resizable(False, False)
root.attributes("-toolwindow", 1)


def only_numbers(char):
    return char.isdigit()


def button_click():
    if e.get() != '':
        n = int(e.get())
        x = [1]
        for k in range(1, n):
            x_tmp = (2 + 1 / x[k - 1])
            x.append(x_tmp)

    else:
        return

    listbox = Listbox(root, relief=GROOVE, listvariable=StringVar(value=x))
    listbox.grid(row=1, column=0, columnspan=3, padx=10, pady=10)


validation = root.register(only_numbers)

e = Entry(root, relief=GROOVE, width=20, borderwidth=1, validate="key", validatecommand=(validation, '%S'))
e.grid(row=0, column=0, columnspan=3, padx=10, pady=10)

button_sum = Button(root, relief=RIDGE, borderwidth=1, text="Submit", padx=3, pady=0, fg='#fff', bg='#a74a6d',
                    command=lambda: button_click())
button_sum.grid(row=0, column=4, padx=10, pady=10)

root.mainloop()
```
