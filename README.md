
while True:

    print("\n===== Shape Menu =====")
    print("1. Square")
    print("2. Triangle")
    print("3. Reverse Triangle")
    print("4. Diamond")
    print("5. Heart")
    print("0. Exit")

    choice = int(input("Enter your choice: "))

    if choice == 1:
        for raw in range(5):
            for col in range(5):
                if raw >= 0:
                    print("*", end=" ")
                else:
                    print(" ", end=" ")
            print()

    elif choice == 2:
        for raw in range(5):
            for col in range(5):
                if col <= raw:
                    print("*", end=" ")
                else:
                    print(" ", end=" ")
            print()

    elif choice == 3:
        for raw in range(5):
            for col in range(5):
                if col >= raw:
                    print("*", end=" ")
                else:
                    print(" ", end=" ")
            print()

    elif choice == 4:
        for raw in range(9):
            for col in range(9):
                if abs(raw - 4) + abs(col - 4) <= 4:
                    print("*", end=" ")
                else:
                    print(" ", end=" ")
            print()

    elif choice == 5:
        for raw in range(6):
            for col in range(7):
                if ((raw == 0 and col % 3 != 0) or
                    (raw == 1 and col % 3 == 0) or
                    (raw - col == 2) or
                    (raw + col == 8)):
                    print("*", end=" ")
                else:
                    print(" ", end=" ")
            print()

    elif choice == 0:
        print("Program finished!")
        break

    else:
        print("Wrong number! Try again.")
