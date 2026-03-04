# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  Stats <-- Test
  Test <-- Phrase
  User 1--1 History
  History o-- Stats
  History o-- Test

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
        - string words
  }
  class Test{
        - numCorrect: int
        - numIncorrect: int
        - testTime: int
  }
  class History{
        - avgSpeed: int
        - avgAccuracy: int
        - vector<Test> tests 
        + calcAvgSpeed(vector<Test>: tests )
        + calcAvgAccuracy(vector<Test>: tests)
  }
  
```
