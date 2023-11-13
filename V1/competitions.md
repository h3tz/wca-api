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

- **GET** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/comp?region=switzerland`
```json
[
  {
    "competition": [
      {
         "region":"Switzerland",
         "date":"Dec 16 - 17, 2023",
         "venue":"Sala Multiuso Sonvico",
         "url":"https://www.worldcubeassociation.org/competitions/TicinoWinterOpen2023",
         "reg_open_utc":"2023-10-17T19:00:00Z",
         "reg_close_utc":"2023-12-06T19:00:00Z",
         "gmaps_url":"https://www.google.com/maps/place/46.057547,8.990467",
         "gmaps_lat":"46.057547",
         "gmaps_lng":"8.990467"
      }
    ]
  },
    ...  
]
```

- Requesting the upcoming competetions (restricted to the next 10)

- **GET** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/comp`
```json
[
  {
    "competition": [
      {
        "region":"Colombia",
        "date":"Nov 13, 2023",
        "venue":"Centro Comercial Casablanca",
        "url":"https://www.worldcubeassociation.org/competitions/MadridCundinamarcaII2023",
        "reg_open_utc":"2023-09-14T19:00:00Z",
        "reg_close_utc":"2023-11-11T19:00:00Z",
        "gmaps_url":"https://www.google.com/maps/place/4.72708,-74.256817",
        "gmaps_lat":"4.72708",
        "gmaps_lng":"-74.256817"
      }
    ]
  },
  {
    "competition": [
      {
         "region":"United States",
         "date":"Nov 13, 2023",
         "venue":"Plymouth Arts and Recreation Center",
         "url":"https://www.worldcubeassociation.org/competitions/MichiganMini82023",
         "reg_open_utc":"2023-10-18T00:00:00Z",
         "reg_close_utc":"2023-11-10T00:00:00Z",
         "gmaps_url":"https://www.google.com/maps/place/42.373885,-83.467277",
         "gmaps_lat":"42.373885",
         "gmaps_lng":"-83.467277"
      }
    ]
  },
  
    ...
]
```

## Notes

* Only `regions`  as offered from https://www.worldcubeassociation.org/competitions can be used.
* Requesting without `region` parameter will only sent back the next 10 competitions from the list

  
