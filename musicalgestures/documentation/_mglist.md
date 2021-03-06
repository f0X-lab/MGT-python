# MgList

> Auto-generated documentation for [\_mglist](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py) module.

- [Musicalgestures](README.md#musicalgestures-index) / [Modules](MODULES.md#musicalgestures-modules) / MgList
  - [MgList](#mglist)
    - [MgList().\_\_add\_\_](#mglist__add__)
    - [MgList().\_\_delitem\_\_](#mglist__delitem__)
    - [MgList().\_\_getitem\_\_](#mglist__getitem__)
    - [MgList().\_\_iadd\_\_](#mglist__iadd__)
    - [MgList().\_\_iter\_\_](#mglist__iter__)
    - [MgList().\_\_len\_\_](#mglist__len__)
    - [MgList().\_\_setitem\_\_](#mglist__setitem__)
    - [MgList().as_figure](#mglistas_figure)
    - [MgList().show](#mglistshow)

## MgList

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L5)

```python
class MgList():
    def __init__(*objectlist):
```

Class for handling lists of MgImage, MgFigure and MgList objects in the Musical Gestures Toolbox.

## Attributes

- `*objectlist` - objects and/or list(s) of objects

MgObjects and/or MgImages to include in the list.

### MgList().\_\_add\_\_

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L128)

```python
def __add__(other):
```

Implements `+`.

#### Arguments

- `other` _MgImage, MgFigure, or MgList_ - The object(s) to add to the MgList.

#### Returns

- `MgList` - The incremented MgList.

### MgList().\_\_delitem\_\_

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L85)

```python
def __delitem__(key):
```

Implements deleting elements given an index from the MgList.

#### Arguments

- `key` _int_ - The index of the element to delete.

### MgList().\_\_getitem\_\_

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L63)

```python
def __getitem__(key):
```

Implements getting elements given an index from the MgList.

#### Arguments

- `key` _int_ - The index of the element to retrieve.

#### Returns

- `MgImage`, `MgFigure`, or `MgList` - The element at `key`.

### MgList().\_\_iadd\_\_

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L103)

```python
def __iadd__(other):
```

Implements `+=`.

#### Arguments

- `other` _MgImage, MgFigure, or MgList_ - The object(s) to add to the MgList.

#### Returns

- `MgList` - The incremented MgList.

### MgList().\_\_iter\_\_

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L94)

```python
def __iter__():
```

Implements `iter()`.

#### Returns

- `iterator` - The iterator of `self.objectlist`.

### MgList().\_\_len\_\_

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L54)

```python
def __len__():
```

Implements `len()`.

#### Returns

- `int` - The length of the MgList.

### MgList().\_\_setitem\_\_

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L75)

```python
def __setitem__(key, value):
```

Implements setting elements given an index from the MgList.

#### Arguments

- `key` _int_ - The index of the element to change.
  value (MgImage, MgFigure, or MgList): The element to place at `key`.

### MgList().as_figure

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L159)

```python
def as_figure(dpi=300, autoshow=True, title=None, export_png=True):
```

Creates a time-aligned figure from all the elements in the MgList.

#### Arguments

- `dpi` _int, optional_ - Image quality of the rendered figure in DPI. Defaults to 300.
- `autoshow` _bool, optional_ - Whether to show the resulting figure automatically. Defaults to True.
- `title` _str, optional_ - Optionally add title to the figure. Defaults to None, which uses the file name as a title.
- `export_png` _bool, optional_ - Whether to export a png image of the resulting figure automatically. Defaults to True.

#### Returns

- `MgFigure` - The MgFigure with all the elements from the MgList as layers.

### MgList().show

[[find in source code]](https://github.com/fourMs/MGT-python/blob/master/musicalgestures/_mglist.py#L47)

```python
def show():
```

Iterates all objects in the MgList and calls `mg_show()` on them.
