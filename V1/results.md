# Show Current User

Get a subset of available data as presented from https://www.worldcubeassociation.org/results

**URL** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/results`

**Method** : `GET`

**Auth required** : No

**Permissions required** : None

## Parameters
must:
- event (222, 333, 444, 555, 666, 777, 333bf, 333fm, 333oh, clock, pyram, skewb, sq1, 444bf, 555bf, 333mbf),
  
optional:
- region

## Success Response

**Code** : `200 OK`

**Content examples**

- Get the results for 4x4

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
        "pos": "1",
        "name": "Max Park",
        "region_rep": "United States",
        "time_s": "16.79",
        "location": "Bay Area Speedcubin' 29 PM 2022"
      }
    ]
  },
  {
    "result": [
      {
        "pos": "2",
        "name": "Sebastian Weyer",
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
        "pos": "1",
        "name": "Richard Delacoste",
        "region_rep": "Switzerland",
        "time_s": "21.25",
        "location": "Norwegian Championship 2022"
      }
    ]
  },
  {
    "result": [
      {
        "pos": "2",
        "name": "Alwin Rölz",
        "region_rep": "Switzerland",
        "time_s": "23.05",
        "location": "Swisscubing Cup II 2023"
      }
    ]
  },
  ...
```

## Notes

* Only one `event`  can be used. E.g.: event=333&event=444.. is not available
* Requesting without `region` parameter will only sent back the next 10 competitions from the list

  