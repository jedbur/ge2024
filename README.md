This is a collection of Jupyter notebooks for some amateur analysis of the Georgian 2024 Parliamentary elections. The data has been obtained from [this website](https://www.electoral.graphics/en-us/Elections-and-Datasets/Navigator-for-Elections/with-datasets/georgia-the-parliament-2024), and is directly provided by the Central Election Commission of Georgia. 

To run the notebooks, I recommend using a virtual environment, which you can install by opening a terminal in the root directory and running the following commands:

```sh 
python3 -m pip install --upgrade pip
python3 -m pip install uv
uv venv .venv -p 3.12
source .venv/bin/activate
uv pip install numpy scipy pandas matplotlib jupyter
```

The file `CEC_data.csv` containts the CEC electoral data, with some of the column names changed. The file `CEC_urban_data.csv` contains only the data for urban polling stations, that is stations with the District ID of 1-10 (Tbilisi), 20 (Rustavi), 59 (Kutaisi), 64, 67-70 (Poti), 79 (Batumi). The file `CEC_rural_data.csv`contains the CEC electoral data with urban polling stations removed. This is inspired by a [post by Roman Udot](https://x.com/romanik_/status/1850634766279962994) who recognised that the two subsets follow significantly different trends. 