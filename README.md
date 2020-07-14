# jQuery-withAjax-GeoNames-App
Geonames app displays a few Wikipedia articles from locations near to a user-entered US zip code

The page presents a simple form into which the user can type a US zip code and, below the form, an empty unordered list.

We add a jQuery ready handler and, within it, a handler to respond to submissions of the form.

When the form is submitted, we make an Ajax request to Geonames:

The first, base, part of the URL we specify with the url parameter of the $.ajax call.
We hardcode the country, radius, and username params via the data hash param; as above, we registered an account with username "webucator" for this example.
We get the postalcode param from the value entered by the user in the #zip field.
On successful retrieval of data from Geonames, we first set ul#results to empty, to clear out previous results (if any), then iterate over the result set, building a list item (with title and link to corresponding Wikipedia entry) for each returned result and appending to the unordered list.
