# Mathematicial-Calculator
# Cone.\ Quadratic equation.\ Circle area and circumference.\ Simultaneous linear equation.

info = ('Program name: Mathematicial Calculator\n'
        'Authors: Dayo\n'
        'Date Created:27/3/2021')  # Programers details
print(info)

print()  # Print a new empty line

def main(): #This store all codes below the main variable in the main() variable
    import sys #This use to end a program 
    user = (input('Enter your name please:'))  # This will store the user input
    user = (str(user))
    if user.isalpha():
        print('Great job', user)  
    else:
        print()
        print('input incorrect')
        main()

    print()

    about = '''Welcome to the applicatin.
                    This app is an application that can be used to calculate four different equations
                    Each application are accurate and correct.
                    Enter 1 to acces Cone calculator application.
                    Enter 2 to acces Quadratic equation solving application.
                    Enter 3 to acces Circle area and circumference finding application.
                    Enter 4 to acces Simultaneous linear equation solving application.'''
    print (about)

    print()
    
    application='''Applications-:
                1 = Cone calculator application.
                2 = Quadratic equation solving application.
                3 = Circle area and circumference finding application.
                4 = Simultaneous linear equation solving application.''' # Application avaliable
    print(application)
    app_input=(input('What Application are you choosing: ')) # Print the appliction the user insert, user can copy and paste to make things easier
    if app_input ==  '1':
        cone()
        cone_ask()
    elif app_input == '2':
        Quadratic()
        Quadratic_ask()
    elif app_input == '3':
        Circle()
        Circle_ask()
    elif app_input == '4':
        Simultaneous()
        Simultaneous_ask()
    else:
        print('input incorrect') # If user input is incorrect, the program strat up again.
        main()    
    print()
def cone(): #This store all codes below the cone variable in the cone() variable
    import sys
    # Cone calculator application
    # Volume Of a Cone
    print('Volume Of a Cone Calculator')
    r = float(input('Enter radius number: ')) # Input is store as a float(decimal)
    h = float(input('Enter height number: ')) # input will be use with the formula below to solve the promblem
    volume = (3.14156 * r * r * h) / 3
    option = input('Do you want to round up your answer to the nearest number (Yes/Enter any key if No):')
    if option == 'Yes':
        print('The volume of the cone = ', int(volume)) # Print the answer to the nearest value  
    else:
        print('The volume of the cone = ', float(volume)) # Print the answer in decimal 
    print()
    # Surface Area Of a Cone
    print('Surface Area Of a Cone Calculator')
    r = float(input('Enter radius number: '))
    l = float(input('Enter lenght number: '))
    sa = (3.14156 * r * (l * r))
    option = input('Do you want to round up your answer to the nearest number (Yes/Enter any key if No):')
    if option == 'Yes':
        print('The Surface Area of the cone =', int(sa)) 
    else:
        print('The Surface Area of the cone =', float(sa))
    print()
    restart=(input('Do you wish to restart or exit or press any key to continue:'))
    while restart == 'restart':
        print()
        main()
    while restart == 'exit':
        print()
        print('You have exit out of the Application')
        sys.exit() # This ends the program if user enter exit 
    print()
def cone_ask(): # This created incase if the user enter a wrong input
    app_input=(input('What Application do you want next?:'))
    if app_input ==  '1':
        cone()
        cone_ask()
    elif app_input == '2':
        Quadratic()
        Quadratic_ask()
    elif app_input == '3':
        Circle()
        Circle_ask()
    elif app_input == '4':
        Simultaneous()
        Simultaneous_ask()
    else:
        print()
        print('input incorrect') # If user input is incorrect, question will be ask again.
        cone_ask()
    print()
