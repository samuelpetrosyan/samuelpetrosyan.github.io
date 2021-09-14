# Սամուել Պետրոսյան, ՔՀԾ-88

- [x] [Խնդիր 154](#խնդիր-154)
- [x] [Խնդիր 164](#խնդիր-164)
- [x] [Խնդիր 174](#խնդիր-174)
- [x] [Խնդիր 184](#խնդիր-184)
- [x] [Խնդիր 194](#խնդիր-194)
- [ ] [Խնդիր 204](#խնդիր-204)
- [ ] [Խնդիր 214](#խնդիր-214)
- [ ] [Խնդիր 224](#խնդիր-224)
- [ ] [Խնդիր 234](#խնդիր-234)
- [ ] [Խնդիր 244](#խնդիր-244)



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

![image](https://user-images.githubusercontent.com/62112092/133281944-20abf295-8ff9-4b1b-82d5-351c2fc3c56a.png)

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


### Խնդիր 184


![image](https://user-images.githubusercontent.com/62112092/133281849-eb976607-271f-4b65-91a3-ffcdf523d74a.png)

![image](https://user-images.githubusercontent.com/62112092/133281818-f16de7ef-68e5-46dc-becc-f25cd4f245c3.png)

Py3
```py
from tkinter import *

root = Tk()
root.title("Սամուել - Խնդիր 184")
root.resizable(False, False)
root.attributes("-toolwindow", 1)


def only_numbers(char):
    return char.isdigit()


def button_click():
    if e.get() != '':
        n = int(e.get())
        message = []
        for k in range(n, 0, -1):
            if 3 ** k < n:
                message.append(k)
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


### Խնդիր 194

![image](https://user-images.githubusercontent.com/62112092/133287328-4159d70d-72c0-452e-a30c-879352bca329.png)
![image](https://user-images.githubusercontent.com/62112092/133287358-81e5966e-8aa5-4069-ad02-5633687f28b4.png)

![image](https://user-images.githubusercontent.com/62112092/133287238-7fa849bc-3c67-4e17-a01f-9d596b0ddc9d.png)

Py3
```py
from tkinter import *
import math

root = Tk()
root.title("Սամուել - Խնդիր 194")
root.resizable(False, False)
root.attributes("-toolwindow", 1)


def only_numbers(char):
    return char.isdigit()


def button_click():
    if e.get() != '':
        n = int(e.get())
        x = 1
        for k in range(1, n+1, 1):
            x = x + 1/(math.factorial(k))

    else:
        return

    listbox = Listbox(root, relief=GROOVE, listvariable=StringVar(value=x))
    listbox.grid(row=1, column=0, columnspan=3, padx=10, pady=10)


validation = root.register(only_numbers)

e = Entry(root, relief=GROOVE, width=20, borderwidth=1, validate="key", validatecommand=(validation, '%S'))
e.grid(row=0, column=0, columnspan=3, padx=10, pady=10)

button_sum = Button(root, relief=RIDGE, borderwidth=1, text="Submit", padx=3, pady=0, fg='#fff', bg='#a74a6d', command=lambda: button_click())
button_sum.grid(row=0, column=4, padx=10, pady=10)

root.mainloop()
```
