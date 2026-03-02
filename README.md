# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  Test <|-- Accuracy
  Test <|-- Speed
  Test <|-- Phrase
  User <|-- History
  History o-- Test
  Phrase o-- Word
  
  class User{
        - name: string
        - email: string
        - password: string
        - accuracy: int
        - speed: int
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
  class Word{
        - word: string
        - numCharacters: int 
  }
  class Phrase{
        - wordCount: int
        - vectpr<string> words
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
