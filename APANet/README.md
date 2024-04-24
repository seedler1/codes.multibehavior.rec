# APANet
## Code
This is the source code for paper: Multi-behavior Recommendation with Action Pattern-aware Networks

## Requirements
* Python3 with library Torch with Cuda
* laptop with an NVIDIA GPU

## Usage
First, run the file `datasets/preprocess.py` to preprocess the data.

- The original code (which is for the already provided sample dataset)
```
cd APANet
cd datasets
python preprocess.py --dataset sample  
```

- The modified code (which uses the publically available Retailrocket dataset)
-- https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset?resource=download&select=events.csv
- only use Retailrocket or other datasets if you have an experimental machine, as for me trying to run the first epoch led to 1+hr of fruitless labor
```
cd APANet
cd datasets
python preprocess.py --dataset Rrocket 
```

Then, train and evaluate the APANet model.

If using sample data
```
python main.py --dataset sample
```

If using Rrocket data

- make sure to modify main.py code to have dataset Rrocket if wanting to run this part later

- parser.add_argument('--dataset', default='sample', help='dataset name: Rrocket/Kkbox/yoochoose/sample')
```
python main.py --dataset Rrocket
```

## Citation