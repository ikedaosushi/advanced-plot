# advanced-plot
A practical wrapper library over matplotlib and seaborn

# Example data 

```python
import seaborn as sns
titanic = sns.load_dataset("titanic")
```

# Stack vertical bar

## data

```python
data = titanic['class'].value_counts().to_frame()
data
```

|  | class |
|:--|--:|
| Third | 491 |
| First | 216 |
| Second | 184 |

## Plot

```python
advanced_plot.stack_vertical_bar(data=data, label='index', value='class')
```

# Vertical bar

## data

```python
data = titanic['class'].value_counts().to_frame()
data
```

|  | class |
|:--|--:|
| Third | 491 |
| First | 216 |
| Second | 184 |

## Plot

```python
advanced_plot.vertical_bar(data=data, label="index", value="class")
```

# Histgram

## data

```python
titanic['age']
```

## Plot

```python
advanced_plot.hist(data = titanic['age'].dropna())
```