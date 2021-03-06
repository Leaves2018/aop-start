# aop-start
`aop-start` is a template repository for "assignment oriented programming". Its purpose is to provide a basic framework for each assignment. It is recommended that you use this as a reference to create your own assignment template repository, and use the `git clone` command to create a starting point each time you start a new assignment.

The software used in this example repository is LaTeX, Python and Jupyter Notebook, and you are encouraged to refer to [aop](https://github.com/Leaves2018/aop) to install the relevant software.

## code
Place the code files here. It is recommended to use the Jupyter Notebook form to complete the assignment. If `.py` format is required for submission, you can convert `.ipynb` to `.py` by using the following command.
```shell
jupyter nbconvert *.ipynb --to script
```

## data
Place the data files (like `.txt` and `.csv`) here.

## images
Place the image files (like `.png`, `.jpg`, `.tiff`) here.

As for the images generated by the code, it is recommended to create a separate folder under this directory to store them separately according to the question number.

For convenience, the path can be created automatically using most programming language. The following code uses Python to create the `./images/q1/` path.
```python
import os


output_path = os.path.join('...' , 'images', 'q1/')
os.makedirs(output_path, exist_ok=True)
```

## report
It is recommended to install `LaTeX` locally, like `MacTeX` for `macOS` or `Tex Live` for `Windows` and `Linux`. 
In this way, as long as the image file name remains the same, the document will be automatically recompiled to get a new PDF every time the image changes.

For longer text, it is recommended to split it into multiple `.tex` files (e.g. create a `.tex` file for each question) and then refer to it in the main `.tex` file using the `\input` command. For example,
```tex
\input{q1} % include ./q1.tex file
```

### Include code
To include code with the help of `minted` package, install `Pygments` at first:
```
pip install Pygments
```
and add the `-shell-escape` compilation parameter to `latexmk`:
```
echo "\$pdflatex='pdflatex -shell-escape';" > ~/.latexmkrc
```

## .gitignore
Use `.gitignore` to ignore unnecessary file commits to the git repository.