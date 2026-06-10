# College Predictor System Diagrams

## ER Diagram

```text
+------------+
|   Student  |
+------------+
| Student_ID |
| Name       |
| Email      |
| Score      |
| Category   |
| Branch     |
+------------+
      |
      | Applies For
      v
+------------+
| Prediction |
+------------+
| Predict_ID |
| Student_ID |
| College_ID |
| Probability|
+------------+
      |
      | Refers To
      v
+------------+
|  College   |
+------------+
| College_ID |
| Name       |
| Location   |
| Ranking    |
| Seats      |
+------------+
      |
      | Contains
      v
+------------+
|   Cutoff   |
+------------+
| Cutoff_ID  |
| College_ID |
| Branch     |
| Category   |
| CutoffMark |
+------------+
```

## Use Case Diagram

```text
                 +------------------+
                 |      Student     |
                 +------------------+
                          |
        -----------------------------------------
        |            |            |             |
        v            v            v             v
   (Register)    (Login)   (Enter Score)  (View Colleges)
                                          |
                                          v
                                  (Get Prediction)

                 +------------------+
                 |      Admin       |
                 +------------------+
                          |
        -----------------------------------------
        |                    |                 |
        v                    v                 v
 (Manage Colleges)   (Update Cutoffs)   (Generate Reports)
```
