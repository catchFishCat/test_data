# Test Data - BC Latency Analysis

This repository contains test data for Bus Controller (BC) latency analysis, comparing traditional and optimized implementations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Data Description

The dataset includes latency measurements for 8 test cases:

1. Legacy BC Time-to-Next Message
2. Legacy BC Frame Auto-Repeat
3. Legacy BC Frame Time Remaining
4. Legacy BC Response Timeout
5. Enhanced BC Time-to-Next Message
6. Enhanced BC DLY (Delay) Instruct
7. Enhanced BC Frame Timer
8. Enhanced BC Watchdog

## Files

- `statistics_traditional.csv` - Statistical summary (min, max, mean, median, std, range) for traditional implementation
- `statistics_optimized.csv` - Statistical summary for optimized implementation
- `raw_data_traditional.csv` - Raw latency measurements for traditional implementation
- `raw_data_optimized.csv` - Raw latency measurements for optimized implementation

## Data Format

### Statistics Files
Columns: `test_id`, `test_name`, `min`, `max`, `mean`, `median`, `std`, `range`

### Raw Data Files
Columns: `TestID`, `TestName`, `Loop`, `Late(ns)`

**Note:** All raw data files have been standardized to use consistent column naming. Only the latency measurement column (`Late(ns)`) is included.

## Usage Example

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load data
trad_stats = pd.read_csv('statistics_traditional.csv')
opt_stats = pd.read_csv('statistics_optimized.csv')

# Compare average latency
fig, ax = plt.subplots()
x = range(len(trad_stats))
ax.bar(x, trad_stats['mean'], width=0.4, label='Traditional', color='#e67e22', alpha=0.8)
ax.bar([i + 0.4 for i in x], opt_stats['mean'], width=0.4, label='Optimized', color='#3498db', alpha=0.8)
ax.set_xticks([i + 0.2 for i in x])
ax.set_xticklabels(trad_stats['test_name'], rotation=45, ha='right')
ax.legend()
plt.show()
```

## Citation

If you use this dataset in your research, please cite:

```
@dataset{bc_latency_test_data,
  author = {catchFishCat},
  title = {BC Latency Test Data},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/catchFishCat/test_data}
}
```

## Contact

catchFishCat - https://github.com/catchFishCat
