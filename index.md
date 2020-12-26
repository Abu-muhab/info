## Getting the questions

>Request
```
curl https://vazilegal.herokuapp.com/quiz/questions
-X GET
```
> Response
```
{
    "successful": true,
    "data": {
        "questions": {
            "1": {
                "options": [],
                "question": "Email",
                "index": 1,
                "actions": {
                    "any": "2"
                },
                "questionId": "WsckhFmHJqSc1JR7jVNg"
            },
            "2": {
                "options": [],
                "question": "Name",
                "index": 2,
                "actions": {
                    "any": "3"
                },
                "questionId": "dCUzl3wBzwUgRn0a6mwa"
            },
            "3": {
                "options": [
                    "Yes",
                    "No"
                ],
                "question": "Do you own a business?",
                "index": 3,
                "actions": {
                    "yes": "4",
                    "no": "END"
                },
                "questionId": "kOeSeliChbIIV3JXndqm"
            },
            "4": {
                "options": [
                    "Nigeria",
                    "US"
                ],
                "question": "Where is your business registered?",
                "index": 4,
                "actions": {
                    "us": "5",
                    "nigeria": "8"
                },
                "questionId": "LwpY0C8rOT4EH5gLcjgZ"
            },
            "5": {
                "options": [],
                "question": "What state is your business registered?",
                "index": 5,
                "actions": {
                    "any": 6
                },
                "questionId": "21Yecjb5CZQgBu9Ml5Zx"
            },
            "6": {
                "options": [
                    "LLC",
                    "S.Corp",
                    "C.Corp",
                    "None of the above"
                ],
                "question": "Which of the following best describes your business model?",
                "index": 6,
                "actions": {
                    "any": 7
                },
                "questionId": "mpwDmVU0gjT7CTzDTXVR"
            },
        }
    }
}
```

```
"actions": {
    "us": "5",
    "nigeria": "8"
},
```
> "actions" respresents the logic jump based on the answer to the question
> in the above code block, if the user answers "us", the next question would be question 5. if the user answers "nigeria", the next question would be question 8

```
"actions": {
    "yes": "4",
    "no": "END"
},
```
> In the above block, "END" means the user has alswered all that is required and the quiz should end

```
"actions": {
    "any": 7
},
```
> In the above block, "any" here means regardless of what was answered, the next question is 7

## Submitting quiz

>Request
```
curl https://vazilegal.herokuapp.com/quiz/submit_quiz
-X POST
-d "{
    "email": "abumuhab98@gmail.com",
    "responses": {
        //questionId:answer
        "1234RDFGH":"yes",
        "KKHFDFG56": "nigeria"
    }
}"
```
> Response
```
{
    successful: true,
    message: 'Diagnosis successful'
}
```