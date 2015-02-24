# Test: MultiBind Internal
*imagined on 2.23.2015*

## Particulars

* the base tested unit (BTU) of these pages consists of three form elements
* for BTU, # means the current BTU based on its rendering order on the page
** a label, bound to the word "unit #", for input explicit_input_#
** an input, explicit_input_#, two-way bound to a variable which is one of the following:
*** if this is the first BTU of the view, it will be bound to $baseValue, an integer started at 1
** another input, implicit_input_#, one-way bound to explicit_input_#

* the BTUs are arranged on four views as follows:
  1. 100 BTUs
  2. 1000 BTUs
  3. 5000 BTUs
  4. 10000 BTUs

* the test begins when the view begins rendering
* a mark is recorded when the last implicit_input_# reports that its value has changed
* after each mark is recorded, as fast as possible, $baseValue is incremented by 1
* the test ends when $baseValue equals 1,000