def Quadratic():
    import sys
    # Quadratic equation solving application
    print('Quadratic equation Calculator')
    import cmath
    a = float(input('Enter a: ')) 
    b = float(input('Enter b: '))
    c = float(input('Enter c: '))
    d = (b ** 2) - (4 * a * c)
    ans1 = (-b + cmath.sqrt(d)) / (2 * a)
    ans2 = (-b - cmath.sqrt(d)) / (2 * a)
    print('The positive answer to the equation =', ans1)
    print('The negative answer to the equation =', ans2)
    print()
    restart=(input('Do you wish to restart or exit or press any key to continue:'))
    while restart == 'restart':
        print()
        main()
    while restart == 'exit':
        print()
        print('You have exit out of the Application')
        sys.exit()
    print()
def Quadratic_ask():
    app_input=(input('What Application do you want next?:'))
    if app_input ==  '1':
        cone()
        cone_ask()
    elif app_input == '2':
        Quadratic()
        Quadratic_ask()
    elif app_input == '3':
        Circle()
        Circle_ask()
    elif app_input == '4':
        Simultaneous()
        Simultaneous_ask()
    else:
        print()
        print('input incorrect') 
        Quadratic_ask()
    print()
def Circle():
    import sys
    # Circle, area and circumference finding application
    print('Circle area and circumference Calculator')
    r = float(input('Enter the radius of the circle:')) 
    a = 3.14 * r * r
    c = 2 * 3.14 * r
    option = input('Do you want to round up your answer to the nearest number (Yes/Enter any key if No):')
    if option == 'Yes':
        print('The Area of the circle =', int(a))
        print('The Circumfreence of the circle =', int(c)) 
    else:
        print('The Area of the circle =', float(a))
        print('The Circumfreence of the circle =', float(c)) 
    print()
    restart=(input('Do you wish to restart or exit or press any key to continue:'))
    while restart == 'restart':
        print()
        main()
    while restart == 'exit':
        print()
        print('You have exit out of the Application')
        sys.exit()
    print()
def Circle_ask():
    app_input=(input('What Application do you want next?:'))
    if app_input ==  '1':
        cone()
        cone_ask()
    elif app_input == '2':
        Quadratic()
        Quadratic_ask()
    elif app_input == '3':
        Circle()
        Circle_ask()
    elif app_input == '4':
        Simultaneous()
        Simultaneous_ask()
    else:
        print()
        print('input incorrect') 
        circle_ask()
    print()
def Simultaneous():
    import sys
    # Simultaneous Linear Equations Solving application
    print('Simultaneous Linear Equations Calculator\n'
          'Before you continue make sure you  have numpy function installed on your PC through your PC command prompt\n')
    import numpy as np #install numpy before use
    a_input = input('Enter the first number value at the top role of the equation:')
    b_input = input('Enter the second number value at the top role of the equation:')
    c_input = input('Enter the first number value at the buttom role of the equation:')
    d_input = input('Enter the second number value at the button role of the equation:')
    e_input = input('Enter the last  number value at the top role of the equation:')
    f_input = input('Enter the last number value at the bottom role of the equation:')
    a = float(a_input)
    b = float(b_input)
    c = float(c_input)
    d = float(d_input)
    e = float(e_input)
    f = float(f_input)
    x = np.array([[a,b], [c,d]])
    y = np.array([e,f])
    ans = np.linalg.solve(x,y)  # Linear Algebra
    print('Answer =')
    print(ans)
    print()
    restart=(input('Do you wish to restart or exit or press any key to continue:'))
    while restart == 'restart':
        print()
        main()
    while restart == 'exit':
        print()
        print('You have exit out of the Application')
        sys.exit()
    print()
def Simultaneous_ask():
    app_input=(input('What Application do you want next?:'))
    if app_input == 'Cone calculator application':
        cone()
        cone_ask()
    elif app_input == 'Quadratic equation solving application':
        Quadratic()
        Quadratic_ask()
    elif app_input == 'Circle area and circumference finding application':
        Circle()
        Circle_ask()
    elif app_input == 'Simultaneous linear equation solving application':
        Simultaneous()
        Simultaneous_ask()
    else:
        print()
        print('input incorrect') 
        Simultaneous_ask()
    print()

main()
