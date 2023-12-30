# Bindings.json

This is the file I'm most worried about communicating clearly

## Commands

This section of bindings.json does the following:

  - lists valid commands 
  - under each command, 
    - contains an ordered list of the arguments that feed that command
    - and a list of the acceptable values for that argument

## Bindings

This section of bindings.json is an example of a valid binding.

```
"bindings": [
        {
            "command": "button_action",
            "args": [
                0,
                "",
                0
            ]
        }
    ]
```

Cato should only get this section, and not the full specification of every possible valid command from the "commands" section of bindings.json

Note that bindings is an ordered list, and a real config will have as many bindings as recognized gestures, typically 8 or 3 depending on mode. 

Leave the number of bindings variable, and use the "commands" section to build a UI element that builds valid bindings as specified.

```
"bindings": [
        {
            "command": "button_action",
            "args": [
                0,
                "",
                0
            ]
        },
        {
            "command": "button_action",
            "args": [
                0,
                "",
                0
            ]
        },
        {
            "command": "quick_sleep",
            "args": []
        }
    ]
```


## General References / Notes
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

