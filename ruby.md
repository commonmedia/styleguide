# Developing Rails applications

## Coding Style
* Use soft-tabs with a two space indent.

* Never leave trailing whitespace.

* Use spaces around operators, after commas, colons and semicolons, around { and before }.
  ```Ruby
  sum = 1 + 2
  a, b = 1, 2
  1 > 2 ? true : false; puts 'Hi'
  [1, 2, 3].each { |e| puts e }
  ```

* No spaces after (, [ or before ], ).
  ```Ruby
  some(arg).other
  [1, 2, 3].length
  ```

* Use empty lines between defs and to break up a method into logical paragraphs.
  ```Ruby
  def some_method
    data = initialize(options)
    data.manipulate!
    data.result
  end
  
  def some_method
    result
  end
  ```

* Use def with parentheses when there are arguments. Omit the parentheses when the method doesn't accept any arguments.
  ```Ruby
  def some_method
   # body omitted
  end

  def some_method_with_arguments(arg1, arg2)
   # body omitted
  end
  ```

* Never use then for multi-line if/unless.
  ```Ruby
  # bad
  if some_condition then
    # body omitted
  end

  # good
  if some_condition
    # body omitted
  end
  ```

* Do not use the `and` and `or` keywords. Always use `&&` and `||` instead.

* Favor modifier if/unless usage when you have a single-line body.
  ```Ruby
  # bad
  if some_condition
    do_something
  end

  # good
  do_something if some_condition
  ```

* Never use unless with else. Rewrite these with the positive case first.
  ```Ruby
  # bad
  unless success?
    puts 'failure'
  else
    puts 'success'
  end

  # good
  if success?
    puts 'success'
  else
    puts 'failure'
  end
  ```

* Never put a space between a method name and the opening parenthesis.
  ```Ruby
  # bad
  f (3 + 2) + 1

  # good
  f(3 + 2) + 1
  ```
  