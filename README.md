# Starbuck Analysis
   
## Exploring Starbucks Store Distribution Worldwide

This repository provides a comprehensive analysis of Starbucks store distributions across the globe. Utilizing a rich dataset of Starbucks locations, this project leverages Apache Spark for data processing within a Jupyter Notebook environment, stores the processed data in MongoDB, and visualizes insights through Metabase dashboards.

## Project Overview

The goal of this project is to explore the geographical distribution and characteristics of Starbucks stores worldwide, identifying patterns and insights that can inform business strategies and consumer behavior studies. By processing the data with Apache Spark, this project handles large volumes of data efficiently, enabling complex analytical tasks.
   
## Dataset

The dataset includes details about Starbucks stores in various countries, encompassing attributes such as location coordinates, store type, amenities provided, and opening dates. This comprehensive dataset is the foundation for our analysis and visualizations.

## Tools and Technologies

![image](https://github.com/rezkmike-study/starbuck-analysis/assets/156246227/9ee2d118-9ea2-40d9-b99b-f34900a3c4d1)

- **Apache Spark**: Used for its robust data processing capabilities, allowing for efficient handling of large datasets.
- **Jupyter Notebook**: Provides an interactive environment for data processing and analysis with Spark.
- **MongoDB**: Serves as the data storage solution, chosen for its scalability and flexibility with large datasets.
- **Metabase**: Utilized for its powerful and user-friendly dashboarding capabilities, enabling dynamic data visualization.

## Repository Structure

- `data/`: Contains the dataset files in CSV format.
- `notebooks/`: Includes the Jupyter Notebook that details the data processing steps with Spark.
- `dashboards/`: Contains the exported Metabase dashboard configurations.

## Getting Started

To get started with this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/starbucks-analysis.git
   ```
2. Navigate to the repository directory:
   ```bash
   cd starbucks-analysis
   ```
3. Start your Jupyter Notebook environment:
   ```bash
   jupyter notebook
   ```
4. Open the Spark processing notebook located in the `notebooks/` directory.
5. Ensure MongoDB is running on your system to store processed data.
6. Set up Metabase for visualization. Instructions for setting up Metabase are available in the `dashboards/` directory.

## Visualization with Metabase

After processing the data, you can explore various visualizations in Metabase. The dashboards provide insights into the density of stores by region, types of stores, and other interesting metrics. Visualizing this data helps in understanding the global spread and strategic placement of Starbucks stores.

## Contributing

Contributions to this project are welcome! Please refer to the CONTRIBUTING.md file for guidelines on how to make contributions.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
