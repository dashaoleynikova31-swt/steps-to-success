# steps-to-success
next step to goal (I'm learning PYTHON!)







moods = []

while True:
    print("\nMood Journal")
    print("1 - Add a new mood")
    print("2 - Show all moods")
    print("3 - Delete a mood")
    print("4 - Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        mood = input("Enter your mood: ")
        moods.append(mood)
        print("Mood added successfully!")

    elif choice == "2":
        if not moods:
            print("No moods yet.")
        else:
            print("Your moods:")
            for i, mood in enumerate(moods, start=1):
                print(f"{i}. {mood}")

    elif choice == "3":
        if not moods:
            print("No moods to delete.")
        else:
            print("Choose a mood to delete:")
            for i, mood in enumerate(moods, start=1):
                print(f"{i}. {mood}")
    
            try:
                number = int(input("Enter the number: "))
    
                if 1 <= number <= len(moods):
                    confirm = input("Are you sure? (yes/no): ").lower()
                    if confirm == "yes":
                        removed = moods.pop(number - 1)
                        print(f"Mood '{removed}' removed successfully!")
                    else:
                        print("Deletion canceled.")
                else:
                    print("Invalid number.")
    
            except ValueError:
                print("Please enter a number.")
                
    elif choice == "4":
        q = input("Do you want to leave this app? (yes/no): ").lower()
        if q == "yes":
            print("Bye! Come back soon, mate!")
            break
        else:
            print("OK! Let's continue!")
            continue
