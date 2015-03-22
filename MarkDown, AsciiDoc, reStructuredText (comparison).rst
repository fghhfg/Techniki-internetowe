====================================
MarkDown, AsciiDoc, reStructuredText
====================================
----------
PORÓWNANIE
----------

+------------------------+------------------------------+---------------+---------------------+
| OPCJE                  | MarkDown                     | AsciiDoc      | reStructuredText    |
+========================+==============================+===============+=====================+
| Headers                | | # Header1                  | | Level1      | column 4            |
|                        | | ## Header2                 | | ---------   |                     |
|                        | | ### Header3                | | Text.       |                     |
|                        | | ### Header3                | | Level2      |                     |
|                        | | #### Header4               | | ~~~~~       |                     |
|                        | | ##### Header5              | | Level3      |                     |
|                        | | ###### Header6             | | ^^^^^^      |                     |
|                        | |                            |               |                     |
|                        | | Alternatywnie dla H1 i H2: |               |                     |
|                        | | Alt-H1                     |               |                     |
|                        | | =====                      |               |                     |
|                        | | Alt-H2                     |               |                     |
|                        | | ---------                  |               |                     |
+------------------------+------------------------------+---------------+---------------------+
| body row 2             | Cells may span columns.                                            |
+------------------------+------------------------------+-------------------------------------+
| body row 3             | Cells may                    | - Table cells                       |
+------------------------+ span rows.                   | - contain                           |
| body row 4             |                              | - body elements.                    |
+------------------------+------------------------------+-------------------------------------+

////

Some care must be taken with grid tables to avoid undesired interactions with cell text in rare cases. For example, the following table contains a cell in row 2 spanning from column 2 to column 4:

+--------------+----------+-----------+-----------+
| row 1, col 1 | column 2 | column 3  | column 4  |
+--------------+----------+-----------+-----------+
| row 2        |                                  |
+--------------+----------+-----------+-----------+
| row 3        |          |           |           |
+--------------+----------+-----------+-----------+

////

If a vertical bar is used in the text of that cell, it could have unintended effects if accidentally aligned with column boundaries:

+--------------+----------+-----------+-----------+
| row 1, col 1 | column 2 | column 3  | column 4  |
+--------------+----------+-----------+-----------+
| row 2        | Use the command ``ls | more``.   |
+--------------+----------+-----------+-----------+
| row 3        |          |           |           |
+--------------+----------+-----------+-----------+

////

Several solutions are possible. All that is needed is to break the continuity of the cell outline rectangle. One possibility is to shift the text by adding an extra space before:

+--------------+----------+-----------+-----------+
| row 1, col 1 | column 2 | column 3  | column 4  |
+--------------+----------+-----------+-----------+
| row 2        |  Use the command ``ls | more``.  |
+--------------+----------+-----------+-----------+
| row 3        |          |           |           |
+--------------+----------+-----------+-----------+

////

Another possibility is to add an extra line to row 2:

+--------------+----------+-----------+-----------+
| row 1, col 1 | column 2 | column 3  | column 4  |
+--------------+----------+-----------+-----------+
| row 2        | Use the command ``ls | more``.   |
|              |                                  |
+--------------+----------+-----------+-----------+
| row 3        |          |           |           |
+--------------+----------+-----------+-----------+

////

=====  =====  =======
  A      B    A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======

////

=====  =====  ======
   Inputs     Output
------------  ------
  A      B    A or B
=====  =====  ======
False  False  False
True   False  True
False  True   True
True   True   True
=====  =====  ======

////

=====  =====
col 1  col 2
=====  =====
1      Second column of row 1.
2      Second column of row 2.
       Second line of paragraph.
3      - Second column of row 3.

       - Second item in bullet
         list (row 3, column 2).
\      Row 4; column 1 will be empty.
=====  =====

