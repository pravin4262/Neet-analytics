# NEET Analytics Platform

An analytics platform for NEET (National Eligibility cum Entrance Test) preparation, featuring performance analysis, rank prediction, and college admission predictions.

## Features

- **Quiz Performance Analytics**
  - Detailed analysis of quiz attempts and performance
  - Topic-wise performance breakdown
  - Accuracy and score tracking
  - Mistake correction rate analysis
  - Visual performance insights using matplotlib and seaborn

- **NEET Rank Prediction**
  - ML-based rank prediction using RandomForest
  - Confidence score calculation
  - Historical performance consideration
  - Topic-wise adjustment factors
  - Performance breakdown analysis

- **College Admission Predictor**
  - College-wise admission probability calculation
  - Category-based adjustments (General, OBC, SC, ST)
  - State quota consideration
  - Historical cutoff data analysis
  - Detailed recommendations

## Installation

```bash
pip install -r requirements.txt
```

Required packages:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- requests

## Usage

### Quiz Performance Analysis

```python
# Load and analyze quiz data
df = create_quiz_df(quiz_data)
analyze_performance(df)
plot_performance_metrics(df)

# Generate summary report
summary = generate_summary_report(df)
```

### NEET Rank Prediction

```python
predictor = NEETRankPredictor()
prediction = predictor.predict_rank(current_quiz, historical_quizzes)
print(f"Predicted NEET Rank Range: {prediction['predicted_rank']}")
print(f"Prediction Confidence: {prediction['confidence_score']}%")
```

### College Admission Prediction

```python
college_predictor = NEETCollegePredictor()
predictions = college_predictor.predict_colleges(
    neet_score=650,
    category='General',
    state='Home'
)
print(predictions)
```



## Features in Detail

### Performance Analytics
- Quiz attempt patterns
- Topic-wise performance analysis
- Mistake correction tracking
- Performance trend visualization
- Automated recommendations generation

### Rank Prediction
- Performance metric extraction
- Topic-based adjustments
- Historical performance consideration
- Confidence scoring
- Detailed performance breakdown

### College Predictions
- Multiple college comparison
- Category-wise analysis
- State quota considerations
- Admission probability calculation
- Customized recommendations


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.


