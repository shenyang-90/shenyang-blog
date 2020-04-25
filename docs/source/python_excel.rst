
Excel
=====

http://www.python-excel.org/

https://xlrd.readthedocs.io/en/latest/api.html


.. code:: python

   import xlrd

   data = xlrd.open_workbook('excel.xls')

   table = data.sheets()[0]
   table = data.sheet_by_index(0)
   table = data.sheet_by_name(u'Sheet1')

   table.row_values(i)
   table.col_values(i)

   table.nrows
   table.ncols

   table.cell(0,0).value
   table.cell(2,3).value

   table.cell(2,3).ctype
   ctype : 0 empty,1 string, 2 number, 3 date, 4 boolean, 5 error

   table.merged_cells

