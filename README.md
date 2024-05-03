# Kursiv

Python for the component era.

> Coming Soon. The AST parser is halfway there!

<br />

`main.ksv`
```jsx
hello = "world"

def App():
  return (
    <>
      <p>Check out this dataframe and array.</p>
      <code>{df.head()}</code>
      <code>{numpy.array([1., 2,, 3.])}</code>
    </>
  )
```

## Use the AST

```python
>>> import kursiv
>>> kursiv.parse("100, my_var")
[Token::Int { value: 100 }, Token::Identifier { id: "my_var" }]
```
