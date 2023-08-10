<html>
  <body>
    <h1>Blog Post: Developing an Offline Geocoding App</h1>
  </body>
</html>

Published: 08/09/2023

**Introduction to SafeGeocoder**

Last semester I completed a course called GIS Application Development. We were tasked with developing an application that intersected with GIS analysis and techniques over the duration of a semester. I worked closely with two other classmates using agile methods to develop the GIS application known as SafeGeocoder.

SafeGeocoder is a code-free offline geocoder with a simple but friendly user interface that allows researchers to geocode a set of patient addresses securely. It works by building a Docker container on the local machine, using PostGIS to pull street line files and store them in Docker, and using PostGIS functions in Python to geocode against the Docker container. The whole thing is wrapped in a self-contained and downloadable executable file and opens in a point-and-click graphical user interface (GUI).

My co-developer for this project has received funding for an intern to continue working on the project as she is seeking to present and publish this fall.

<img src="https://xmcgill.github.io/Geocoder.jpg" width="500" height="400">

Figure 1. SafeGeocoder GUI

**Motivation for Development**

Medical geography is a subfield of geography that focuses on the spatial patterns and processes of health and disease. In a cancer prevention setting, we use medical geography to identify clusters of higher-than-expected disease burden and to test associations between cancer outcomes and environmental, social, and economic factors, including access to healthcare, air and water quality, and social inequalities, and to inform interventions. All of these require the use of geocoded data. While there are many free and fast ways to geocode, all of them require you to send addreses data over a server. Because of data security concerns, the strictest health researchers won’t send patient addresses to remote servers for geocoding. The only existing methods for offline geocoding are expensive, cumbersome, or require working with code, which are all limiting factors for many researchers. So, we made this standalone desktop application to geocode addresses through a friendly GUI without ever sending them off the local machine. We included the capability to jitter coordinates before returning them as a CSV or SHP to protect patient data further. And for researchers interested in the characteristics of the patient’s residence, we added the ability to attach standard census tract-level socioeconomic and sociodemographic data, such as socioeconomic and race data.

**Limitations**

•	You must already have Docker Desktop downloaded and installed on your computer to use this application.

•	Downloading street data can take a while! Geocoding can too, but not as long. This is the cost of geocoding secuely, but you won’t have to download the same files twice, so once you geocode in a state, you won’t have to wait the next time you need to geocode in the same state.

•	Currently we have limited functionality (geocode, jitter, add census data), but we plan to build in more in the future!

**What I Learned**

How to create an app

Package an app

Learned about docker containers

Learned basic SQL

Debugged in python

Built a GUI using QT designer

