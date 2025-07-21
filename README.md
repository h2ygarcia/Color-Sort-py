import random

def color_sorting_game():
    colors = ['Red', 'Blue', 'Green', 'Yellow', 'Orange', 'Purple']
    # Avoiding repeating colors by using random.sample which takes
    # unique randomized colors up to the size of the colors array
    items = random.sample(colors, 6)
    print("Welcome to the Color Sorting Game!")
    print("Here are your colors:")
    print(items)

    print("\nType the items in order, sorted by color name (A-Z), separated by commas.")
    user_input = input("Your sorted list: ")
    user_sorted = [color.strip().capitalize() for color in user_input.split(',')]

    correct_sorted = sorted(items)
    print(f"\nCorrect sorted order: {correct_sorted}")

    if user_sorted == correct_sorted:
        print("Congratulations! You sorted the colors correctly!")
    else:
        print("Oops! That's not correct.")
        print(f"Your answer: {user_sorted}")

if __name__ == "__main__":
    color_sorting_game()
