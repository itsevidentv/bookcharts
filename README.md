Hello & welcome to yr very own bookchart!

-- EDITING --

Using this is pretty simple. The only file(s) you'll need to update are those for individual years in the markers folder. To do that, click on the file (e.g. 'markers-2026.js') and click the pen icon to edit. To add a new book, add a comma to the end of the previous line (important!), then add a new line: 

{name:"X", position:{top:"Y%", left:"Z%"}, color:"A"}

X = title of book

Y = vertical axis. 0 - something to say, 100 - nothing.

Z = horizontal axis. 0 - said it badly, 100 - said it well.

A = category. Pick from fic, nonfic, poetry, or other.

-- ADDING --

If you want to add a new year, you absolutely can! You'll have to do a few things: 

1. In the markers folder, create a new file - markers-YYYY.js. I've made dummy examples but just in case, the file should contain the following code:

		const markersYYYY = [

		];

2. In the markers.js file, add another year to the code, following the same format as the other years.

		YYYY: typeof markersYYYY !== "undefined" ? markersYYYY : []

3. In the index.html file, look for <div id="sidebar"> and add a new label for the year:
   
		<label><input type="checkbox" data-year="YYYY"> YYYY</label>

-- CUSTOMISING --

If you want to change colours, look for /* Marker fill */ in the index.html file. Change the hex codes:

		.marker-fic { background: #EC9165; }
		.marker-nonfic { background: #6c9d66; }
		.marker-poetry { background: #4c8493; }
		.marker-other { background: #df9097; }

If you want to change the fonts, the two currently used are Solway for the sidebar and Rethink Sans for the book titles. 

