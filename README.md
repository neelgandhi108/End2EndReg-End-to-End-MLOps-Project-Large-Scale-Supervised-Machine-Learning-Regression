# End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression

# Emelop's Maturity Model

At Level 0, there is no automation, and machine learning is conducted through Jupyter notebooks without proper pipelining or automation. Level 1 introduces DevOps practices, including automated releases and basic testing, but lacks machine learning-specific automation.

Level 2 is automated training, where machine learning training pipelines are established, and experiment tracking is introduced. Deployment is not yet automated, but it's relatively simple.

Level 3 focuses on automated deployment, allowing models to be easily deployed with minimal human intervention. It also introduces A/B testing capabilities for comparing model versions.

The choice of which level to target depends on project requirements and maturity, with Level 0 being suitable for proof of concept, Level 2 for early production, and Level 3 or 4 for more mature and complex use cases. In this context, the project is operating at **Level 3**.

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/MLModel%20(1).png" alt="MLModel(1)"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/MLModel%20(2).png" alt="MLModel(2)"></td>
  </tr>
</table>

## Exploratory data analysis (EDA) and Machine learning

We delve into exploratory data analysis (EDA) and machine learning to predict trip durations based on pickup and drop-off latitude and longitude. The project's primary focus is on visualizing and understanding the dataset through a variety of plots and packages:

1.  **Matplotlib:** Utilized for vendor_id and store_fwd flag histograms, providing a foundational visualization framework.
    
2.  **Seaborn:** Used for creating visually appealing plots, such as violin plots and boxplots, and leverages Matplotlib's functionality for enhanced aesthetics.
    
3.  **Pandas:** Employed for parallel coordinates, showcasing cluster characteristics within the dataset.
    
4.  **Bokeh:** Offers interactive time series plots, allowing for zooming, axis manipulation, and interactive legends.
    
5.  **Folium:** Enables geographic visualizations with interactivity, displaying pickup locations, cluster locations, and additional terrain options.
    
6.  **Pygmaps:** An archive package, utilized for location and cluster visualizations with unique interactive features.
    
7.  **Plotly:** Provides colorful visualizations, including bubble plots, with some requiring interaction with Plotly servers.
    
8.  **Gmaps:** Known for its familiarity and user-friendly features, offers route-related functionalities.
    
9.  **Ggplot2:** Although in a developing state in Python, it produces beautiful plots for weather data of NYC, with a slight learning curve.
    
10.  **Basemaps:** Excluded due to complexity, numerous arguments, different styles, and limited documentation.
    
11.  **No package:** A heatmap of NYC taxi traffic is created through image processing, offering insights into basic image manipulation.
    
12.  **Datashader:** Ideal for handling large datasets for location heatmaps, though image processing is faster for specific use cases.
    
13.  **Holoviews:** Offers interactive and artistic visualizations, demanding substantial system resources for optimal performance.
    

Additionally, an animation is included to illustrate the pickup-drop heatmap's evolution throughout the day using Matplotlib's animation capabilities.

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/EDA%20(1).png" alt="EDA"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/EDA%20(2).png" alt="EDA(1)"></td>
  </tr>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/EDA%20(3).png" alt="EDA(2)"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/EDA%20(4).png" alt="EDA(3)"></td>
  </tr>
</table>

Experiment tracking, using tools like MLflow, is crucial for reproducibility, organization, and model optimization in machine learning. MLflow helps organize experiments into runs, allowing you to track parameters, metrics, metadata, artifacts, and even models. The MLflow UI provides an intuitive interface to manage and analyze your experiments and runs.

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (3).png"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (4).png"></td>
  </tr>
</table>

In the project, I installed MLflow, configured a backend for the MLflow model registry, added tracking to a Jupyter Notebook, and visualized the logged information in the MLflow UI. Additionally, I logged parameters, metrics, and tags for each experiment run in MLflow.

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (5).png"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (9).png"></td>
  </tr>
</table>

AWS Setup

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (11).png"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (12).png"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (13).png"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (14).png"></td>
  </tr>
</table>

In the project, I demonstrated how to perform hyperparameter tuning for an XGBoost model using Hyperopt, logged the results into MLflow, and explored the optimization results in the MLflow UI. Additionally, I discussed model selection criteria and introduced the "auto log" functionality in MLflow to easily log training runs with minimal code.

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (10).png"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (1).png"></td>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (2).png"></td>
  </tr>
</table>

In the project, I demonstrated model management using MLflow. I showed how to save machine learning models as artifacts, log preprocessing steps, and provided code examples on how to load and make predictions with the saved models. Additionally, I discussed the benefits of organizing models in the MLflow Model Registry for better model versioning and management.

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (6).png"></td>
  </tr>
</table>

In the project related to model management, I implemented a Model Registry using MLflow. This registry helps streamline the process of managing machine learning models, including registering models, transitioning them between different stages (e.g., staging, production), annotating models, and version control. Use the MLflow client class to interact with the Model Registry and make informed decisions about promoting models to production based on their performance on test data.

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (7).png"></td>
  </tr>
</table>


Running MLflow with multiple data scientists working on various ML models and utilizing the Model Registry.
Showcased the setup of a remote tracking server on AWS EC2, configuring AWS credentials, and connecting to the server.
Trained a machine learning model, logged metrics, and artifacts, and registered models using MLflow.
Demonstrated how to access and use the MLflow UI to visualize experiments, models, and metrics.

<table>
  <tr>
    <td align="center"><img src="https://github.com/neelgandhi108/End2EndReg-End-to-End-MLOps-Project-Large-Scale-Supervised-Machine-Learning-Regression/blob/main/Assets/ExperimentTrackingandManagement (8).png"></td>
  </tr>
</table>



