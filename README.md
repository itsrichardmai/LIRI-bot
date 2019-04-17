For this week of class, we learned to utilize node packages like axios, node-spotify-api, fs and more. 
We learned that it would be more effective to utilize separate modules/.js files to organize our code.

running "node liri.js <2> <3>" 
<2> and <3> being placeholders for the arguments passed in. 
line 8 in LIRI.js var category = process.argv[2]; serves as our logic to tell the application what to do going forward. If category is "band", run the bandSearch(); function
If category is "spotify", run the spotifySearch() function. 
If the category is "movie" run the movieSearch() function.

Used axios to manage API calls.

Case1: node liri.js spotify <"songname">
Expected: displays songname, populariity, album

Case2: node liri.js movie <"moviename">
Expected:            
            console.log("Title: " + response.data.Title);
            console.log("Year: " + response.data.Year);
            console.log("IMBD Rating: " + response.data.imdbRating);
            console.log(response.data.Ratings[1].Source + ": " + response.data.Ratings[1].Value)
            console.log("Country: " + response.data.Country);
            console.log("Language: " + response.data.Language);
            console.log("Plot: " + response.data.Plot);
            console.log("Actors: " + response.data.Actors);

Case3: node liri.js band <"bandname">
Expected: 
             console.log(response.data[0].venue.name);
            console.log(response.data[0].venue.country + ", " + response.data[0].venue.city);
            console.log(moment(response.data[0].datetime).format("L"));

        