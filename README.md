



## create a virtual environments 

```bash
python -m venv venv

``` 

## Activate a virual environment

```bash
source venv/bin/activate


``` 


```bash

pip install -e .


``` 

python -m src.data_ingestion

for checking tensorboard ui 

``` bash
tensorboard --logdir=tensorboard_logs/

```





# after completing training of model 

```bash 
dvc init --no-scm


```

after that create a dvc.yaml file 
then 
```bash 
dvc repro 

```



* dvc add artifacts/raw 
* dvc add artifacts/processed
* dvc add artifacts/model 
* dvc add artifacts/model_checkpoint 
* dvc add artifacts/weights

# you will get  

* model_checkpoint.dvc
* model.dvc
* processed.dvc 
* raw.dvc 
* weights.dvc

# to connect iam s3 bucket with local dev
dvc remote add -d myremote gs://my-dvc-bucket97/

* dvc status
* dvc push

* dvc pull
