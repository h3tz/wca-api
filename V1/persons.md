# Show Current User

Get a subset of available data as presented from https://www.worldcubeassociation.org/competitions

**URL** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/persons`

**Method** : `GET`

**Auth required** : No

**Permissions required** : None

## Parameters
- wcaid
  
### optional

## Success Response

**Code** : `200 OK`

**Content examples**

- Requesting personal information (so far just very high level)

- **GET** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/persons?wcaid=2023HETZ02`
```json
[ 
  { "result": [ 
    { 
      "wcaid": "2023HETZ02",
      "country": "Germany",
      "sex": "Male",
      "compCount": "11",
      "successfulltries": "176",
      "avatar_url": "https://avatars.worldcubeassociation.org/uploads/user/avatar/2023HETZ02/1698178795.jpg", "events": [] 
    }
  ] 
 }
]
```

## Notes
- Only the full WCAID requests are currently supported (e.g. 2023HETZ01). In case more than one person will be available (e.g. you request just 2023) will not return all person's information from every one have 2023 in its WCAID.
