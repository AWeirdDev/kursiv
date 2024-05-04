# ***Kursiv***

Python for the component era.

> Coming Soon. The AST parser is halfway there!

<br />

<table>
  <thead>
    <tr>
      <th>
        Original
      </th>
      <th>
        Transformed (Edge 🏔️)
      </th>
      <th>
        Transformed (AST)
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
<td>

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

</td>
<td>

`transformed_edge.py`
```python
# ;__k94hpi=FRAGMENT,__1c2fgp=HTML,NOIMPORT
hello = "world"
def App():
  return (
    __k94hpi(
      __1c2fgp("p")("Check out this dataframe and array."),
      __1c2fgp("code")(df.head()),
      __1c2fgp("code")(numpy.array([1.0, 2.0, 3.0]))
    )
  )
```

</td>
<td>

`transformed_ast.rs`
```rs
[
  …,
  Function {
    id: "App",
    block: Block {
      tokens: [
        Return {
          tokens: [
            Kursiv { .. },
          ],
        },
      ],
    },
  },
]
```

</td>
    </tr>
  </tbody>
</table>


## Use the AST

```python
>>> import kursiv
>>> kursiv.parse("100, my_var")
[Token::Int { value: 100 }, Token::Identifier { id: "my_var" }]
```
