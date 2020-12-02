# Alphorder

Alphorder is a tool that allows you to put order in your folders with a simple line of code from the comandline or you can import it to your **Python proyect**

# Instalation

You can install alphorder whit **pip** running the following command

```
pip install alphorder
```

# Usage

There are two main ways you can use alphorder, from the comandline and importing it to your proyect.

## Proyect

You can import alphorder to your proyect with this line of code

```python
from alphorder import Alphorder
```
This way you have imported the class that contains the methods to order your folders

### Alphabetic order

You can put all the files and folders into the corresponding folder to his name, this mean that if there is a file called **Casa** will me moved to the folder **C**.

All of the numeric starting folders or files will be moved to a folder called **#**.

All of this will be achived bia the method `sort`

```python
Alphorder.sort("path/to/folder")
```

### Move to a specific folder
You can move all the content of a folder to another one with the method `moveToFolder`.

The method will receive two params, the first one will be the path of the folder, and the second one will be the folder to move.

> If the second param is not a valid path, then the program will create a folder with the second param as its name and move all the content to it.

```python
Alphorder.sort("/path/to/folder", "path/to/second/folder")
# or you can simply add a word or sentence
Alphorder.sort("/path/to/folder", "ordenado con alphorder")
```

### Move to a specific folder with params
You can perform the same that before but just for the content that matches a series one of the keywords that you specifie with the method `moveToFolderByKeywords`

This method will receive a param more that the previous one: an array of strings to match

> The target will be moved if any of the keywords is founded on its name

```python
Alphorder.sort("/path/to/folder", "second path", ["sort", "alph"])
```

## Commandline

You can use the same methods that on the proyect directly from the commandline with the `alphorder` keyword.

### Alphabetic order

```bash
alphorder "/path/to/folder"
```

As you can see is allmost the same as before.

### Move to a specific folder

As in a proyect you need to specify two params: the main path and the target path.

```bash
alphorder "/path/to/folder" "/target/path"
```

> If the second param is not an existing folder then a folder with the same name will be created on the main folder

### Move to a specific folder with params

If you add more params after the two path this ones will be taked as **keywords**, and then just will be moved the files or the folders that **contains** any of the **keywords** in its name

```bash
alphorder "/path/to/folder" "/target/path" word1 word2 "sample of a sentence"
```