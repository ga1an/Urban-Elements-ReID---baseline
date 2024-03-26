# Urban-Elements-ReID---baseline

## Download code and set up enviroment
To download the main code and set up the enviroment please follow the instructions in [Part Aware Transformer](https://github.com/liyuke65535/Part-Aware-Transformer)

## Modified codes
In order to use PAT for the [Urban Elements ReID](https://www.kaggle.com/competitions/urbam-reid-challenge/overview) competition follow the next steps:

### 1) Download the dataset
Download the UrbanElements dataset from the section [Data](https://www.kaggle.com/competitions/urbam-reid-challenge/data) in the Kaggle competition page.

### 2) Add the corresponding dataloaders
Add to the folder `data/datasets/` the dataloaders and initialization files `UrbanElementsReID.py`, `UrbanElementsReID_test.py` and `__init__.py`.

### 3) Configuration files
Add to `config/` folder and set up the correspondig paths and configuration of `UrbanElementsReID_test.yml` and `UrbanElementsReID_train.yml` files.

### 4) Train the model
In order to train the model first make sure that all the condifuration settings and paths are correct. Then run the following line:

```bash
python update.py --config_file "config/UrbanElementsReID_test.yml" --track "path to store the track.txt and track_submission.csv"
```

### 5) Evaluation
To evaluate the results of the models use the script update.py to create the track_submission.csv and add the submission to Kaggle in order to obtain the obtained score. 

```bash
python update.py --config_file "config/UrbanElementsReID_test.yml" --track "path to store the track.txt and track_submission.csv"
```

### Acknowledgment 
Special thanks to liyuke65535 for the creation and publication of [Part Aware Transformer](https://github.com/liyuke65535/Part-Aware-Transformer) repo. and congratulations for the excelent work.
