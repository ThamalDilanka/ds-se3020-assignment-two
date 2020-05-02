# Fire Alert 
## Distributed Systems | SE3020 - Assignment 2 - REST API

### Contributers
Student ID | Name
-----------|--------------
IT18009132 | Dilanka R.M.T.
IT18001112 | Tharaka W.C.M.K.
IT18007848 | Rathnayake R.H.C.S.
IT18006476 | Gunarathna G.K.N.L.

### Presentation Video - Watch on YouTube
[![FireAlert](https://i.ibb.co/KNyT8Lq/youtube.png)](https://www.youtube.com/watch?v=X1D8vReTA1Y&feature=youtu.be)

### Derectory Structure
There are four separate applications in this repository. Here are the details of the directories you could find above.

Directory or File | Descritption
------------------|---------------
fire-alert-api | The REST API of the system
fire-alert-rmi | The RMI server and desktop client application
fire-alert-web | The web client application
fire-alert-sensor | Fire sensor simulator application
database | Sample collection files of the system
Fire Alert System Documentation.pdf | Complete Documentation of the system
Install.txt | Deployment process (You can find the same details in the following section)

### Deployment

> Your PC should have installed 10.0 or above version of Node.js runtime environment and JDK 11 or above version.

#### REST API
1. Clone this repository and open the CMD inside the `fire-alert-api` directory.
2. Set the all environment variables which has defined inside the `config.env` file. You may provide values for following keys.

  * DATABASE - connection string of the MongoDB database
  * DATABASE_PASSWORD - password of the cluster admin
  * JWT_SECRET - define a secret for the JSON Web Token
  * JWT_EXPIRES_IN - define the valid preriod of a token
  * EMAIL_SENDING_ACCESS_TOKEN - define a email sending token
  * EMAIL_FROM - the email that sending the alerts
  * SENDGRID_API_KEY - SENDGRID Api key 
  * MESSAGEBIRD_ACCESSKEY - Messagebird access key

3. Run 'npm start' script to run the application. It will start on port 8000, unless you changed the port in the `fire-alert-api/config.env` file

> Note: Since most of the above environment variables should not be exposed to the public, those are removed from the repository. However, all other components of the system are using the hosted version of API and this API has been deployed on the **Heroku** platform. [This link](http://fire-alert-solution.herokuapp.com/) could be used instead of running the API on your machine. You may refer the [API documentation](https://github.com/ThamalDilanka/ds-se3020-assignment-two/blob/master/fire-alert-api/README.md) for more details.

#### RMI Server adn Desktop Client Application

* Both RMI Server and Desktop Client run in localhost.
* Below external libraries should be added to the classpath of the project. They have been provided in the dependencies folder inside the fire-alert-rmi 

	commons-logging-1.2.jar
	commons-logging-1.2-javadoc.jar
	httpclient-4.3.1.jar
	httpcore-4.3.2.jar
	json-20190722.jar

* Run RMIServer using Run as Java Application option.
* You must have the internet connection when the RMIServer is    
  running.
* Run the desktop client.

#### Web Client Application
1. Clone this repository and open the CMD inside the `fire-alert-web` directory.
3. Run 'npm start' script to run the application. It will start on port 3000.

> Note: This application has been hosted in **GitHub Pages**. You may use [this link](https://thamaldilanka.github.io/fire-alert-web/) to access the live version of the web client application. 

#### Fire Sensor Simulator Application
There are two options to run this application. You may use the packaged version of the application unless you want to customize sensor id and others.

##### Run the executable file
1. Clone this repository and run the executable file inside the `fire-alert-sensor/dist/Fire Sensor FSID100.exe` directory.

##### Run using the script
1. Clone this repository and open the CMD inside the `fire-alert-sensor` directory.
3. Run 'npm start' script to run the application.
