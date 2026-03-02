# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  User <|-- Accuracy
  User <|-- Speed
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
        
  }
  class Speed{
        - time: int
  }
  class Word{

  }
  class Phrase{
    
  }
  class History{

  }
```
