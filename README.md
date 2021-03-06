# Qualean
- Inspired by Boolean + Quantum concepts. 
- We can assign it only 3 possible real states. True, False, and Maybe (1, 0, -1).
- But it internally picks an imaginary state, an imaginary number random.uniform(-1, 1).
- It multiplies real number with imaginary number and stores that 'magic' number internally after using Bankers rounding to 10th decimal place.

## Functions
- __add__(self, value)
	- It will add a qualean to another qualean.
	- It also supports addition of qualean to another data type like int, float or decimal
- __and__(self, value)
	- Checks wether both are qualean data types and both are not zero
- __or__(self, value)
	- Checks wether one of the two are qualean data types and not zero
- __bool__(self)
	- Converts the qualean to bool
	- False is qualean is 0 else True
- __eq__(self, value)
	- Checks if value of the qualean object is equal to value
	- value can be int, float, bool or decimal
- __float__(self)
	- Converts qualean to float
	- example, type (float (qualean (1))) = 'float'
- __ge__(self, value)
	- Return self>=value.
- __gt__(self, value)
	- Return self>value.
- __invert__(self)
	- Return (-1) * self
- __le__(self, value)
	- Return self<=value.
- __lt__(self, value)
	- Return self<value.
- __mul__(self, value)
	- Return self * value
- __repr__(self)
	- Return repr(self).
- __sqrt__(self)
	- Return math.sqrt (self)
- __str__(self)
	- Return str(self).
- magic_number(self)
	- It multiplies the real with imaginary number.
	- It uses python math.round function which internally uses banker's algorithm for rounding.

## Data descriptors
- imag
	- The randomly generated imaginary number
- qual
	- The qualean number
- real
	- The real number as per input

## Tests
- test_qualean_values
	- This will test if the class throws ValueError if number other than -1, 0 or 1 is given.
- test_bankers_rounding
	- Test if the final number has 10 decimal places
- test_float_conversion
	- Test if qualean data type is successfully converted to float
- test_n_times_addition
	- q + q + q ... 100 times = 100 * q
- test_sqrt_func
	- q.__sqrt__() = Decimal(q).sqrt ()
- test_one_million_qs_add
	- sum of 1 million different qs is very close to zero
- test_one_million_qs_mul
	- multiplication of 1 million different qs is very close to zero
- test_bool_False
	- qualean (0) should be False
- test_bool_True
	- qualean (-1) should be True
- test_and_False
	- q1 and q2 returns False when q2 is not defined as well and q1 is False
- test_and_True
	- q1 and q2 returns True when q1 and q2 is defined and q1 and q2 both are True
- test_or_True
	- q1 or q2 returns True when q1 and q2 are defined and q1 and q2 are not false
- test_or_True
	- q1 or q2 returns True when q1 is not defined as well and q2 is not false
- test_or_False
	- q1 is False and q2 not defined should return True
- test_invert
	- q + (~q) == 0
- test_repr
	- r.__repr__() == f'{num}'
- test_str
	- r.__str__() == f'{num}'
- test_eq
	- q == q should return True
- test_ge
	- test greater/less than equal to (<=, >=)
- test_lt
	- test less/greater than (<,>)
- test_readme_exists
	- readme exists
- test_readme_contents
	- readme contains more than 100 words
- test_readme_proper_description
	- all functions definition are present
- test_readme_file_for_formatting
	- Readme file formatting
- test_fourspace
	- test PEP8 guidelines for indentation
- test_function_name_had_cap_letter
	- function should not have capital letters
