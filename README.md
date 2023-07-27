class Movie:
    def __init__(self, title, rating):
        self.title = title
        self.rating = rating

def get_average_rating(movies):
    total_ratings = sum(movie.rating for movie in movies)
    return total_ratings / len(movies)

def main():
    print("Welcome to the Simple Movie Dataset Analysis!")

    # Sample movie data
    movies = [
        Movie("The Shawshank Redemption", 9.3),
        Movie("The Godfather", 9.2),
        Movie("The Dark Knight", 9.0),
        Movie("Pulp Fiction", 8.9),
        Movie("Inception", 8.8),
    ]

    while True:
        print("\nMenu:")
        print("1. Display Movie Statistics")
        print("2. Display Average Movie Rating")
        print("3. Exit")

        choice = input("Enter your choice (1-3): ")

        if choice == '1':
            print("\nMovie Statistics:")
            for movie in movies:
                print(f"- {movie.title} (Rating: {movie.rating})")

        elif choice == '2':
            average_rating = get_average_rating(movies)
            print(f"\nAverage Movie Rating: {average_rating:.2f}")

        elif choice == '3':
            print("Exiting the Simple Movie Dataset Analysis...")
            break

        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
