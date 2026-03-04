# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  Stats <|-- Test
  Test <|-- Phrase
  User <|-- History
  History o-- Stats
  
  class User{
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
  }
  class Stats{
        - accuracy: int
        - wpm: int
        + calcAccuracy( numCorrect: int, numIncorrect: int) int
        + calcSpeed( wordcount: int, time: int) int

  }
  
  class Phrase{
        - wordCount: int
        - vector<string> words
        
  }
  class Test{
        - numCorrect: int
        - numIncorrect: int
        - testTime: int
  }
  class History{
        - avgSpeed: int
        - avgAccuracy: int
  }
  
```
