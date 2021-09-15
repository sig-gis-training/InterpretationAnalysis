Per-class Agreement
===================

1. Per-class agreement amongst interpreters should be analyzed and reported as follows:

+---------------------+---------------------------+-----------------------------+------------------------------+---------+
|                     | All interpreters agreeing | One interpreter disagreeing | Two interpreters disagreeing | etc.    |
+=====================+===========================+=============================+==============================+=========+
| Class 1 (reference) | Percent                   | Percent                     | Percent                      | Percent |
+---------------------+---------------------------+-----------------------------+------------------------------+---------+
| Class 2 (reference) | Percent                   | Percent                     | Percent                      | Percent |
+---------------------+---------------------------+-----------------------------+------------------------------+---------+
| Class 3 (reference) | Percent                   | Percent                     | Percent                      | Percent |
+---------------------+---------------------------+-----------------------------+------------------------------+---------+
| Total               | Percent                   | Percent                     | Percent                      | Percent |
+---------------------+---------------------------+-----------------------------+------------------------------+---------+

For this example, consider the following case:

+--------------+---------------+---------------+---------------+------------+
| Point number | Interpreter 1 | Interpreter 2 | Interpreter 3 | Reference  |
+==============+===============+===============+===============+============+
| 1            | Forest        | Forest        | Forest        | Forest     |
+--------------+---------------+---------------+---------------+------------+
| 2            | Forest        | Forest        | Non-forest    | Forest     |
+--------------+---------------+---------------+---------------+------------+
| 3            | Forest        | Non-forest    | Non-forest    | Non-forest |
+--------------+---------------+---------------+---------------+------------+
| 4            | Non-forest    | Non-forest    | Non-forest    | Non-forest |
+--------------+---------------+---------------+---------------+------------+
| 5            | Non-forest    | Forest        | Forest        | Forest     |
+--------------+---------------+---------------+---------------+------------+
| 6            | Forest        | Forest        | Non-forest    | Forest     |
+--------------+---------------+---------------+---------------+------------+
| 7            | Non-forest    | Non-forest    | Non-forest    | Non-forest |
+--------------+---------------+---------------+---------------+------------+
| 8            | Non-forest    | Non-forest    | Non-forest    | Non-forest |
+--------------+---------------+---------------+---------------+------------+
| 9            | Non-forest    | Forest        | Non-forest    | Forest     |
+--------------+---------------+---------------+---------------+------------+
| 10           | Forest        | Forest        | Forest        | Forest     |
+--------------+---------------+---------------+---------------+------------+

2. One way to calculate the agreement between interpreters is to count if the references match what the interpreters report. This can done in Excel by:

   a. Add columns next to the test case for *All interpreters agreeing, One interpreter disagreeing, & Two interpreters disagreeing*
   b. Paste the formula below

::

   All interpreters agreeing =IF(COUNTIF(B2:D2,E2)=3,1,0)
   One interpreter disagreeing =IF(COUNTIF(B2:D2,E2)=2,1,0)
   Two interpreters disagreeing =IF(COUNTIF(B2:D2,E2)=1,1,0)

.. Note ::
   The COUNTIF function counts the number of times a range equals a value. In this case our range is the interpreters classification, and our matching value is the reference column. 