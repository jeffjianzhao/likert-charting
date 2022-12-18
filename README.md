# likert-charting

Likert scale questions are commonly used in human-computer interaction, user experience, and usability research. 
This repo provides some handy Python scripts for generating the following two common types of charts for Likert scale questionnaire results. 

The number of questions, the number of conditions (techniques), and the number of scale points (e.g., 5 or 7) can be configured as needed. So as the layout of individual sub-charts for the questions. The input is a 3-dimensional array of the questionnaire results: [techniques X questions X participants].

For example:

```python
questions = ['Q1', 'Q2', 'Q3', 'Q4', 'Q5', 'Q6']  # the text of questions
scale_num = 7  # 7-point Likert Scale
column_num = 3  # the number of columns for showing charts
colors = ['#7fc97f', '#beaed4', '#fdc086'] # recommend to use ColorBrewer

# test with random data (12 participants)
rating1 = np.random.randint(1, scale_num+1, (len(questions), 12))
rating2 = np.random.randint(1, scale_num+1, (len(questions), 12))

likertScaleChart('test2.pdf', questions, [rating1, rating2], scale_num, column_num, ['tech1', 'tech2'], colors[:2])
```

## Histograms Based

See `likert-hist-chart.py` or `likert-hist-chart.ipynb`.

![Histograms](../likert-charting/histograms.png)

## Stacked Bar Charts Based

See `likert-bar-chart.py` or `likert-bar-chart.ipynb`.

![Bars](../likert-charting/bars.png)

## Author
Jian Zhao ([www.jeffjianzhao.com](www.jeffjianzhao.com)).

## License

[MIT](https://opensource.org/licenses/MIT)