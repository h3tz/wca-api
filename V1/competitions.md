# Show Current User

Get a subset of available data as presented from https://www.worldcubeassociation.org/competitions

**URL** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/comp`

**Method** : `GET`

**Auth required** : No

**Permissions required** : None

## Parameters

- region

## Success Response

**Code** : `200 OK`

**Content examples**

- Requesting all upcoming competetions in switzerland

- **Post** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/comp?region=switzerland`
```json
[
  {
    "competition": [
      {
        "region": "Switzerland",
        "date": "Nov 11 - 12, 2023",
        "venue": "Swiss Science Center",
        "url": "https://www.worldcubeassociation.org/competitions/SwissScienceOpen2023",
        "reg_open_utc": "2023-10-09T17:00:00Z",
        "reg_close_utc": "2023-10-11T06:12:05Z"
      }
    ]
  },
  {
    "competition": [
      {
        "region": "Switzerland",
        "date": "Dec 16 - 17, 2023",
        "venue": "Sala Multiuso Sonvico",
        "url": "https://www.worldcubeassociation.org/competitions/TicinoWinterOpen2023",
        "reg_open_utc": "2023-10-17T19:00:00Z",
        "reg_close_utc": "2023-12-06T19:00:00Z"
      }
    ]
  },

    ...  
]
```

- Requesting the upcoming competetions (restricted to the next 10)

- **Post** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/comp`
```json
[
  {
    "competition": [
      {
        "region": "Spain",
        "date": "Nov 1, 2023",
        "venue": "Centro Comercial Sant Boi & Xperience",
        "url": "https://www.worldcubeassociation.org/competitions/NhoodXperienceSideEvents2023",
        "reg_open_utc": "2023-10-03T17:15:00Z",
        "reg_close_utc": "2023-10-29T22:59:00Z"
      }
    ]
  },
  {
    "competition": [
      {
        "region": "Iran",
        "date": "Nov 2, 2023",
        "venue": "Ferdowsi Hotel (هتل فردوسی)",
        "url": "https://www.worldcubeassociation.org/competitions/ChekaadAutumn2023",
        "reg_open_utc": "2023-10-07T14:30:00Z",
        "reg_close_utc": "2023-10-19T20:30:00Z"
      }
    ]
  },
  
    ...
]
```

## Notes

* Only `regions`  as offered from https://www.worldcubeassociation.org/competitions can be used.
* Requesting without `region` parameter will only sent back the next 10 competitions from the list

  