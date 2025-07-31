# Task 2 Solution

```python
# Movie Ratings Menu System
# This program allows a user to add movies with ratings, view them, and calculate an average rating.

# ------------------------
# FUNCTION DEFINITIONS
# ------------------------

def display_menu():
    """
    Display the menu options and return the user's choice as an integer.
    Validates that input is between 1 and 4.
    """
    print("\n--- Movie Ratings Menu ---")
    print("1. Add a new movie")
    print("2. List all movies and ratings")
    print("3. Show average rating")
    print("4. Exit")
    
    while True:
        try:
            choice = int(input("Enter your choice (1–4): "))
            if 1 <= choice <= 4:
                return choice
            else:
                print("Please enter a number between 1 and 4.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")

def add_movie(movies):
    """
    Prompt the user for a movie title and rating, and add it to the movies list.

    Parameters:
    - movies (list): The list of movie dictionaries.
    """
    title = input("Enter the movie title: ").strip()
    while True:
        try:
            rating = int(input("Enter the rating (1–5): "))
            if 1 <= rating <= 5:
                break
            else:
                print("Rating must be between 1 and 5.")
        except ValueError:
            print("Invalid input. Please enter an integer.")
    
    # Add the movie as a dictionary
    movies.append({"title": title, "rating": rating})
    print(f"Movie '{title}' added with rating {rating}.")

def list_movies(movies):
    """
    Print the list of movies and their ratings.

    Parameters:
    - movies (list): The list of movie dictionaries.
    """
    if not movies:
        print("No movies added yet.")
        return
    
    print("\n--- Movie List ---")
    for i, movie in enumerate(movies, start=

```
