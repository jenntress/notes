# Postman Instructions
- GET: use url http://localhost:3001/api/villains/ or superheroes
- POST: select Body at the top, and x-www.form-urlencoded
- POST multiple powers: multiple lines(inputs) of evilPower "doesn't work csv!"
- POST new note to superhero: we need the hero's Id and the route name: note.
  ex:localhost:3001/api/superheroes/note/58dc7ee5dd29d91d409cfea8. The body will be "content" for the key, and whatever for the value.
- PUT:

## async
- POST in JSON with async.each:
  -  "async.each" doing a bunch of things at once.. asynchronously (good for batching). async for each thing in this array of data, for each item in the array the function will execute. Must tell async when to quit - use "cb" - put it with whatever results I want once I've completed that action.
  - In postman, http://localhost:3000/api/superheroes/multiple-superPowers Go to POST, then Body, then "raw", then text dropdown to JSON, then type:
    {"data":[{ "name": "superman"},{ "name": "uberman" },{ "name": "loserman" }]}
