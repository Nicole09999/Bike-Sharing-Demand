# bike_rentals_prediction
# Bike Sharing Demand Prediction with AutoGluon

This project predicts bike sharing demand using AutoGluon, an automated machine learning library. AutoGluon simplifies model training by automating feature engineering, model selection, and hyperparameter tuning.

## Usage

1. **Installation**: Install AutoGluon and other dependencies:
    ```bash
    pip install autogluon
    ```

2. **Dataset**: Download the dataset from the Kaggle competition:
    ```bash
    kaggle competitions download -c bike-sharing-demand
    unzip -o bike-sharing-demand.zip
    ```

3. **Usage**: Load the dataset, preprocess it, and train a predictor using AutoGluon:
    ```python
    import pandas as pd
    from autogluon.tabular import TabularPredictor

    # Load data, preprocess as needed

    # Specify label column and problem type
    label = 'count'
    problem_type = 'regression'

    # Initialize AutoGluon predictor
    predictor = TabularPredictor(label=label, problem_type=problem_type)

    # Fit predictor to training data
    predictor.fit(train_data)
    ```

4. **Evaluation**: Evaluate the predictor and make predictions:
    ```python

    # Make predictions
    predictions = predictor.predict(test_data)
    ```

5. **Further Customization**: Explore additional features and hyperparameters to improve model performance.

## Author
Nicole Dcosta

## License
This project is licensed under the [MIT License](LICENSE).
