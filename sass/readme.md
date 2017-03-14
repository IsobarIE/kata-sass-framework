BASE FOLDER

The base/ folder holds isobar's custom reset file (based on Normalize.css v5), print and font-face/typographic rules etc.

_isobar-reset.scss
_print.scss
_typography.scss

LAYOUT FOLDER

The layout/ folder contains everything that takes part in laying out the site. This folder should have stylesheets for the main structural or global parts of the site (header, footer, navigation, sidebar etc) and default styles for forms.

_header.scss
_footer.scss
_sidebar.scss
_forms.scss
_navigation.scss
_structure.scss


COMPONENTS FOLDER

For smaller components, there is the components/ folder which is more focused on widgets than larger sections of the layout. It contains smaller modules like a carousel, loader, buttons etc. There are usually a lot of files in components/ since the whole site/application should be mostly composed of tiny modules.

_buttons.scss
_carousel.scss


PAGES FOLDER

If you have page-specific styles, it is better to put them in a pages/ folder, in a file named after the page. For instance, it’s not uncommon to have very specific styles for the home page hence the need for a _home.scss file in pages/.

_home.scss
_contact.scss


UTILS FOLDER

The utils/ folder contains all Sass tools and helpers used across the project. Every global variable, function, mixin and placeholder should be put in here.

The rule of thumb for this folder is that it should not output a single line of CSS when compiled on its own.

_grid.scss (Susy)
_variables.scss
_mixins.scss

MAIN FILE

The main file (usually labelled main.scss) should be the only Sass file from the whole code base not to begin with an underscore. This file should not contain anything but @import and comments.

Files should be imported according to the folder they live in, one after the other in the following order:

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
