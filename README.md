# AI-Travel-Genie-MultiAgent
TravelAI Genie is a multi-agent itinerary planner that uses OpenAI models, RAG, and OpenTripMap data to build smart travel plans. It handles user prompts, destination analysis, daily schedules, and reasoning steps while giving explainable itineraries. Built for my Applied GenAI course project.

TravelAI Genie – Multi-Agent Travel Planner
A GenAI project built as part of my Applied Generative AI coursework. The idea was simple: can an AI plan a trip the way a real travel consultant would? So I built a multi-agent workflow that reads user prompts, fetches real city data, reasons through it, and creates a personalized travel itinerary.

1. What this project does
TravelAI Genie takes a natural-language travel request and turns it into a structured itinerary.
Here’s what’s happening under the hood:
A Planner Agent breaks the prompt into location, dates, preferences, budget factors.
A Data Agent pulls attractions using the OpenTripMap API plus a local RAG store for supporting info.
A Reasoning Agent evaluates distance, timing, day planning, and feasibility.
A Writer Agent prepares a clean, readable itinerary that feels like a real recommendation.
The whole process runs inside a multi-agent workflow built using OpenAI, LangChain, CrewAI, and ChromaDB.
The goal was to handle a wide variety of cases:
– solo trips
– family travel
– multi-city plans
– fixed or flexible dates
– activity preferences (food, nightlife, culture, nature)

2. Key Features
Natural-language itinerary generation
Multi-agent architecture for structured reasoning
Real-time attraction lookup through OpenTripMap
RAG with vector embeddings for extra context
Custom day-by-day scheduling logic
Error-handling for edge cases like invalid dates or unsupported cities
Clear output formatting for use in demos and reports

3. Tech Stack
Languages: Python
Models: OpenAI GPT models
Frameworks: LangChain, CrewAI
Vector Store: ChromaDB
APIs: OpenTripMap API
Other Libraries: requests, datetime, pandas

4. How it works (Step-By-Step Flow)
User enters a travel prompt.
Planner Agent interprets:
destination
trip length
travel style
constraints
Data Agent fetches attractions using OpenTripMap.
RAG layer enriches the attraction details using vector similarity search.

5. Why I built this
I wanted to explore how agent-based systems behave when they have to collaborate on an open-ended task. Travel planning is messy—there’s a lot of ambiguity, missing data, and user intent that needs interpretation.
This project helped me learn:
how to structure multi-agent reasoning
how to integrate APIs inside agent workflows
how RAG improves factual grounding
how to build explainable AI outputs
how to debug long-running agent executions
Reasoner Agent organizes activities into a feasible plan.
Writer Agent finalizes the itinerary in a clean format.

6. How to Run
Clone the repo
Install dependencies
Add your API keys inside an .env file
Run the notebook or integrate the agents in your own script

7. Output Example
A daily plan with top attractions
Restaurant suggestions
Neighborhood-wise breakdown
Time-wise schedule for each day
Travel tips + reasoning summaries

8. Future Improvements
Add cost estimation
Include live weather data
Add hotel recommendations
Build a small Streamlit UI
Support multi-country journeys

9. Acknowledgements
This project was created for my Applied GenAI course, where we explored multi-agent systems, RAG workflows, and real-world data integration.


