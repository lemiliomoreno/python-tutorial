# Python tutorial - First steps

Welcome to the first part of our Python tutorial.

## Install Python
First of all we need our Python command line, don't be affraid of using commands, this will be our favorite tool.

Go to [Python](https://www.python.org/downloads/) official website and download its latest version. It doesn't matter which operating system (OS) you are working on.

After it downloads, see how it executes in your OS.

### For Mac and Linux
Open a terminal:
* On Mac: `cmd + space` and search for terminal, hit return.
* On Linux: `cmd + alt + t`, depending on distribution.
```bash
$ python3
```

### For Windows
Open `Python 3.x (xx-bit)`.

## How Python is executed?
Python is an interpreted language, not compiled, it executes at runtime, this means, it'll execute the lines of code while it reads them.

Easy right? let's move on.

## Do something
Let's see how we print a simple word

```python
>>> print('Hello!')
# Hello!
```

Python includes multiple [built-in functions](https://docs.python.org/3/library/functions.html#built-in-functions), one of them is [`print()`](https://docs.python.org/3/library/functions.html#print). This one, will receive a `string`, in this case: `'Hello!'`, _note that is specified within single quotes_.

## Create a Python executable file

### For Mac and Linux
Create a file with your prefered text editor and name it as `my_first_python_executable.py`.

### For Windows
Open `IDLE (Pyhton 3.x.x)`, select `File -> New file` or `Ctrl + N` and save it as `my_first_python_executable.py`.

### Executing the file
We can see that the file extension is `.py`, meaning that is a Python executable.

Let's write some Python code:

[_Sample code_](src/my_first_python_executable.py)
```python
# my_first_python_executable.py
print('Hello world!')
print('I am a Python executable file!')
print('Bye...')
```
Save and execute it.

#### For Mac and Linux
```bash
$ python3 my_first_python_executable.py
# Hello world!
# I am a Python executable file!
# Bye...
```

#### For Windows
Select `Run -> Run module` or `F5`
```python
# Hello world!
# I am a Python executable file!
# Bye...
```

Now that you know how to open the command line and execute Python files, we should move on and start our real development. Continue to [Python tutorial - Data types](https://gitlab.com/pytorial/part-2-data-types).
