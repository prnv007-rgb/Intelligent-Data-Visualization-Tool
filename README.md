# Intelligent Data Visualization Tool

An end-to-end solution that leverages machine learning and natural language processing to automate data visualization. Simply upload your CSV file, describe what you want to explore, and let the tool select the optimal axes and chart type for you.

---

##  Features

* **CSV Upload**: Easily load any tabular data in CSV format.
* **Natural Language Queries**: Ask questions like "Show me sales over time" or "Compare revenue vs. marketing spend."
* **Axis Selection via Llama**: Uses a LLaMA-based language model to determine the best `x` and `y` columns from your data.
* **Chart-Type Prediction**: A custom-trained machine learning model predicts the most suitable visualization (bar, line, scatter, etc.).
* **Grammar & Spelling Correction**: Refines model-generated sentences via LLaMA to ensure clear, polished chart descriptions.
* **One-Click Plotting**: Generates Matplotlib/Plotly charts automatically—no manual coding required.

---

## 🎯 Getting Started

### Prerequisites

* Python 3.8 or higher
* `pip` package manager
* Optional (for model performance): GPU with CUDA support



## Usage

1. **Launch the Application**

2. **Upload your CSV**: Select the file via the provided prompt or web interface.
3. **Enter your Query**: For example, "Plot monthly user sign-ups against marketing spend."
4. **View Your Chart**: The tool will display the visualization in a new window or embed it in the notebook.

### Example
on run_viz_tool.py --file data/sales.csv "Show quarterly revenue trends"
```

*Automatically generates a line chart of `Quarter` vs. `Revenue`.*

---

## ⚙️ How It Works

1. **Data Ingestion**: Reads the CSV into a Pandas DataFrame.
2. **Axis Prediction**: Sends your query and DataFrame column list to a LLaMA-based model, which returns the best-fit `x` and `y` columns.
3. **Chart-Type Classification**: Feeds the DataFrame slice and the corrected sentence to a custom ML classifier to predict chart type.
4. **Grammar Correction**: Submits the raw description to LLaMA for polishing.
5. **Visualization**: Renders the final chart using Matplotlib or Plotly.


*Happy visualizing!*
