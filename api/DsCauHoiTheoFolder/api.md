# Get list of single or parent question in folder

## Purpose

used to get the single question or question that contains child

``` gql
query AllFolders($condition: FolderCondition, $questionsByFolderIdCondition2: QuestionCondition) {
  allFolders(condition: $condition) {
    nodes {
      name
      des
      questionsByFolderId(condition: $questionsByFolderIdCondition2) {
        nodes {
           id
          questionId
          questionsByQuestionId {
            nodes {
              id
              questionId
            }
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
  "questionsByFolderIdCondition2": {
    "questionId": null
  }
}
```


