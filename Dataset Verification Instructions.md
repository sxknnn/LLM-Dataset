 ## Dataset Verification Instructions

### Structure Consistency:
The structure of the query must match the corresponding structured data. Ensure all fields are correctly represented (e.g., origin, destination, stops, preferences).

### Project Relevance:
* The query must be related to our project, which is focused on road-based navigation.
* Remove any queries about air travel, waterways, boats, or other unrelated topics.
* Ensure the queries are related to road navigation or multi-destination travel.

### Reporting:
* If you find any issues, note the index number and describe the problem in the comment section.
* If everything looks correct, simply write "No comment" in the comment section.

### How to Fill in the Excel Sheet:
* Index Number: Enter the index number of the query with the error.
* Query: Fill it by the same query.
* Comment:
  * If there’s an issue (such as a mismatch or an irrelevant query), note the index number and describe the issue.


### For Example:
```
    {
        "query": "Take me to the train station using public transport.",
        "structured": {
            "start": "current_location",
            "end": "train station",
            "mode": "public_transport"
        },
        "index": 8
    },
    {
        "query": "I want to go to the beach but avoid toll roads.",
        "structured": {
            "start": "current_location",
            "end": "beach",
            "avoid": [
                "tolls"
            ]
        },
        "index": 9
    },
```
| Index | Query | Comment |
| ----- | ----- | ------- |
| 8 | Take me to the train station using public transport. | Irrelevant Query |
|  |  |  |
