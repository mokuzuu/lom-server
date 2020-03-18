# lom-server

API server for lom

## Main features of the app
- Login/Signup (MUST)
- The user register a new word (MUST)
- The user can see all words in list (MUST)
  - A word name
  - Registration date and time
  - correctness
- The user can see a detail of the word (MUST)
  - A word name
  - Registration date and time
  - correctness
  - description
  - note
  - Dates and time when the user tests a word
- The user can test how much they remember words (MUST)
- The user can filter a list by
  - alphabet (MUST)
  - percentage of correctness (MUST)

## DATABASE
- User
  - id: `string` `required` `primary key` `email can be used`
  - username: `string` `required`
  - icon: `img` `required`
  - dictionary_id: `Dictionary ID array` `required` `foreign key`

- Dictionary
  - id: `number` `increment` `required` `primary key`
  - words: `number array` `foreign keys`

- Words
  - id: `number` `increment` `required` `primary key`
  - name: `string` `required` 
  - registration_time: `Date` `required`
  - test
    - time: `Date array`
    - number_of_try: `number`
    - number_of_correctness: `number`
  - description: `string`
  - note: `string`


## APIs
- `/signup` : Create a new user
- `/login` : Login an existing user