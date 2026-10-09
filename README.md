\# BentoML Iris Classification Service



A beginner-friendly machine learning deployment project built with Python, Scikit-learn, BentoML, and Docker.



\## Project Overview



This project demonstrates how to train an Iris classification model, serve predictions through a BentoML API, and run the service inside a Docker container.



\## Technologies Used



\- Python

\- Scikit-learn

\- BentoML

\- Docker

\- NumPy



\## Project Structure



```text

MLService/

├── train.py

├── test.py

├── service.py

├── bentofile.yaml

├── requirements.txt

├── .bentoignore

├── .gitignore

└── README.md

```



\## Features



\- Train an Iris classification model.

\- Create a prediction API using BentoML.

\- Package the model service into a Bento.

\- Containerize the service with Docker.

\- Test predictions through the `/classify` endpoint.



\## Run Locally



Install the dependencies:



```bash

pip install -r requirements.txt

```



Train the model:



```bash

python train.py

```



Test the model:



```bash

python test.py

```



\## Build and Run with BentoML and Docker



Build the Bento:



```bash

bentoml build

```



Check the available Bentos:



```bash

bentoml list

```



Containerize your Bento, replacing the tag with the one returned by `bentoml list`:



```bash

bentoml containerize iris\_classifier:YOUR\_TAG

```



Run the Docker image, again using your actual tag:



```bash

docker run --rm -p 3000:3000 iris\_classifier:YOUR\_TAG

```



Open the service documentation:



http://localhost:3000



\## API Testing



The service exposes a prediction endpoint:



`POST /classify`



Example request body:



```json

\[\[5.1, 3.5, 1.4, 0.2]]

```



Example prediction from my test:



```json

\[0]

```



The output represents the model's predicted class label for the supplied input.



\## Learning Outcome



Through this project, I practised training a machine learning model, creating an inference API with BentoML, containerizing a service with Docker, and testing the deployed endpoint.



This project is part of my ongoing journey in machine learning and MLOps.



\## Author



Humera Shaikh



GitHub: https://github.com/skhumera0202

