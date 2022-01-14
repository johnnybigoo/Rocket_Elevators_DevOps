<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://rocket-elevators-devops.herokuapp.com/assets/_rocket/R2-3c6296bf2343b849b947f8ccfce0de61dd34ba7f9e2a23a53d0a743bc4604e3c.png">
    <img src="https://rocket-elevators-devops.herokuapp.com/assets/_rocket/R2-3c6296bf2343b849b947f8ccfce0de61dd34ba7f9e2a23a53d0a743bc4604e3c.png" alt="Logo" width="500" height="200">
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
and as part of the DevOps project we must monitoring it with **New Relic** and **Google Analytics**

<br>

### Website deployed:
[https://rocket-elevators-devops.herokuapp.com/](https://rocket-elevators-devops.herokuapp.com/)


<br>

### Exemple of how the  *Speech Api* actually work:


First we create a *.wav* sound in this specific specs :
|# Rate                         |Format         |Channel  |
|-------------------------------|---------------|---------|
|`16000Hz`                        |`16-bit`       |`1(Mono)`|

We then enroll the *.wav* sound and extract them for modeling and then send to the database. Once enrolled we can use an other sample and let the **API** compare the 2 sounds together and then give a results based on the modeling from the first data we gave. The 2 major result are `Accepted (score > 0.5)` and `Rejected (score < 0.5)`.

> **Pros:** The **Speech-To-Text** worked really well and the transcription doesnt differ a lot from the true result.
> 
> **Cons:** The **Speech API** from  **Azure** as some flaws where it wont recognize enrolled voice from conversation.

## Installation

Clone or download the .zip for this project. 

Here are the commands that will have to be entered in your terminal to start the server:
- mySQL server start
- ruby -v (To check if a corresponding version need to be installed)
- rails -v (To check if a corresponding version need to be installed)
- bundle install (To install all the necessary Gems)
- Create in the root `.env` file and add assign to variable `AZURE_KEY=` your Azure speech service key.
- Check in the directory for config/database.yml and if necessary replace the database password by yours.
- rails db:create
- rails s

<br>

Here are the commands that will have to be entered in your terminal when modifications are made in the database:
- Ctrl + C (to stop the server)
- rails db:migrate reset
- rails db:seed

<br>

### Testing 
You don't need to be logged in, just click in SPEECH SERVICES menu tabe and choose service you desire to test.

> Put the audio file on your local drive to test the *speaker transcribe*.

<br>

[Click here to download the audio samples](https://github.com/johnnybigoo/ML-Audio-Samples.git)

<br>

- `Enroll` : The *enroll* section is used to create your voice profile inside the Database.
- `Upload` : The *Upload* section is used to test this audio clip against a voice profile.
- `Verify` : With the *verify* section you can test your Newly enroll profil ( or an older one) against and audio clip and verify if your test match !

<br>

To access the database, use Dbeaver or MySQLWorkbench, which shows a history of data stored in the server. The fictitious and real data covers the last 3 years of activity from companies. Graphical representations and charts will also be available in the stats page of the website. 

<br>

## Built With

* [Ruby V-2.6.6](https://www.ruby-lang.org/en/)
* [Rails V-5.2.6](https://guides.rubyonrails.org/)
* [MySql V-5.7](https://dev.mysql.com/)
* [Bootstrap](https://getbootstrap.com)
* [JQuery](https://jquery.com)
* [Postgres V-10.18](https://www.postgresql.org/docs/10/release-10-18.html)
* [Microsoft Cognitive Services](https://azure.microsoft.com/en-us/services/cognitive-services/)


<br>



