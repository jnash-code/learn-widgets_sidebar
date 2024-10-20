When chainging any input on the page.

The following chunk must be executed.

```
v = st.slider(
    'With default value 25',
    0.0, 10.0, 4.0
)
"v is : ", v

random_arg = np.random.randn(1,1)[0,0]

w = st.slider(
    'With default value 25',
    0.0, 10.0, random_arg
)
"w is : ", w
```
I can tell because the part `"New default value : ", random_arg` does run.