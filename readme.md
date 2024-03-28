
<h1 align="center">
  Unofficial World Cube Association (WCA) Public API - LIVE data
  <br>
  <br>
 <p><a href=""><img src="https://i.ibb.co/nQgzJ0P/wca-api.png" alt="WCA API" width="200"></a></h1>
</h1>
 <center>
<p align="center">
 <a href=""><img src="https://img.shields.io/badge/heroku-%23430098.svg?style=for-the-badge&logo=heroku&logoColor=white" alt="WCA API"></a>
  <a href=""><img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" alt="WCA API"></a>
    <a href=""><img src="https://img.shields.io/badge/-selenium-%43B02A?style=for-the-badge&logo=selenium&logoColor=white" alt="WCA API"></a>
 </p>
   
## Key Features
Welcome to the **unofficia**l World Cube Association (WCA) Public API documentation! 
With this API you will receive  **data in real-time**.

I'm not affiliated with or part of the official WCA software team.

**Note**: This V1 version will be updated multiple times during the next weeks till V2 a stabilized version is released.

**Note**: Currently this app is running in the staging Phase (that is the reason for the very long URL). Once Tests are done they will be moved to the production stage and the URL will change

## Open Endpoints

| Endpoint             | description
| :---------------- | :------: 
| [comp](/V1/competitions.md)    |   Get the next competitions as presented from https://www.worldcubeassociation.org/competitions
| [results](/V1/results.md)    |   Get all results as presented from [https://www.worldcubeassociation.org/results/rankings/333/single](https://www.worldcubeassociation.org/results/rankings/xxx/single)
| [records](/V1/records.md)    |   Get all results as presented from [https://www.worldcubeassociation.org/results/records](https://www.worldcubeassociation.org/results/records)

### Feature highlights

#### Get the next competition registration date
>  Using the "next" option of the endpoint [comp](/V1/competitions.md)  you will receive the competitions the registration open date and time will be the next one  based on your region

## Endpoints that require Authentication
wip

## Support

## Issues
You can reach me the following way
- Create an issue
- Discord id: 528622643310624768
- [WCA Account](https://www.worldcubeassociation.org/persons/2023HETZ02)

## You may also like...
- Unofficial World Cube Association (WCA) Public API: https://github.com/robiningelbrecht/wca-rest-api
- Senior Ranking: https://logiqx.github.io/wca-ipy-www/Senior_Rankings.html#333-single-40-eu-de
- WIP: DiscordBot - WCABuddy

## Latest changes
- 10.11.2023: some bugfixes around gender and draft version of people api
- 13.11.2023: comps now also return google maps URL and separate cords
- 19.01.2024: comps name is now part of endpoint comp
- 25.03.2024: comps get a new attribute "next" to get the next competition based on the registration will open
