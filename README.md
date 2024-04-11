# Kursiv

Python in your control.

<br />

`main.py`

```python
import kursiv

# Create a box
box = kursiv.Box(
  allow_imports=[],  # Allow NO packages/modules
  disallow_nodes=["def"]  # Allow NO functions
)

# (1) Run the box from a script file
box.run("script.py")

# (2) ...or from a code string
box.run("""foo()""")
```

<br />

`script.py`

```python
print("Hello, World!")

# Uncomment and see error
# def hello():
#   print("panik!")
```

