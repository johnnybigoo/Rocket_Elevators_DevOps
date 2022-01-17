<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="R2.png">
    <img src="./app/assets/images/_rocket/R2.png" alt="Logo" width="500" height="200">
  </a>

  <h3 align="center">Rocket Elevators DevOps
</h3>
  
  <p align="center">
    Odyssey Program - Week 14 
  </p>
</p>



<!-- ABOUT THE PROJECT -->
## About The Project

Rocket Elevators DevOps is one of the final project for the last 14th week.

By this week we had to configurate and deploy our website in another server. Examples suggested were Digitalocean or Vultr. I have choose Heroku
and as part of the DevOps project we must monitoring it with **New Relic** and **Google Analytics** services.

<br>

### Website deployed:
[https://rocket-elevators-devops.herokuapp.com/](https://rocket-elevators-devops.herokuapp.com/)


<br>

## Installation

Clone or download the .zip for this project. 

Here are the commands that will have to be entered in your terminal to start the server:
- mySQL server start
- ruby -v (To check if a corresponding version need to be installed)
- rails -v (To check if a corresponding version need to be installed)
- bundle install (To install all the necessary Gems)
- Create in the root `.env` file and add assign to variable `NEW_RELIC_KEY=` & `GOOGLE_ANALYTICS_KEY=`.
- Check in the directory for config/database.yml and if necessary replace the database password by yours.
- rails db:create
- rails s

<br>

Here are the commands that will have to be entered in your terminal when modifications are made in the database:
- Ctrl + C (to stop the server)
- rails db:migrate reset
- rails db:seed

<br>

### Preview
<br><hr>
### New Relic:
<br>

<img src="gifs/new-relic-1.gif" width="1050" height="550"/>

<br><hr>
### Google Analytics:
<br>
<img src="gifs/google-analytics-2.gif" width="1050" height="550"/>

<br>


<br>

## Built With

* [Ruby V-2.6.6](https://www.ruby-lang.org/en/)
* [Rails V-5.2.6](https://guides.rubyonrails.org/)
* [MySql V-5.7](https://dev.mysql.com/)
* [Bootstrap](https://getbootstrap.com)
* [JQuery](https://jquery.com)
* [Postgres V-10.18](https://www.postgresql.org/docs/10/release-10-18.html)


<br>