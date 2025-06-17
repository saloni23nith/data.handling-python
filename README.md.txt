OMDb and Dad Jokes Mashup
This project is a fun Python application that combines movie data from the OMDb API with dad jokes from the icanhazdadjoke API. For a given movie title, the app analyzes the plot, finds a keyword, and serves up relevant dad jokes using that keyword — all with a bit of snark depending on the Rotten Tomatoes rating.

 Features
Fetches movie details from the OMDb API

Extracts Rotten Tomatoes ratings

Identifies the longest plot keyword with matching dad jokes

Pulls up to two relevant dad jokes using icanhazdadjoke.com

Outputs a humorous mashup that varies based on movie quality


How It Works
The user inputs a movie title.

The app:

Fetches movie data and plot summary via the OMDb API.

Extracts a long keyword from the plot that has matching jokes.

Queries icanhazdadjoke for jokes using that keyword.

The result:

Movie title and Rotten Tomatoes rating

Plot with a keyword highlighted

1-2 dad jokes based on that keyword

A snarky comment based on the movie's rating

🛠️ Installation & Setup
Requirements
Python 3.7+

requests_with_caching module (provided)

Internet connection not required (uses cached API results)

File Structure
main.py - main application logic

requests_with_caching.py - caching utility for API requests

permanent_cache.json - cached responses from OMDb and icanhazdadjoke

 How to Use
python
Copy
Edit
print(haha_me("Back to the Future"))
Sample Output:

vbnet
Copy
Edit
Back to the Future  
Rotten Tomatoes rating: 93%  
Marty McFly, a 17-year-old high school student, is **accidentally** sent 30 years into the past...  
Speaking of **accidentally**, that reminds me of some jokes.  
Hope they're as good as the movie!

I accidentally drank a bottle of invisible ink. Now I'm in hospital, waiting to be seen.  
A butcher accidentally backed into his meat grinder and got a little behind in his work that day.
Functions Overview
get_movie_data(title) - Fetches movie info from OMDb.

rt_rating(movie_data) - Extracts Rotten Tomatoes score.

get_joke_data(term) - Gets 1-2 dad jokes containing the term.

get_jokes(plot_string) - Finds longest joke-worthy keyword from plot.

highlight(word, sentence) - Bold-highlights the keyword in the plot.

haha_me(movie_title) - The final mashup generator.

 Limitations:
Only supports movies and search terms found in the permanent_cache.json.

Will return a fallback message if no jokes are found or movie is missing.



