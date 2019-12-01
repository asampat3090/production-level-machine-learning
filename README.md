# Tools for Production Level Machine Learning

[NOTE: This repo is an constant work in progress. Any feedback is greatly appreciated :smile:]

A curated list of useful tools and references for production level machine learning, both open source, and propreitary. Also included are some pointers for tradeoffs of choosing 

## Data
Data handing is a broad topic that requires a number of tools for processing, storage, privacy, pipelines, and many others.

### Storage
Open Source &  SaaS Services
* **Object store**: Store binary data (images, sound files, compressed texts) 
  * [Amazon S3](https://aws.amazon.com/s3/) 
  * [Ceph](https://ceph.io/) 
* **Database**: Store metadata (file paths, labels, user activity, etc). 
  * [Postgres](https://www.postgresql.org/) is the right choice for most of applications, with the best-in-class SQL and great support for unstructured JSON. 
* **Data Lake**: to aggregate features which are not obtainable from database (e.g. logs)
  * [Amazon Redshift](https://aws.amazon.com/redshift/)
* **Feature Store**: store, access, and share machine learning features. Feature extraction can be computationally expensive and nearly impossible to scale, hence re-using features by different models and teams is a key to high performance ML teams. 
  * [FEAST](https://github.com/gojek/feast): Only for Google Cloud 
  * [Michelangelo Palette](https://eng.uber.com/michelangelo/): Specific part of a proprietary project within Uber

### Pipelines 
Open Source 
* [Lore](https://github.com/instacart/lore)
* [Airflow](https://airflow.apache.org/) 
* [Luigi](https://github.com/spotify/luigi)

## Machine Learning Development Frameworks 
There are number of development frameworks out there. There are fundamental libraries as well as derivative APIs (e.g. Keras) which simplifies the interface. 

Open Source
* [Tensorflow](https://www.tensorflow.org/): Fundamental tool for deep learning and well supported by Google & community
* [PyTorch](https://pytorch.org/): Fundamental tool based upon Torch developed and well supported by Facebook & community
* [Keras](https://keras.io/): Simplified API for easier development 
* [Scikit Learn](https://scikit-learn.org/stable/)
* [DeepDetect](https://github.com/beniz/deepdetect)

## Model / Experiment Management
Open Source
* [Polyaxon](https://github.com/polyaxon/polyaxon): reproducible machine learning at scale
* [Datmo](https://github.com/datmo/datmo):  replicable model versions
* [MLFlow](https://github.com/databricks/mlflow): machine learning experiment tracking
* [ModelDB](https://github.com/mitdbg/modeldb): system for managing machine learning models for scikit-learn & spark.ml
* [DVC](https://github.com/dataversioncontrol/dvc): replicable etl and feature extraction pipelines
* [CookieCutter Data Science](https://github.com/drivendata/cookiecutter-data-science): replicable file structures for data projects 
* [Docker CookieCutter Data Science](https://github.com/manifoldai/docker-cookiecutter-data-science):  fork of above to run cookie-cutter project in a Docker container
* [Duct Tape](https://github.com/jhclark/ducttape):  replicable running of code 
* [Dynamic Training Bench](https://github.com/galeone/dynamic-training-bench): tensorflow training and tuning 
* [Sacred](https://github.com/IDSIA/sacred): reproduce experiments with a GUI to track 
* [Pachyderm](https://github.com/pachyderm/pachyderm): reproducible way to version data and ETL pipelines
* [Django Estimators](https://github.com/fridiculous/django-estimators): specific to django and scikit-learn estimators
* [MAX](https://github.com/IBM/MAX): model template for tracking model types
* [Kinoa](https://github.com/oleg-panichev/kinoa): save experiment results easily

## Continuous Integration 

SaaS Tools
* [Argo](https://argoproj.github.io/): Open source Kubernetes native workflow engine for orchestrating parallel jobs (incudes workflows, events, CI and CD).
* [CircleCI](https://circleci.com/): Language-Inclusive Support, Custom Environments, Flexible Resource Allocation, used by instacart, Lyft, and StackShare.
* [Travis CI](https://travis-ci.org/)
* [Buildkite](https://buildkite.com/): Fast and stable builds, Open source agent runs on almost any machine and architecture, Freedom to use your own  tools and services

Open Source
* [Jenkins](https://jenkins.io/download/): Open source on device build system

## Training for Machine Learning / Deep Learning
Open Source 
* [SystemML](https://systemml.apache.org/) - for big data applications using Spark
* [FfDL](https://github.com/IBM/FfDL)

## For Production Systems / Model Serving
Open  Source
* [Hydrophere Data](https://github.com/Hydrospheredata)
* [Clipper](https://github.com/ucbrise/clipper)
* [Seldon](https://github.com/SeldonIO/seldon-core)

## End-to-End
SaaS Proprietary
* [Tensorflow Extended (TFX)](https://github.com/tensorflow/tfx)
* [Michelangelo](https://eng.uber.com/michelangelo/)
* [Google Cloud AI Platform](https://cloud.google.com/ai-platform/) 
* [Amazon SageMaker](https://aws.amazon.com/sagemaker/) 
* [Neptune](https://neptune.ml/) 
* [Floydhub](https://www.floydhub.com/) 
* [Paperspace](https://www.paperspace.com/) 
* [Determined AI](https://determined.ai/) 
* [Domino Data Lab](https://www.dominodatalab.com/) 

References
* https://www.researchgate.net/publication/229869757_An_Introduction_to_Model_Versioning
