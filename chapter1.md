S
ite Architecture
Server-side Routing
Through a custom .htaccess rule, all site requests redirect to a single PHP page called router.php. Browsing to any site page invokes router.php.

This critical file performs eight key functions:

Loads the boot.php include file, providing access to critical functions.
Starts a PHP session.
Translates the typed URL into a path, based on a simple set of rules (defined below).
Performs access control.
Runs performance testing, if enabled.
Loads template files, if applicable.
Loads the requested page.
Loads a 404 page when the user supplies invalid paths.
Routing Rules
Basic Logic

The routing system can handle paths with any number of directories (terms). A single term path might look like this:

online.usfsp.edu/login

A two-term path:

online.usfsp.edu/admin/reports

A three-term path:

online.usfsp.edu/admin/edit/chat

Regardless of the number of terms in the path, the final term always becomes a filename with a .php extension. Therefore, the previous examples would resolve as follows:

online.usfsp.edu/login.php online.usfsp.edu/admin/reports.php online.usfsp.edu/admin/edit/chat.php

For example, if the user types online.usfsp.edu/admin/reports, the system looks for a file called reports.php in a folder called admin.

The system always disregards trailing slashes. The following two URLs, for example, are equivalent:

online.usfsp.edu/admin/edit/chat online.usfsp.edu/admin/edit/chat/

Query Strings

Any time the final term in a path is an integer, the system automatically appends it to the end of a URL as a query string value assigned to a variable called id. For example:

online.usfsp.edu/admin/edit/chat/4234

Becomes:

online.usfsp.edu/admin/edit/chat.php?id=4234

Custom query strings can still be used. For example:

online.usfsp.edu/login/?account=none

Becomes:

online.usfsp.edu/login.php?account=none

Display vs. Process Pages

All site pages can be grouped two ways: display pages that visitors access directly and process pages that they access indirectly.

Display pages always load header.php and footer.php template files, and these files link to CSS and JS. They also provide boilerplate HTML.

Process pages never load template files. An example process page is chatManger.php, a page accessed via client-side AJAX calls.

The system classifies pages -- and therefore determines whether to load template files -- based on the presence or absence of the term "process" in the path. If the term appears, the requested page is assumed to be a process page, and no template files are loaded. For example:

online.usfsp.edu/process/login

Resolves to:

online.usfsp.edu/process/login.php

Meanwhile, router.php will not load template files for this page.

In cases where a display page has a companion process page (for example, a login form with an accompanying action page), the same filename is used, in this case, login.php. The files appear in different places: One is in the site root, the other in the /process directory.

HTML Structure
All web pages load with the fewest number of HTTP requests possible. Every display page loads a single, compressed JavaScript file and a single, compressed CSS file.

CSS
JS
