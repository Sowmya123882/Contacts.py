# Contacts.py
contacts = {}

while True:
    print("\n1. Add Contact")
    print("2. View Contacts")
    print("3. Search Contact")
    print("4. Delete Contact")
    print("5. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        name = input("Enter name: ")
        number = input("Enter phone number: ")
        contacts[name] = number
        print("Contact added!")

    elif choice == "2":
        print("\nContacts List:")
        for name, number in contacts.items():
            print(name, ":", number)

    elif choice == "3":
        search = input("Enter name to search: ")
        if search in contacts:
            print(search, ":", contacts[search])
        else:
            print("Contact not found!")

    elif choice == "4":
        delete = input("Enter name to delete: ")
        if delete in contacts:
            del contacts[delete]
            print("Contact deleted!")
        else:
            print("Contact not found!")

    elif choice == "5":
        print("Goodbye!")
        break

    else:
        print("Invalid choice!")
