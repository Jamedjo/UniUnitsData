UniUnitsData
============

Data repository for http://www.uniunits.co.uk

## Add a new content
You can add new units and universities to the site by forking this repo, making changes, and submitting a pull request.

### ID scheme
The university id scheme is a 3 digit base 36 number 000..001...002... ...009...00A...00B...00C... ...00Z...010...011... etc, passed through rot18 as found at http://jsfiddle.net/Jamedjo/bTLjW/

This helps the keep the URL slug short and looking like text so people don't think about the ordering. (36^3=46656, so should be plenty). This also means that the name of the university isn't used so you can correct the name of a uni without worrying about it breaking any URLs.

## Units
Units should have an id unique to that university, a title, and potentially other meta-data which can be used in a search/filter. Ideally the id will be the same one the university uses internally.

## TODO:
In the future I will add a tag system for units, so they can be tagged as part of a course, and so that units in a uni can be filtered by course.
I will decide on a format for metadata which could be added.

### Potential Meta-data
 * Year-of-study which is currently referred to as `stage`. E.g. 3rd year
 * Calender year the feedback relates to will be stored in a database, but having a record of which years each unit was taken in would help the interface only display year the course was actually run.
 * We could also add FB group links for course/unit/uni so that units you take could be auto recommended.
 * Valid institution email domains for each university

