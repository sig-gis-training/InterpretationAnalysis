Interpreter agreement
=====================

Part 1. Calculating agreement between interpreters
-----------------------------------------------------------

Quality control refers to the quality of interpretation through cross-validation based on a set of samples that were assessed by two or more interpreters. These checks can be conducted in CEO by creating multiple projects with the same sample plots. Multiple interpreters can each complete one of these projects, allowing for comparison.

1. Establish a reference interpretation for each of the cross-validation sample units.

  a. Choose a reference interpretation--this should be one of the interpreter’s class assignments.
  b. This reference interpretation will be the basis for establishing the performance of individual interpreters.

2. Calculate agreement for each interpreter based on the reference interpretation. For each pair of interpreters, create a confusion matrix and include it in your project documentation.

+------------------------+-------------------------+------------------------+------------------------+
|                        | Class 1 (reference)     | Class 2 (reference)    | Class k (reference)    |
+========================+=========================+========================+========================+
| Class 1 (interpreter)  | Counts of sample points |Counts of sample points |Counts of sample points |
+------------------------+-------------------------+------------------------+------------------------+
| Class 2 (interpreter)  | Counts of sample points |Counts of sample points |Counts of sample points |
+------------------------+-------------------------+------------------------+------------------------+
| Class k (interpreter)  | Counts of sample points |Counts of sample points |Counts of sample points |
+------------------------+-------------------------+------------------------+------------------------+

3. To work an example, pretend that you and another interpreter have both collected data on a set of sample units on this Amazon land cover classification. Here are the results:

+--------------+------------------------------+------------+
| Point number | Interpreter 1 (Interpreter)  | Reference  |
+==============+==============================+============+
| 1            | Forest                       | Forest     |
+--------------+------------------------------+------------+
| 2            | Forest                       | Forest     |
+--------------+------------------------------+------------+
| 3            | Forest                       | Non-forest |
+--------------+------------------------------+------------+
| 4            | Non-forest                   | Non-forest |
+--------------+------------------------------+------------+
| 5            | Non-forest                   | Forest     |
+--------------+------------------------------+------------+
| 6            | Forest                       | Forest     |
+--------------+------------------------------+------------+
| 7            | Non-forest                   | Non-forest |
+--------------+------------------------------+------------+
| 8            | Non-forest                   | Non-forest |
+--------------+------------------------------+------------+
| 9            | Non-forest                   | Forest     |
+--------------+------------------------------+------------+
| 10           | Forest                       | Forest     |
+--------------+------------------------------+------------+

4. Calculate the confusion matrix below:

+--------------------------+-------------------+------------------------+
|                          |Forest (reference) | Non-forest (reference) |
+==========================+===================+========================+
| Forest (interpreter)     |                   |                        |
+--------------------------+-------------------+------------------------+
| Non-forest (interpreter) |                   |                        |
+--------------------------+-------------------+------------------------+

5. Based on the confusion matrices, for each interpreter, overall agreement with the reference is to be calculated as follows:

   Agreement between interpreter and the majority = Sum of counts in all the diagonal cells / Sum of all counts

6. The overall agreement per interpreter can be reported as below:

+---------------+----------------------------------------------------------------+
| Interpreter   | Overall agreement                                              |
+===============+================================================================+
| Interpreter 1 | Sum of counts in all of the diagonal cells/ Sum of all counts  |
+---------------+----------------------------------------------------------------+
| Interpreter 2 | Sum of counts in all of the diagonal cells/ Sum of all counts  |
+---------------+----------------------------------------------------------------+
| Interpreter n | Sum of counts in all of the diagonal cells/ Sum of all counts  |
+---------------+----------------------------------------------------------------+

7. Completed example:

.. csv-table:: Interpreter data
   :file: tables\ex-1-agreement-table-filled.csv

.. csv-table:: Confusion matrix of interpreters and reference
   :file: tables/ex-1-confusion-matrix-filled.csv
   :header-rows: 1

.. csv-table:: Overall agreement between interpreters
   :file: tables\ex-1-overall-agreement-filled.csv

