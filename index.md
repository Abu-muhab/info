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