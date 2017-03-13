BASE FOLDER

The base/ folder holds the reset file, font-face/typographic rules etc.

_reset.scss
_typography.scss

LAYOUT FOLDER

The layout/ folder contains everything that takes part in laying out the site or application. This folder should have stylesheets for the main parts of the site (header, footer, navigation, sidebar etc) and CSS styles for all the forms.

_header.scss
_footer.scss
_sidebar.scss
_forms.scss
_navigation.scss


COMPONENTS FOLDER

For smaller components, there is the components/ folder. While layout/ is macro (defining the global wireframe), components/ is more focused on widgets. It contains all kind of specific modules like a slider, a loader, a widget, and basically anything along those lines. There are usually a lot of files in components/ since the whole site/application should be mostly composed of tiny modules.

_media.scss
_carousel.scss
_thumbnails.scss


PAGES FOLDER

If you have page-specific styles, it is better to put them in a pages/ folder, in a file named after the page. For instance, it’s not uncommon to have very specific styles for the home page hence the need for a _home.scss file in pages/.

_home.scss
_contact.scss


UTILS FOLDER

The utils/ folder gathers all Sass tools and helpers used across the project. Every global variable, function, mixin and placeholder should be put in here.

The rule of thumb for this folder is that it should not output a single line of CSS when compiled on its own. These are nothing but Sass helpers.

_variables.scss
_mixins.scss
_functions.scss
_placeholders.scss (frequently named _helpers.scss)


VENDORS FOLDER

And last but not least, most projects will have a vendors/ folder containing all the CSS files from external libraries and frameworks – Normalize, Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to say “Hey, this is not from me, not my code, not my responsibility”.

_normalize.scss
_bootstrap.scss
_jquery-ui.scss
_select2.scss

MAIN FILE

The main file (usually labelled main.scss) should be the only Sass file from the whole code base not to begin with an underscore. This file should not contain anything but @import and comments.

Files should be imported according to the folder they live in, one after the other in the following order:

vendors/
utils/
base/
layout/
components/
pages/

In order to preserve readability, the main file should respect these guidelines:

one file per @import;
one @import per line;
no new line between two imports from the same folder;
a new line after the last import from a folder;
file extensions and leading underscores omitted.
