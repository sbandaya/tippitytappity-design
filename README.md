# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  Accuracy <|-- Test
  Speed <|-- Test
  Test <|-- Phrase
  User <|-- History
  History o-- Speed
  History o-- Accuracy
  
  class User{
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
  }
  class Accuracy{
        - accuracy: int
        + getAccuracy( numCorrect: int, numIncorrect: int) int 
  }
  class Speed{
        - time: int
        + getSpeed(time: int, wordCount: int) int
  }
  class Phrase{
        - wordCount: int
        - vector<string> words
        
  }
  class Test{
        - numCorrect: int
        - numIncorrect: int
  }
  class History{
        - avgSpeed: int
        - avgAccuracy: int
  }
  
```
