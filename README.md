# School-Fees-Management-System
print("...... Welcome to School Fees System ......")
students = {
    "Trupti": {"total": 35000, "paid": 10000},
    "Rishikesh":   {"total": 35000, "paid": 15000},
    "Bhavesh":  {"total": 35000, "paid": 12000},
    "Kunal":   {"total": 35000, "paid": 20000},
    "Pooja":  {"total": 35000, "paid": 18000}
        }

while True:
    print("\n....... Students Details.....")
    print("1. Check Total Fees")
    print("2. Check Paid Fees")
    print("3. Check Pending Fees")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice in ["1", "2", "3"]:
     name = input("Enter student name (Trupti,Rishikesh,Bhavesh,Kunal,Pooja): ")
     if name in students:
            total = students[name]["total"]
            paid = students[name]["paid"]
            pending = total - paid

            if choice == "1":
                print(f"Total Fees of {name}: Rs.{total}")
            elif choice == "2":
                print(f"Paid Fees of {name}: Rs.{paid}")
            elif choice == "3":
                print(f"Pending Fees of {name}: Rs.{pending}")
     else:
            print("Student not found!")

    elif choice == "4":
        print("Thank you....!")
        break

    else:
        print("Invalid choice! Please try again.")
