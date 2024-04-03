First, we import the necessary System namespace for Console.Write, Console.ReadLine, and Convert.ToDouble methods.
We declare the DiscountCoverage class with the Main method, which is the entry point for the console application.
Within the Main method, we declare the necessary variables:
input is a string variable used to store the user's input.
isMember and isPremiumMember are boolean variables to store whether the user is a regular member and a premium member, respectively.
totalSum and discount are double variables to store the total price and the discount value.
We then ask the user if they are a customer with Console.Write and store the input in the input variable. We use Trim() to remove any extra whitespace and ToLower() to convert the input to lowercase for easier comparison. We then check if the user entered "j" using isMember = input == "j".
We set the totalSum to 0 and discount to 0. We also initialize the isPremiumMember to false.
If the user is a member, we ask if they are a premium member and store the input in the input variable. We then check if the user entered "j" using isPremiumMember = input == "j".
We ask for the total price and store the input in the input variable. We then convert the input to a double using Convert.ToDouble and store it in the totalSum variable.
We set the discount value based on whether the user is a member and if they are a premium member. If the user is not a member, the discount is 0 or 2%, depending on the total price. If the user is a member, the discount is 5% or 10%, depending on whether they are a premium member.
We then set the memberType based on the user's membership status. We use the ternary operator to simplify the string concatenation.
Finally, we print the result to the console using Console.WriteLine with string interpolation. We include the member type, the discount value, and the total price.