# Kursiv

The Pygments alternative. Based on Rust.

```python
from kursiv import highlight

h = highlight("print('hello, world!')")
print(h)
```

## API <kbd>dev</kbd>
API Documentation.

### <kbd>def</kbd> api.parse

```python
parse(code: str)
```

Parse the code with Rust-based AST.
