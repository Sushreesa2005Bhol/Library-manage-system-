# Library-manage-system-

books = []

def add_book():
    book = input("Enter book name: ")
    books.append({"name": book, "issued": False})
    print("Book added successfully!")

def search_book():
    name = input("Enter book name to search: ").lower()

    for book in books:
        if book["name"].lower() == name:
            print("Book found:", book["name"])
            print("Status:", "Issued" if book["issued"] else "Available")
            return

    print("Book not found!")

def show_books():
    for book in books:
        print(book["name"], "-", 
              "Issued" if book["issued"] else "Available")

while True:
    print("\n1. Add Book")
    print("2. Search Book")
    print("3. Show All Books")
    print("4. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        add_book()
    elif choice == "2":
        search_book()
    elif choice == "3":
        show_books()
    elif choice == "4":
        break
    else:
        print("Invalid choice!")
        
