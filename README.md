## Overview

This repository contains a website that lists search engines, which can be added to the web browser by clicking on them.

Website available at:  
http://gima.github.io/opensearch/


## Contributing

If the search engine that you wish to add already provides an *OpenSearch search engine definition* xml file, you only need add it's url to the [`index.html`](docs/index.html).

Otherwise you need to create one. It's probably easiest to make a copy of one of the provided xml's and modify it. Then add it to the index as instructed above.

#### Example:

The search engine [DuckDuckGo's HTML version](https://duckduckgo.com/html) has OpenSearch definition xml file in it's source:

~~~html
<link .. type="application/opensearchdescription+xml" rel="search" href="/opensearch_html.xml">
~~~

And thus the OpenSearch definition file's url becomes: [`https://duckduckgo.com/opensearch_html.xml`](https://duckduckgo.com/opensearch_html.xml)

Then to add it to the `index.html`:

~~~diff
   n("https://en.wikipedia.org/w/opensearch_desc.php")
   n("http://caniuse.com/opensearch.xml")
+  n("https://duckduckgo.com/opensearch_html.xml")
 })
~~~
