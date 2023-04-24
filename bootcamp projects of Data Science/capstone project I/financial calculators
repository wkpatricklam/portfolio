import math

# function to calculate simple interest
def simple_interest(principal, rate, time):
    return principal * (1 + rate * time)

# function to calculate compound interest
def compound_interest(principal, rate, time):
    return principal * math.pow((1 + rate), time)

# function to calculate monthly bond repayment
def bond_repayment(present_value, rate, months):
    monthly_rate = (rate / 100) / 12
    return (monthly_rate * present_value) / (1 - math.pow(1 + monthly_rate, -months))

# main program
print("Investment - to calculate the amount of interest you’ll earn on your investment")
print("Bond - to calculate the amount you’ll have to pay on a home loan")
choice = input("Enter either 'investment' or 'bond' from the menu above to proceed: ").lower()

if choice == "investment":
    principal = float(input("Enter the amount of money that you are depositing: "))
    rate = float(input("Enter the interest rate (as a percentage): ")) / 100
    time = float(input("Enter the number of years you plan on investing: "))
    interest = input("Do you want simple or compound interest? ").lower()
    if interest == "simple":
        total = simple_interest(principal, rate, time)
    elif interest == "compound":
        total = compound_interest(principal, rate, time)
    else:
        print("Invalid interest type entered!")
        exit()
    print(f"\nYour total amount after {time} years at {rate*100}% interest rate with {interest} interest is {total:.2f}")

elif choice == "bond":
    present_value = float(input("Enter the present value of the house: "))
    rate = float(input("Enter the interest rate: "))
    months = int(input("Enter the number of months you plan to take to repay the bond: "))
    repayment = bond_repayment(present_value, rate, months)
    print(f"\nYour monthly bond repayment is {repayment:.2f}")

else:
    print("Invalid choice entered!")
    exit()
