UniUnitsData
============

Data repository for http://www.uniunits.co.uk

## Add a new content
You can add new units and universities to the site by forking this repo, making changes, and submitting a pull request.

The university id scheme is a 3 digit base 36 number 000..001...002... ...009...00A...00B...00C... ...00Z...010...011... etc, passed through rot18 as found at http://jsfiddle.net/Jamedjo/bTLjW/

This helps the keep the URL slug short and looking like text so people don't think about the ordering. (36^3=46656, so should be plenty). This also means that the name of the university isn't used so you can correct the name of a uni without worrying about it breaking any URLs.

## Units
Units should have an id unique to that university, a title, and potentially other meta-data which can be used in a search/filter. Ideally the id will be the same one the university uses internally.

## TODO:
In the future I will add a tag system for units, so they can be tagged as part of a course, and so that units in a uni can be filtered by course.
I will decide on a format for metadata such as year-of-study which is currently referred to as `stage`, and for other things like that. The year the student is giving feedback on will dealt with in the commenting system, but might need some metadata to say what years the course was run between.
