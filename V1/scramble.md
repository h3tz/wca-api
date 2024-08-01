# Show Current User

Receive a scramble

**URL** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/scramble`

**Method** : `GET`

**Auth required** : No

**Permissions required** : None

## Parameters
- event (222, 333, 444, 555, 666, 777, clock, pyram, skewb, minx)

## Success Response

**Code** : `200 OK`

**Content examples**

- Requesting clock scramble

- **GET** : `https://wcascrap-64e44a2b3e5b.herokuapp.com/api/V1/scramble?event=clock`
```json
[
  {
    "result": [
      {
        "event": "clock",
        "scramble": "UL2 UL1 D5 D3 R6 D1 UL5 R1 UL4 R5 R4 DL5 DR5 U5"
      }
    ]
  }
]
```
## Notes

* So far it is  just returning the scramble without any usability checks. Community feedback welcome.
  
