# Gitpod Test

[![Open in KataPod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/HadesArchitect/GitpodTest/)

By default it always opens `intro.md` file.

## How to add "Next Step" link

```
[start scenario](command:katapod.loadPage?step2){.orange_bar}
```

Replace `step2` with the name of the step you need, matching the markdown file name. Omit the extension as we support only MD for now

## How to paste "Execute the code" code block 

Just like that:

    ```
    cqlsh
    ```
