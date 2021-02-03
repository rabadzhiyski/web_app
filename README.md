# web_app
World Bank Data Dashboard of top 10 World Economies

## Contents
The repository contains an example of a web application installed on [Heroku](https://heroku.com)

## Libraries
flask
pandas
plotly
gunicorn


## Heroku installation
Before doing the steps create a free account to Heroku.

**1. Update conda and create a virtual environment** (in case Anaconda installed, if not, skip that step).

''' conda update python
python3 -m venv worldbankvenv
source worldbankenv/bin/activate '''

**2. Install the necessary libraries**
pip install flask pandas plotly gunicorn

**3. Go to the app folder**
cd "app folder"

**4. Install heroku**
curl https://cli-assets.heroku.com/install-ubuntu.sh | sh
https://devcenter.heroku.com/articles/heroku-cli#standalone-installation

**5. Check verison to confirm installation.**
heroku --version

**6. Login to heroku (it should open your browser, click ok)**
heroku login

**7. Create Procfile**
touch Procfile

**8. Write the below in the Procfile**
web gunicorn myapp:app

**9. Create requirements file (be carefull as errors appear if python/numpy/pandas versions are not supported)**
pip freeze > requirements.txt

**10. Add initialize repository and commit**
git init
git add .
git commit -m ‘first commit’

**11. Create app in heroku**
heroku create my-app-name

**12. Check if remote repository was added**
git remote -v

**13. Push to remote repository**
git push heroku master

## Acknowledgements
This web-app is part of Udacity Data Science Nanodegree program. 
Most of the code was already billed within the program exercise.
