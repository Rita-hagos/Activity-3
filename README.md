# Activity-3

Q1. Use Big O Notation to describe the time complexity of an algorithm that takes 4N + 16 steps.

4N + 16 = N bc by dropping constants, the numbers in this scneario don't matter so it will be 0(N)

Q2. Use Big O Notation to describe the time complexity of an algorithm that takes 2N² steps.

2N^2 = N^2

Q3. Use Big O Notation to describe the time complexity of this function (double_then_sum).
def double_then_sum(array) 
	doubled_array = []

	array.each do |number| 
		doubled_array << number *= 2
	end

	sum = 0

	doubled_array.each do |number| 
		sum += number
	end
	return sum 
end

Answer: the firsrt lopp eunce once for every element and inside its multipled by 2 before it gets pushed into array so the loop will result in =0(N)
Whileas the second loop also equals = 0(N) so total time: 0(N) + 0(N) = 0(2N)
but we will drop the constant resulting 0(N)

Q4. Use Big O Notation to describe the time complexity of this function
def multiple_cases(array) 
	array.each do |string|
		puts string.upcase 
		puts string.downcase 
		puts string.capitalize
	end 
end

Answer: Insdie each iteration there's 3 constant operations so 3 steps. T(N) = 3N.
3N = N. Final answer = 0(N)

Q5. The next function iterates over an array of numbers, and for each number whose index is even, it prints the sum of that number plus every number in the array. What is this function’s efficiency in terms of Big O Notation? 

def every_other(array) 
	array.each_with_index do |number, index|
		if index.even?
			array.each do |other_number|
            	puts number + other_number
			end 
		end
	end 
end

Answer: The total work is about 
N/2 * N = N^2/2
= 0(N^2)


