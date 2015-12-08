# Where are all the features?

Tail Blazer will in due course have all the usual features which can be expected of any file tailing utility plus much more.  For a full list of planned features see [issues](https://github.com/RolandPheasant/TailBlazer/issues) and if there are any features which you would expect Tail Blazer to have but are not already listed, feel free to raise a new issue.  However for now, the reason I have not pushed forward with implementing features is I have wanted to get the architecture right first and foremost as I want a rock solid foundation before the structures are built.  That point has now been reached so the features will start appearing in the near future.

So where is the project at? To answer that I have gathered great feedback from many test users and I see a range of different usage scenarios which Tail Blazer must cover. These are listed below and each of the scenarios has now been addressed.

## Watch log files when I debug my code

This was address in version 0.1 where new lines are added to the end of the display and the new lines are highlighted to draw attention to the event.

## Very large file handling

The support team in the company I work for have folders full of 10-20 Gigabyte files filled every day from a very intensive market data pricing system.  When they have to analyse these files the problems which they are looking for could be anywhere in the file so it is important to be able to find data in any part of the file.  This is why I have not imposed a limit on file size.

![Very large file](https://github.com/RolandPheasant/TailBlazer/blob/master/Images/VeryLargeFile.gif)

As you can see the 5 gig file opened in moments and scrolling is quick and smooth.  In such large files the line numbers are an estimate so may not be totally accurate.  The search function will take time. There is no getting around the fact that scanning a file line by line is a time consuming process. 


## Rapidly changing file

Another system in the same company produces a 10 Megabyte file every minute then rolls over. 

![Very fast file](https://github.com/RolandPheasant/TailBlazer/blob/master/Images/VeryFastFile.gif)

This image illustrates that even when a a file is changing rapidly the user interface is still very smooth.


## Low memory usage

For each of the files above the only lines in memory are those displayed on the screen.  The file search function necessitates recording the starting position of each line which matches the search text.  In a very large file if there are millions of lines matches memory usage can be massive so for now I have arbitrarily limited search results to 50k lines. I have some ideas about how to circumvent this limitation and also how to allow the user some control over such matter. 


## Further performance work and feedback

If you want to try it out, you can get the latest version from [releases](https://github.com/RolandPheasant/TailBlazer/releases). Extract the file and double click TailBlazer.exe

I would appreciate some feed back on how you get on with Tail Blazer, whether good or bad!
