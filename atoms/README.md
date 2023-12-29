# Bindings

Note - wiki for bindings reflects an older format for command entry.

Please use specified "command / args" from bindings.json

e.g.

Old format: 
```
["button_action",0,"double_tap",1]
```
New format: 
```
{
    "bindings" : [
        {
            "command" : "button_action",
            "args" : [0, "double_tap", 1]
        },
        {
            "command" : "button_action",
            "args" : [0, "double_tap", 2]
        }
    ]   
}
```
For list of valid commands and associated args, please refer to: https://github.com/aulitech/Cato/wiki/BindingList

