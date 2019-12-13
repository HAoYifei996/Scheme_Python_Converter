# Scheme-Python Code Converter

This is the document that record every change We've made to our scheme project code to implement this converter. The project is inspired by the scheme project from **CS 61A** at UC Berkeley.

## Get Started

Run ``scheme.py`` to get started. We will update README for any changes we have implemented. Beyond this, ``scheme.py`` perform as a Scheme interpreter.

Run ``(exit)`` to terminate the program.

## Scheme -> Python

1. **Builtins**

	For example, for plus operation in scheme, if we type in the following: 

	```
	(+ 1 2)
	```

	The output should be:

	```
	1 + 2
	```

	Now we still want it to compute the result, but output the code in Python order instead of output the result of computation like in the interpreter.

	*Modification*

	In ``BuiltinProcedure.apply``, we change the output in ``try``. Instead of ``return self.fn``, we still do the evaluation but return the expression in a different order.

	Builtins we've implemented in our code:
	
		* Arithmatic:
			= + - * / < > <= >= expt abs

		* Boolean Operation:
			boolean? not eq? null? even? odd?


