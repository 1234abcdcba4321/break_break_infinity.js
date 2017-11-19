	# break_break_infinity.js
	A replacement for break_infinity.js when 1e900719925470992 isn't enough.
	If you want to prioritize speed over massive numbers, please use break_infinity.js instead.
	
	https://github.com/1234abcdcba4321/break_break_infinity.js
	
	This library is open source and free to use/modify/fork for any purpose you want.
	
	By 1234abcdcba4321 (and 100% copied from patashu shh)
	
	---
	
	bigDecimal has only two fields:
	
	mantissa: A number (double) with absolute value between [1, 10) OR exactly 0. If mantissa is ever 10 or greater, it should be normalized (divide by 10 and add 1 to exponent until it is less than 10, or multiply by 10 and subtract 1 from exponent until it is 1 or greater). Infinity/-Infinity/NaN will cause bad things to happen.
	exponent: A bigInt.
	
	The decimal's value is simply mantissa*10^exponent.
	
	Functions of bigDecimal:
	
	fromMantissaExponent(mantissa, exponent)
	fromDecimal(value)
	fromNumber(value)
	fromString(value)
	fromValue(value)
	
	toNumber()
	mantissaWithDecimalPlaces(places)
	toString()
	toFixed(places)
	toExponential(places)
	
	abs(), neg(), sign()
	add(value), sub(value), mul(value), div(value), recip()
	
	cmp(value), eq(value), neq(value), lt(value), lte(value), gt(value), gte(value)
	cmp_tolerance(value, tolerance), eq_tolerance(value, tolerance), neq_tolerance(value, tolerance), lt_tolerance(value, tolerance), lte_tolerance(value, tolerance), gt_tolerance(value, tolerance), gte_tolerance(value, tolerance)
	
	log(base), log10(), log2(), ln()
	pow(value, other), pow(value), pow_base(value), exp(), sqr(), sqrt(), cube(), cbrt()	
