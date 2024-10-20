# Question

When changing any input on the page, the following chunk must be executed.

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
This can be confirmed by the fact that the part `"New default value : ", random_arg` does run and different output are printed.


I wonder will any of this widget will re-initialize their return value when rerun.

# Conclusion

The widget with a random default value will change its return value to a new "default value" every time the page rerun, and the value picked by users will be overwritten.

The widget with a constant default value, although executed again, will not change the value of return value being picked in the previous rerun.