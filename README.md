product_dictionary ={
                     1:["coke",30,40],
                     2:["pepsi",30,40], 
                     3:["maza",40,50],
                     4:["sprite",30,30], 
                     5:["up",30, 20],
                     6:["Lays",10, 10],
                     7:["dorritos",15,20] 
                     }

data_base2 = {1234 : [1]}  #id pass



option1 = int(input("type 1 for customer, or type 2 for the owner"))
        
if option1 == 1 :
    print(product_dictionary)
elif option1 == 2:
    user = int(input("Enter id : "))
    password = int(input("Enter pass : "))

    if user in data_base2.keys():  #user = 1234. database[1234]
        if data_base2[user][0] == password:
            print("Valid User")
        else:
            print("Wrong Password")
            pass;
    else:
        print("User is not in Database")
        pass;

i = 0

while True :
    print("product list")
    print("Num :product,Qty,cost")

    for x,y in product_dictionary.items():
        print(f"{x} : {y[0]},{y[1]},{y[2]}")

    product = int(input("Enter the product Numb : "))
    quantity = int(input("Enter the quantity : "))

    i = i + (product_dictionary[product][2] * quantity)

    print("Your Bill : ",i)

    final = int(input("payment method type 1 for cash type 2 for card"))
    if final == 1:
        print("thank you for cash payment - collect your recipt")
        pass;
    elif final == 2:
        print("thank you for card payment - collect your recipt")
    else :
        pass

    option5 = int(input("kindly give feedback 1 to 5"))

    print(option5)

    option = input("DO you wish to continue ? ")
    if option == "yes":
        continue;
    elif option == "no":
        break;
    else:
        print("Please type either 'yes' or 'no'")
