# Post Evaluation

### API Endpoint
- **Endpoint**: POST `/Provider/Evaluations/PostEvaluation`

### Request Body
```json
{
  "evaluation_id": 0,
  "request_id": 0,
  "answers": [
    {
      "question_id": 0,
      "anwser_rate": 0
    }
  ],
  "note": "string"
}
```

- **evaluation_id**: Integer, comes from order details api.
- **request_id**: Integer, required (ID of the request being evaluated).
- **answers**: Array of objects containing:
  - **question_id**: Integer, required (ID of the evaluation question).
  - **anwser_rate**: Integer, required (rating for the question).

- **note**: String, optional (additional notes or comments).

### Response Example

- **status**: Boolean, indicates if the operation was successful.
- **message**: String, a message indicating the result of the operation.
- **error**: String, empty if no error occurred.
- **Data**: Null, no additional data returned upon success.
```json
{
  "status": true,
  "message": "تمت المهمه بنجاح",
  "error": "",
  "Data": null
}
```



