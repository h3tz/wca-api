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
      "result":[
         {
            "event":"clock",
            "scramble":"(uuuu,5,5)(uUUu,0,3)(UUuU,-2,-2)(uUuU,4,4)(uUUU,0,5)(uUUU,-5,-4) y2 (UUUu,-4,-2)(uuUU,2,-3)(UuuU,-5,-5)(uuUU,5,0)(UUuU,-3,1)(uuuU,-5,2)"
         }
      ]
   }
]
```
## Notes

* So far it is  just returning the scramble without any usability checks. Community feedback welcome.
  
