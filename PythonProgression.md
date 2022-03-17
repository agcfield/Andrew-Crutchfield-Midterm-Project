## Pages:

1. [Homepage](https://github.com/agcfield/Andrew-Crutchfield-Midterm-Project/blob/main/README.md)
2. [IT Professions](https://github.com/agcfield/Andrew-Crutchfield-Midterm-Project/blob/main/ITProfessions.md)
3. [Python Progression](https://github.com/agcfield/Andrew-Crutchfield-Midterm-Project/blob/main/PythonProgression.md)
4. [Movie Recommendations](https://github.com/agcfield/Andrew-Crutchfield-Midterm-Project/blob/main/MovieRecommendations.md)
5. [How to Tie a Shoe](https://github.com/agcfield/Andrew-Crutchfield-Midterm-Project/blob/main/HowToTieAShoe.md)

# Python Progression

Along with this class (INFOTC 1000), I am also simultaneously taking INFOTC 1040, in which I have developed a knowledge of Python that is far superior to my knowledge of JavaScript. The purpose of this page is to show how my skills with Python have developed overtime, by showing one of my first Python programs, and comparing it to my most recent one.

## Early Code

The following code calculates and prints to the user the volume of a cylinder after a height and radius are provided.

```
import math

def main():

    print("Hello! This program is used to calculate the volume of a cylinder.")
    
    do_calculation = True
    while (do_calculation):
        while True:
            try:
                cylinder_radius = float(input("Enter the radius of your cylinder: "))
                if (cylinder_radius < 0):
                    print("The value you enter cannot be negative. Please try again.")
                    continue
            except:
                print("The value you entered is invalid. Only numerical values are valid. Please try again.")
            else:
                break
                
        while True:
            try:
                cylinder_height = float(input("Enter the height of your cylinder: "))
                if (cylinder_height < 0):
                    print("The value you enter cannot be negative. Please try again.")
                    continue
                cylinder_volume = math.pi * cylinder_radius**2 * cylinder_height
                print("The volume of your cylinder is",cylinder_volume)
                another_calculation = input("That was fun. Would you like to perform another calculation? (y/n): ")
                if (another_calculation != "y"):
                    do_calculation = False
            except:
                print("The value you entered is invalid. Only numerical values are valid. Please try again.")
            else:
                break

main()
```

## Recent Code

The following code will open a file of numbers, and return various statistics regarding those numbers.

```
def main():

    evaluate_file = True
    while evaluate_file == True:

        numbers_file_name = input("Enter the name of the file containing the numbers you want to see stats about: ")

        try:
            numbers_file = open("%s.txt" % numbers_file_name,"r")
            print("File name: " , numbers_file_name)

            numbers_list = []
            sum_of_numbers = 0
            numbers_count = 0
            for number in numbers_file:
                sum_of_numbers += float(number)
                numbers_count += 1
                numbers_list.append(float(number.strip()))
            
            average_of_numbers = sum_of_numbers / numbers_count
            
            numbers_list.sort()

            maximum_number = numbers_list[-1]

            minimum_number = numbers_list[0]

            numbers_range = maximum_number - minimum_number

            print("Sum: ", sum_of_numbers)
            print("Count: ", numbers_count)
            print("Average: ", average_of_numbers)
            print("Maximum: ", maximum_number)
            print("Minimum: ", minimum_number)
            print("Range: ", numbers_range)

            numbers_file.close()

            evaluate_another_file = input("Would you like to evaluate another file? (y/n): ")
            if evaluate_another_file == "y":
                continue
            else:
                exit()
            
        except:
            print("The requested file could be opened because it was not found. Make sure the desired file exists before you enter its name and that the name you enter does not include a file extension.") 
            continue
    
main()
```
