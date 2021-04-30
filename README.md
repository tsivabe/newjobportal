
Python Django JobPortal Website
===============================

Step1: Create a project folder and clone the repository

    git clone git@github.com:x20182473/newjobportal.git

Step2: Activate virtual environment to avoid breaking your internal packages
    virtualenv env
   source env/bin/activate

Step3: install pre-requisites:
    pip install -r requirements.txt

 Website runs with Amazon RDS (Postgres Database)
 Configure the database setting in settings.py (update the below parametes based on your setup)

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'postgres',
        'USER': 'postgres',
        'PASSWORD': 'database',
        'HOST': 'database1.cpqkd85h5c1y.us-east-1.rds.amazonaws.com',
        'PORT': '5432',


python manage.py makemigrations 
python manage.py migrate

Step4: Collect static content to the application

python manage.py collectstatic

Step5: run the server locally to validate

python manage.py runserver 0.0.0.0:8080


Prepare the server for Elastic bean stack deployment by setting the config filee

Add __pycache__/ on .gitignore

Launch the application on EBS by creating the Pipeline:
1) Create EBS environment and application:

2) Create Pipeline
map the pipeline to github repository
create deploy project
create teh code pipeline

