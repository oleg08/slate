# Students Camps

## Get All Students Camps

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```shell
curl "https://yolo-study.com/api/v1/adminpanel/students_camps" \
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 3,
    "name": "Інтенсив з граматики",
    "course": "Інтенсив з англійської „Дази&Діди”",
    "course_id": 80,
    "aasm_state": "confirmed",
    "teacher": "Христина Тинкалюк",
    "teacher_id": 60,
    "users_amount": 8,
    "finished_lessons": 9
  },
  {
    "id": 4,
    "name": "Інтенсив з граматики 04.06",
    "course": "Інтенсив з англійської „Дази&Діди”",
    "course_id": 80,
    "aasm_state": "unconfirmed",
    "teacher": "Христина Тинкалюк",
    "teacher_id": 60,
    "users_amount": 2,
    "finished_lessons": 0
  }
]
```

This endpoint retrieves all students camps.

### HTTP Request

`GET https://yolo-study.com/api/v1/adminpanel/students_camps`

## Get a Specific Students Camp

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "https://yolo-study.com/api/v1/adminpanel/students_camps/3" \
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "students_camp": {
    "id": 3,
    "name": "Інтенсив з граматики",
    "course": "Інтенсив з англійської „Дази&Діди”",
    "course_id": 80,
    "aasm_state": "confirmed"
  },
  "users": [
    {
      "id": 210,
      "email": "tadigitalagency@gmail.com",
      "name": "Ганна",
      "surname": "Шевченко",
      "avatar_url": "/images/original/missing.svg",
      "lessons_left": null
    },
    {
      "id": 1201,
      "email": "markovych@icloud.com",
      "name": "Mykola",
      "surname": null,
      "avatar_url": "/images/original/missing.svg",
      "lessons_left": null
    }
  ]
}
```

This endpoint retrieves a specific students-camp.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET https://yolo-study.com/api/v1/adminpanel/students_camps/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the students-camp to retrieve

## Create a Students Camp

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "https://yolo-study.com/api/v1/adminpanel/students_camps" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 5,
  "name": "Інтенсив з граматики",
  "course": "Інтенсив з англійської „Дази&Діди”",
  "course_id": 80,
  "aasm_state": "unconfirmed",
  "teacher": "Наталія Слободян",
  "teacher_id": 7,
  "users_amount": 0,
  "finished_lessons": 0
}
```

This endpoint creates a specific students-camp.

### HTTP Request

`POST https://yolo-study.com/api/v1/adminpanel/students_camps`

### URL Parameters

Parameter | sub-parameter | Description
--------- | ----------- | -----------
students_camp | name | name of the students-camp
-| teacher_id | Id of the assigned teacher
-| course_id | Id of the assigned course


## Update students-camp

```shell
curl "https://yolo-study.com/api/v1/adminpanel/students_camps/2" \
  -X PATCH \
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 5,
  "name": "Інтенсив з граматики",
  "course": "Інтенсив з англійської „Дази&Діди”",
  "course_id": 80,
  "aasm_state": "unconfirmed",
  "teacher": "Наталія Слободян",
  "teacher_id": 7,
  "users_amount": 0,
  "finished_lessons": 0
}
```

This endpoint updates a specific students-camp

### HTTP Request

`PATCH https://yolo-study.com/api/v1/adminpanel/students_camps/2`

### URL Parameters

Parameter | sub-parameter | Description
--------- | ----------- | -----------
students_camp | name | name of the students-camp
-| teacher_id | Id of the assigned teacher
-| course_id | Id of the assigned course

## Delete a Specific students-camp

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "https://yolo-study.com/api/v1/adminpanel/students_camps/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE hhttps://yolo-study.com/api/v1/adminpanel/students_camps/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete
