# README for GumTree example

#### Web-based view:

1. Generate the web-based view:
    ``` bash
    gumtree-4.0.0-beta3/bin/gumtree webdiff Test.java revision/Test.java
    ```
2. Then visit http://127.0.0.1:4567/monaco-diff/0

#### AST mapping in pdf:

0. Install graphviz:
    Linux:
        ``` bash
        sudo apt install graphviz
        ```

    MacOS:
        ```bash
        brew install graphviz
        ```

1. Generate the dot file:
    ``` bash
    gumtree-4.0.0-beta3/bin/gumtree dotdiff Test.java revision/Test.java > tree.dot
    ```

2. Generate the pdf:
    ```bash
    dot -Tpdf tree.dot -o output.pdf
    ```


#### Raw Edit script:

```bash
gumtree-4.0.0-beta3/bin/gumtree textdiff Test.java revision/Test.java > diff.txt
```