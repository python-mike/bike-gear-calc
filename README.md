# bike-gear-calc
operation = input("Select language e-English, u-Ukraine")
if operation == "e":
    result = b = float(input('Rear sprocket:')) 
    a = float(input("Front sprocket:"))
    d = float(input("Diameter of wheel:"))
    l = float(input("Circumference, mm:"))
    k = float(input('Cadence,rpm:'))
    operation = input("Calculate diameter or circumference d/c?")
    result = None

    if operation == "c":
        result = round(0.00006 * k * l * (a / b), 1) 
    elif operation == "d":
        result = round(0.00006 * k * (3.141592 * d) * (a / b), 1)
    else:
        print("Unsupported select")
    if result is not None:
        if result > float(100):
            print('You are really fast!!!')
        print("Speed, km/h:", result)
elif operation == "u":
    result = b = float(input('Задня зірка:'))
    a = float(input("Передня зірка:"))
    d = float(input("Повний діаметр колеса:"))
    l = float(input("Довжина окружності, мм:"))
    k = float(input('Каденція,об/хв:'))
    operation = input("Розрахувати діаметр (d), чи довжину окружності(с): d/c?")
    result = None

    if operation == "c":
        result = round(0.00006 * k * l * (a / b), 1)
    elif operation == "d":
        result = round(0.00006 * k * (3.141592 * d) * (a / b), 1)
    else:
        print("Невірне введення")
    if result > float(100):
        print('Тут вже шолом не допоможе')
    if result is not None:
        print("Швидкість, км/год:", result)

