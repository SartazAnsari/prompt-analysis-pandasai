# Mobile Games Rating Analysis with PandasAI and LLM

## Overview

This project demonstrates the usage of [PandasAI](https://docs.pandas-ai.com/) with [BambooLLM](https://www.pandabi.ai/) to analyze a dataset of mobile game ratings. The analysis includes verifying outputs generated by PandasAI with manually generated results. The dataset used can be found [here](https://www.kaggle.com/datasets/dem0nking/mobile-games-android-and-ios-rating-dataset) and it consists mobile game ratings and related information.

## Prerequisites
1. **Python 3.x**: Download and install from [python.org](https://www.python.org/). 

## Setup
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/SartazAnsari/prompt-analysis-pandasai.git
   cd prompt-analysis-pandasai
   ```

2. **[ CHOOSE ANYONE ] Environment setup**
    * Using **Python**
        1. Create virtual environment: 
            ```bash
            python -m prompt-analysis-pandasai-env
            ```
        2. Activate the environment:
            * Windows: 
                ```bash
                prompt-analysis-pandasai-env\Scripts\activate
                ```
            * Unix or MacOS:
                ```bash
                source prompt-analysis-pandasai-env/bin/activate

                ```
        3. Install the required packages:
            ```bash
            pip install notebook
            pip install ipykernel
            pip install kaggle
            pip install pandas matplotlib
            pip install pandasai
            ```
        4.  if you get error as Microsoft Visual C++ 14.0 or greater is required while installing `pandasai` then install **MSVC v143 - VS 2022 C++ x64/x86 Build Tools** and **Windows 11 SDK** or **Windows 10 SDK** from [Build tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/). 
        5. If you get error as No module named 'yaml' then install `pip install pyyaml`.   
    * Using **Conda**
        1. Install **Miniconda/Anaconda**: Download and install from [conda.io](https://conda.io).
        2. Create a new environment:
            ```bash
            conda create --name prompt-analysis-pandasai-env python=3.12
            ```
        3. Activate the environment:
            ```bash
            conda activate prompt-analysis-pandasai-env
            ```
        4. Install the required packages:
            ```bash
            conda install -c conda-forge notebook
            conda install -c conda-forge ipykernel
            conda install -c conda-forge kaggle
            conda install pandas matplotlib
            pip install pandasai
            ```
        5.  if you get error as Microsoft Visual C++ 14.0 or greater is required while installing `pandasai` then install **MSVC v143 - VS 2022 C++ x64/x86 Build Tools** and **Windows 11 SDK** or **Windows 10 SDK** from [Build tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/). 
        6. If you get error as No module named 'yaml' then install `conda install pyyaml`.

3. **[ IF NOT SET BEFORE ] Setting up the Kaggle API**
    * Sign in to **Kaggle** and navigate to the **Account** tab of your user profile.
    * Scroll down to the **API** section and click on **Create New API Token**. 
    * This will download a file named `kaggle.json` containing your API credentials.
    * Place the `kaggle.json` file in the `~/.kaggle/` directory. If the directory does not exist, create it.
    * You're all set up! You can now use the Kaggle API to download datasets directly to your project.

4. **Setting up LLM and Agent**
    * By default, PandasAI uses BambooLLM if no other LLM is specified. You can skip setting up LLM and directly pass the DataFrame to Agent as follows:
    ```bash
    agent = Agent(dfs=df)
    ``` 
    * To use BambooLLM, create an account on [PandaBI](https://www.pandabi.ai/).
    * Go to `API Keys` > `Add API Key` and copy the API Key.
    * Create a `.env` file and set the key as follow:
    ```bash
    PANDASAI_API_KEY = 'YOUR_API_KEY_GOES_HERE'
    ```
    * For more detailed information, you can refer to the [PandasAI documentation](https://docs.pandas-ai.com/en/latest) and the [PandasAI GitHub repository](https://github.com/pandasai/pandasai).

## Analysis
* Insights into the number of unique games, developers, and genres.
* Top games and developers were identified based on ratings and count of games developed.
* Various visualizations such as pie charts, bar charts, and line charts were generated to present the data effectively.
* Outputs generated by PandasAI were verified against manually generated results, demonstrating the accuracy and utility of the tool.

## Usage
1. Ensure the dataset is available in the project directory.
2. Import the necessary libraries and functions.
3. Run the provided Python script to perform the analysis and generate visualizations.