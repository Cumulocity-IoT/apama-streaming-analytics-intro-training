# Introductory training for Apama

*WORK IN PROGRESS*

This repository contains slides and Apama code for individual/group exercises to learn about Apama.

Course is designed to be taken in-person with access to an Apama installation for each participant. Course length about four hours.

The Slides cover an introduction to Apama and its use cases, integration with other products inside and outside SAG and cloud deployment. The EPL code provides practical learning exercises. for working with EPL and doing various analytic tasks.

The excercises are designed with active learning principles in mind. They start with a short series of problems to be worked through with the organizer, followed by a larger set of tasks for the particpants to work on in groups with help from the organizer using the documentation provided.

This was created for the SAG Global Architect Program 2018-2019 by Matthew Johnson

To run this course you need to:

* Replace the host of the docker server you're doing to deploy the server into into the following files:
    * ```training_monitor/config/connectivity/DigitalEventServices/DigitalEventServices.properties```
    * ```training_client/config/connectivity/DigitalEventServices/DigitalEventServices.properties```
    * ```training_server/config/connectivity/DigitalEventServices/DigitalEventServices.properties```
    * ```Apama Gap Training.pptx``` (on the slide on Apama in the Cloud describing configuring your docker client)
* Produce a zip file for distributing to the trainees consisting of:
    * ```training_client```
	 * ```TypeRepository```
	 * ```doc```
	 * ```docker.exe``` (a copy of the windows docker client executable)
* Start the server processes in your docker server with:
    ```docker stack deploy -c docker-compose.yml training```
* Open the ```training_monitor``` project in your designer and run it to see the dashboard

This will allow your trainees to use the client project to run analytics, with their alerts shown on your dashboard. You will also be able to demo the Grafana integration by logging into port 39090 on your Docker server with admin/admin.

______________________
These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.

Contact us at [TECHcommunity](mailto:technologycommunity@softwareag.com?subject=Github/SoftwareAG) if you have any questions.


