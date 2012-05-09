# Developing Rails applications

## Coding Style
* Use soft-tabs with a two space indent.
* Never leave trailing whitespace.
* Use spaces around operators, after commas, colons and semicolons, around { and before }.
  ```
  sum = 1 + 2
  a, b = 1, 2
  1 > 2 ? true : false; puts 'Hi'
  [1, 2, 3].each { |e| puts e }
  ```

* No spaces after (, [ or before ], ).
  ```
  some(arg).other
  [1, 2, 3].length
  ```

* Use empty lines between defs and to break up a method into logical paragraphs.

  ```
  def some_method
    data = initialize(options)
    data.manipulate!
    data.result
  end
  
  def some_method
    result
  end
  ```
