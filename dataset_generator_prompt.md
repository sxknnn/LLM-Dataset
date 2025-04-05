## Prompt:

Generate road-based navigation queries that involve multiple stops, time constraints, and specific route preferences (e.g., avoiding highways, using the fastest route, scenic routes, or gas stations). Provide the corresponding structured data in JSON format with fields: query, start, stops, end, arrive_by (if relevant), avoid (e.g., highways), preference (e.g., fastest), and any other necessary details. For example,

```
[
    {
        "query": "I need to go to my friend's house, then pick up a package from the post office, and finally head home before 7 PM.",
        "structured": {
            "start": "current_location",
            "stops": [
                {
                    "location": "friend's house"
                },
                {
                    "location": "post office"
                }
            ],
            "end": "home",
            "arrive_by": "19:00"
        },

    },
    {
        "query": "Plan a route from my home to the airport, but I want to stop at a pharmacy on the way.",
        "structured": {
            "start": "home",
            "stops": [
                {
                    "location": "pharmacy"
                }
            ],
            "end": "airport"
        },
    }, 
    {
        "query": "Find the fastest way to reach the mall, but avoid highways.",
        "structured": {
            "start": "current_location",
            "end": "mall",
            "avoid": [
                "highways"
            ],
            "preference": "fastest"
        },
    },
    {
        "query": "I need to drop my kid at school by 8 AM and then go to work.",
        "structured": {
            "start": "home",
            "stops": [
                {
                    "location": "school",
                    "arrive_by": "08:00"
                }
            ],
            "end": "work"
        },
    },
    {
        "query": "Take me to the nearest gas station and then continue to my destination.",
        "structured": {
            "start": "current_location",
            "stops": [
                {
                    "search": "gas station",
                    "location": "nearby"
                }
            ],
            "end": "destination"
        },
    },
]
```
