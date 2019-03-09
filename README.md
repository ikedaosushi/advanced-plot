# advanced-plot
A practical wrapper library over matplotlib and seaborn

# Install

```
pip install advanced-plot
```

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

![Stack vertical bar](https://github.com/ikedaosushi/advanced-plot/blob/master/assets/stack_vertical_bar.png)

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

![Vertical bar](https://github.com/ikedaosushi/advanced-plot/blob/master/assets/vertical_bar.png?raw=true)

# Histgram

## data

```python
titanic['age']
```

## Plot

```python
advanced_plot.hist(data = titanic['age'].dropna())
```

![Histgram](https://github.com/ikedaosushi/advanced-plot/blob/master/assets/advanced_hist.png)