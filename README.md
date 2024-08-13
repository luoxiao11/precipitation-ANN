# Predicting Surface Precipitation Rates: Pixel-Based Neural Network

## Project Description

The **Tropical Cyclone Precipitation, Infrared, Microwave, and Environmental Dataset (TC PRIMED)** is centered around satellite passive microwave observations of tropical cyclones. It provides corrected brightness temperature data from consistent sources, which makes it suitable for machine learning applications. Specifically, the dataset contains passive microwave brightness temperature data that has been adjusted for instrument drift and bias, ensuring consistency throughout multiple years of satellite observations. This adjustment allows for a focus on differences in sensor characteristics rather than instrument errors.

When developing a machine learning model, datasets typically consist of input features and target labels. In the case of TC PRIMED, the dataset provides passive microwave brightness temperature data, which can be used as input features to predict storm-scale phenomena or pixel-based characteristics. In this project, we focus on a pixel-based approach to regression using a neural network model.

### Approach

1. **Data Preparation**:
   - **Input Features**: Passive microwave brightness temperature observations from the Global Precipitation Measurement (GPM) satellite's Microwave Imager (GMI) sensor, with frequencies ranging from 10.65 GHz to 89.0 GHz.
   - **Target Label**: Surface precipitation rate obtained from the NASA Goddard PROFiling algorithm (GPROF), provided in mm/hour.

2. **Model Setup**:
   - **Model Type**: Artificial Neural Network (ANN) for regression.
   - **Features**: The model utilizes brightness temperature observations to predict surface precipitation rates at each pixel.
   - **Training**: The neural network is trained on a subset of TC PRIMED data, specifically focusing on oceanic regions to avoid complexities associated with land surfaces.

3. **Product**:
   ![Precipitation Image](/img/precip.png)

4. **Evaluation**:
   - **Performance**: The model's predictions are compared against GPROF data, with an emphasis on understanding the discrepancies, especially at higher precipitation rates.
   - **Application**: The trained model can be applied to TC PRIMED overpass data to make pixel-based predictions of surface precipitation rates.

5. **Challenges and Considerations**:
   - **Data Limitations**: The sample size and choice of observation frequencies may impact the model's ability to generalize and capture high precipitation rates accurately.
   - **Model Hyperparameters**: Adjustments to the number of hidden layers, nodes, activation functions, and other parameters are essential for improving model performance.
   - **Normalization**: Normalizing input features to handle varying data scales and improve training stability.
