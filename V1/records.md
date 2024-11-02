# Show Current User

Get a subset of available data as presented from https://www.worldcubeassociation.org/records

**URL** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/records`

**Method** : `GET`

**Auth required** : No

**Permissions required** : None

## Parameters
  
optional:
- region
- event (222, 333, 444, 555, 666, 777, 333bf, 333fm, 333oh, clock, pyram, skewb, sq1, 444bf, 555bf, 333mbf)
- gender (male, female)

## Success Response

**Code** : `200 OK`

**Content examples**

- Get the records of all events (very time-consuming)

- **Post** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/records`
```json
 [
  [
    {
      "results": [
        {
          "event": "333",
          "region": ""
        }
      ]
    },
    {
      "result": [
        {
          "location": "Pride in Long Beach 2023",
          "name": "Max Park",
          "pos": "1",
          "region_rep": "United States",
          "time_s": "3.13"
        }
      ]
    },
    {
      "result": [
        {
          "location": "Flag City Summer 2023",
          "name": "Luke Garrett",
          "pos": "2",
          "region_rep": "United States",
          "time_s": "3.44"
        }
      ]
    },
    {
      "result": [
        {
          "location": "Wuhu Open 2018",
          "name": "Yusheng Du (杜宇生)",
          "pos": "3",
          "region_rep": "China",
          "time_s": "3.47"
        }
      ]
    }
  ],
  [
    {
      "results": [
        {
          "event": "222",
          "region": ""
        }
      ]
    },
  ...
```

- Get the records only from 444

- **Post** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/records?event=444`
```json
{
    "results": [
      {
        "event": "444",
        "region": ""
      }
    ]
  },
  {
    "result": [
      {
        "location": "Bay Area Speedcubin' 29 PM 2022",
        "name": "Max Park",
        "pos": "1",
        "region_rep": "United States",
        "time_s": "16.79"
      }
    ]
  },
  {
    "result": [
      {
        "location": "French Championship 2023",
        "name": "Sebastian Weyer",
        "pos": "2",
        "region_rep": "Germany",
        "time_s": "17.13"
      }
    ]
  },
  {
    "result": [
      {
        "location": "Altona Algorithms Attempt 2 2021",
        "name": "Feliks Zemdegs",
        "pos": "3",
        "region_rep": "Australia",
        "time_s": "17.98"
      }
    ]
  },
  ...
```
- Get the records only from 444 of Switzerland

- **Post** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/records?event=444&region=switzerland`
```json
[
  [
    {
      "results": [
        {
          "event": "333",
          "region": "Switzerland"
        }
      ]
    },
    {
      "result": [
        {
          "location": "WCA European Championship 2022",
          "name": "Richard Delacoste",
          "pos": "1",
          "region_rep": "Switzerland",
          "time_s": "4.63"
        }
      ]
    },
    {
      "result": [
        {
          "location": "Swisscubing Cup V 2022",
          "name": "Julian Bürgi",
          "pos": "2",
          "region_rep": "Switzerland",
          "time_s": "5.27"
        }
      ]
    },
    {
      "result": [
        {
          "location": "Rheinland-Pfalz Open 2023",
          "name": "Alwin Rölz",
          "pos": "3",
          "region_rep": "Switzerland",
          "time_s": "5.68"
        }
      ]
    }
  ],
  ...
```
## Notes

* Without `event` or `region`, it is very time-consuming (around 10s)

  
