# Get list of single or parent question in a set

## Purpose

used to get the single question or question that contains child

``` gql
query AllSets($condition: SetCondition) {
  allSets(condition: $condition) {
    nodes {
      id
      setOfQuestionsBySetId {
        nodes {
          questionByQuestionId {
            id
            questionId
            content
            questionsByQuestionId {
              nodes {
                id
                questionId
                content
                answersData
                correctAnswer
              }
            }
            answersData
            correctAnswer
          }
        }
      }
    }
  }
}
```

## Input

``` json
{
  "condition": {
    "id": 1
      },

}
```
