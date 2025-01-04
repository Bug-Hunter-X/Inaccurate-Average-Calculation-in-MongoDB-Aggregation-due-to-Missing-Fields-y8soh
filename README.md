# MongoDB Aggregation Bug: Handling Missing Fields in $avg

This repository demonstrates a common error in MongoDB aggregation pipelines when dealing with missing fields. The `$avg` operator can produce unexpected results if the documents being processed lack the field specified for averaging.

The `bug.js` file shows an aggregation pipeline that attempts to calculate the average age of users, but it fails to correctly handle users without an `age` field. The `bugSolution.js` file provides a corrected version using the `$ifNull` operator to handle missing values gracefully.

## How to Reproduce

1.  Clone this repository.
2.  Connect to your MongoDB instance.
3.  Create a collection named 'users' with some documents, including some without an `age` field.
4.  Run the code in `bug.js` and observe the incorrect results.
5.  Run the code in `bugSolution.js` to see the correct results.
