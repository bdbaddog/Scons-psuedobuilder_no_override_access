Sample code to demonstrate issue where PsuedoBuilder doesn't get access to values set in OverrideEnvironment created when a builder is called with variables set


```
x=env.Program('target','source',MY_SPECIAL_VAR_FOR_PSEUDO='Yes')
```

