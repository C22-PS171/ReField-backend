# ReField Backend
This is backend repository of ReField App using restful API   

## Technology
This ReField backend is created with:
* Node.js using library framework express.js
* Database service using Google Cloud SQL (MySQL 5.7)
* Deployment backend app service using Goole App Engine
* CI/CD service to automation deployment process that linked with this repository using Google Cloud Build

## Run the ReField Backend App
### 1. Run this backend app in local:
``` bash
# Open your text editor (Visual Studio is recommended text editor)
# Make sure you install node.js
# Open terminal then run the command below:

# Clone this repository
$ git clone https://github.com/C22-PS171/ReField-backend

# Go into the app's directory
$ cd ReField-backend
```

> Configuration to connect to your database
``` bash
# Make sure u have your own database (your database must MySQL database, phpMyAdmin is recommended)
# Do the step below:

- Open .env file and change configuration (connection string) with your database connection: 

DB_HOST=<YOUR_DATABASE_HOST>
DB_USER=<YOUR_DATABASE_USER>
DB_PASS=<YOUR_DATABASE_PASSWORD>
DB_NAME=<YOUR_DATABASE_NAME>
DB_PORT=<YOUR_DATABASE_PORT>
```

> Run the backend app
``` bash
# In app's directory (ReField-backend) do this command below:

# Install all apps's depedencies
$ npm install

# Run the app
$ npm start
```

### 2. Run this backend app using Google Cloud Platform services:
> Cloud SQL (Database service)
``` bash
# Open your GCP console go to SQL tab in the left side bar, enable and create instance in Cloud SQL then create database in that instance
# Make sure you create MySQL instance, this app using MySQL 5.7 version
# Setting instance connection to public
```

> Cloud Build (CI/CD service)
``` bash
# Create an empty repository github
# Open your GCP console go to Cloud Build tab in the left side bar, go to triggers tab then create trigger
# Link your trigger to the repository you've made before
# Make sure you add variabel then fill in the value with your connection string to your SQL instance and database like image below
```
![Trigger](https://user-images.githubusercontent.com/106735115/173184683-4a40e142-2860-4428-aa36-c6da7350bd25.png)


> App Engine (Deployment service)
``` bash
# Download the code from this backend repository then push or upload it to your empty repository
# CI/CD service will run then it also will automation the deployment process
# When deployment service is succes in Cloud Build console in history tab will appear checklist mark, if not succes then will appear cross mark like image below
```
![CBuild](https://user-images.githubusercontent.com/106735115/173185090-468655fd-caec-47a7-b221-e2f2a31bec67.png)

``` bash
# When deployment service is succes go to App Engine tab then go to services tab there is column name Service that is contain link to your data
# Make sure you add route endpoint to get the data, you can see the route endpoint in server.js file
# If the route endpoint you've add true it will return the data like image below
```
![link](https://user-images.githubusercontent.com/106735115/173185288-4de986b7-c063-4b56-8002-f84308022665.png)

