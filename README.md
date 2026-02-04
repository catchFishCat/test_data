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
