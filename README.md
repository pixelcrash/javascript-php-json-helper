# JSON FROM PHP -> JAVASCRIPT MULTIARRAY


## JSON FILE
```
<?php
header('Content-type: application/json');
?>

{
  "responses" :
    [
     {
      "type": "select",
      "question": "This is the question",
      "name": "question-two",
      "options": [
        {"text" : "question 1", "value" : "v1"},
        {"text" : "question 2", "value" : "v2"},
        {"text" : "question 3", "value" : "v3"}
      ]
    },
    
    {
     "type": "select",
     "question": "This is the question",
     "name": "question-two",
     "options": [
       {"text" : "question 1", "value" : "v1"},
       {"text" : "question 2", "value" : "v2"},
       {"text" : "question 3", "value" : "v3"}
     ]
   }
    ]
}
```

## JS Functions to access Elements

Respond saved in data
```
console.log(data);
```

### Get number of *responses*
```
var n = Object.keys(data.responses).length;
```

### Put options into an object
```
var objects = {};
var i = 0;

data.responses[i].options.forEach(function(entry) {
      console.log(entry.text + " " + entry.value);
      objects[i] = {text: entry.text, value: entry.value};
      i++;
  });
```
