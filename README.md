# Wiki2HTML
Convert a MediaWiki source document e.g. in Wikiversity into a HTML document output. The input value can be set by the Link parameters.

    wiki2html.html?title=Swarm_intelligence&server=http://en.wikiversity.org

## Call of MediaWiki API
The following URL is an example call for retrieving the source of an MediaWiki article:

 http://en.wikiversity.org/w/index.php?title=Swarm_intelligence&action=raw

The call retrieves the article about ___Swarm intelligence___ from the english  Wikiversity.

* The abbreviation ___en___ is the language
* ___wikiversity.org___ defines the Wiki product by the domain name. This can be replaced e.g. by ___wikipedia.org___, to download the corresponding article in Wikipedia instead of the learning resource in Wikiversity.
* addessing the API is performed by  ___/w/index.php___. To read the corresponding article in the browser the users will use the URL
 https://en.wikiversity.org/wiki/Swarm_intelligence
* The API call above has to parameters with key-value pairs.
  * ___title=Swarm_intelligence___ for the definition of the title
  * ___action=raw___ to get the raw sources of the article in the Wiki syntax

## Images Download wget

* The link ___https://en.wikipedia.org/wiki/Special:Redirect/file/Annweiler_Rathaus.JPG___ refers to the current version of the image ___Annweiler_Rathaus.JPG___.
* Size of image can be determined by ___http://en.wikipedia.org/wiki/Special:FilePath/Annweiler_Rathaus.JPG?width=300___ (here resize the width to 300 pixels.


## Generate an AJAX Call in HTML5 Environment

## Acknowledgements
Special thanks to  [Elia Contini](http://eliacontini.info/) for sharing the regular expressions for parsing the MediaWiki input file for processing and compiling into HTML5 under [GNU GPL 3](http://www.gnu.org/licenses/gpl.html).

## Use Tools for the repository
* [Grunt](https://gruntjs.com/getting-started) to automate code generation from modular javascript libraries to a WebApp in the folder ___/docs___. The folder ___/docs___ is used to access the WebApp directly in your browser by the URL
 https://niebert.github.io/Wiki2Reveal
 * [Browserify] to combine modular Javascript libraries for use in a browser. This is necessary because the browser does not understand the ___require(...)___ of NodeJS. Browserify parses the libraries and library dependencies and replaces the ___require___-command by an aggregated script call of used javascript sources for the WebApp.  
