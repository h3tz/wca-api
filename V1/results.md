# Show Current User

Get a subset of available data as presented from https://www.worldcubeassociation.org/records

**URL** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/records`

**Method** : `GET`

**Auth required** : No

**Permissions required** : None

## Parameters
  
optional:
- region
- event (222, 333, 444, 555, 666, 777, 333bf, 333fm, 333oh, clock, pyram, skewb, sq1, 444bf, 555bf, 333mbf),

## Success Response

**Code** : `200 OK`

**Content examples**

- Get the records of all events (very time consuming)

- **Post** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/api/V1/results?event=444`
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
        "time_s": "17.13",
        "location": "French Championship 2023"
      }
    ]
  },
  ...
```

- Get the results for 4x4 from switzerland

- **Post** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/api/V1/results?event=444&region=Switzerland`
```json
[
  {
    "results": [
      {
        "event": "444",
        "region": "Switzerland"
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

## Notes

* Only one `event`  can be used. E.g.: event=333&event=444.. is not available
* Requesting without `region` parameter will only sent back the next 10 competitions from the list

  
