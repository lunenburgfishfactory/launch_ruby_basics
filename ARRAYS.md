# 1 In the code below, an array containing different types of pets is assigned to pets.

pets = ['cat', 'dog', 'fish', 'lizard']
Select 'fish' from pets, assign the return value to a variable named my_pet, then print the value of my_pet.

Expected output:

I have a pet fish!
------------------------------
pets = ['cat', 'dog', 'fish', 'lizard']
my_pet = nil
pets.select do |pet|
  my_pet = pet if pet.include?('fish')
end

#my_pet = pets[2] (how to select using index number)

puts "I have a pet #{my_pet}!"

# 2 Select 'fish' and 'lizard' from pets at the same time, assign the return value to a variable named my_pets, then print the value of my_pets.

pets = ['cat', 'dog', 'fish', 'lizard']
my_pet = []
pets.select do |pet|
  if pet.include?('fish')
  my_pet << pet
  elsif pet.include?('lizard')
  my_pet << pet
  end
end

puts "I have a pet #{my_pet[0]} and a pet #{my_pet[1]}!"

-LS solution
my_pets = pets[2..3]

puts "I have a pet #{my_pets[0]} and a pet #{my_pets[1]}!"

# 3 Remove 'lizard' from my_pet then print the value of my_pets.

my_pet.pop

puts "I have a pet #{my_pet[0]}!"

# 4 Using the code below, select 'dog' from pets, add the return value to my_pets, then print the value of my_pets.
pets = ['cat', 'dog', 'fish', 'lizard']
my_pet.push(pets[1])
puts "I have a pet #{my_pet[0]} and a pet #{my_pet[1]}!"

# 5 In the code below, an array containing different types of colors is assigned to colors.

colors = ['red', 'yellow', 'purple', 'green']
Use Array#each to iterate over colors and print each element.

colors.each do |color|
  puts "I'm the color #{color}!"
end

# 6 In the code below, an array containing the numbers 1 through 5 is assigned to numbers.

Use Array#map to iterate over numbers and return a new array with each number doubled. Assign the returned array to a variable named doubled_numbers and print its value using #p.

numbers = [1, 2, 3, 4, 5]
doubled_numbers = numbers.map { |number| number * 2 }  

# 7 In the code below, an array containing five numbers is assigned to numbers.

Use Array#select to iterate over numbers and return a new array that contains only numbers divisible by three. Assign the returned array to a variable named divisible_by_three and print its value using #p.

numbers = [5, 9, 21, 26, 39]
divisible_by_three = numbers.select do |number|
  number % 3 == 0
end

p divisible_by_three

# 8 The following array contains three names and numbers. Group each name with the number following it by placing the pair in their own array. Then create a nested array containing all three groups. What does this look like? (You don't need to write any code here. Just alter the value shown so it meets the exercise requirements.)

['Dave', 7, 'Miranda', 3, 'Jason', 11]

[['Dave, 7],['Miranda', 3],['Jason', 11]]

# 9 In the code below, a nested array containing three groups of names and numbers is assigned to favorites.

Use Array#flatten to flatten favorites so that it's no longer a nested array. Then assign the flattened array to a variable named flat_favorites and print its value using #p.

favorites = [['Dave', 7], ['Miranda', 3], ['Jason', 11]]
flat_favorites = favorites.flatten
 p flat_favorites 

# 10 In the code below, two arrays containing several numbers are assigned to two variables, array1 and array2.

array1 = [1, 5, 9]
array2 = [1, 9, 5]
Compare array1 and array2 and print true or false based on whether they match.

puts array1 == array2