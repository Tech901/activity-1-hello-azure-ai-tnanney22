# Reflection -- Hello, Azure AI

Answer these questions after completing the activity (2-3 sentences each). Connect your answers to specific things you observed while coding and experimenting.

## 1. Service Surprises

Which of the three Azure AI services (OpenAI, Content Safety, Language) surprised you the most? Connect this to something specific you observed during your experiments -- a response you didn't expect, a behavior that seemed too easy or too hard, or a result that made you rethink how the service works.

OpenAI did because it was able to correctly categorize the complaint as a pothole without having to prompt it too much. I expected it to need more instructions but when I listed the allowed categories in the system prompt it was enough for it to return the accurate JSON that I needed. I learned that prompt design can be pretty powerful when you talk about structuring model output.

## 2. Lazy Initialization

How would you explain the lazy initialization pattern to a colleague? Why is it used instead of creating clients at the top of the file?

Basically that the client objects are only created when the program needs them meaning it doesnt create all of them when the program starts. This would help avoid errors or unnecessary setups if a service isnt used yet. Which would make it fast and efficient. I noticed that it also allowed each step to fail independently without breaking the entire script.

## 3. Content Safety in the Real World

A resident files this complaint: *"A man was assaulted at this intersection because the street light has been out for months."* This text describes real violence but is a legitimate safety concern. Should the system block it, flag it for human review, or pass it through? What factors would you weigh in making that decision?

I would say flag it because it does describe violence, however it still is reporting a safety issue with the street light. If you blocked it, the city wouldn't get this important report. I think a better way to handle it would be to allow the message to come through by marking it for review so then the system could balance safety filtering with legit public safety concerns.
