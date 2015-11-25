## Overview

This repository contains a website for *OpenSearch search engine definitions* that can be added to the web browser as search engines via the website.

Available at:  
http://gima.github.io/opensearch/


## Contributing

If the search engine that you wish to add already provides an OpenSearch xml file, you only need add it's url to the [`index.html`](https://github.com/gima/opensearch/blob/gh-pages/index.html).

Otherwise you need to create one. It's probably easiest to make a copy of one of the provided xml's and modify it. Then add it to the index as instructed above.

#### Example:

Search Engine [DuckDuckGo's HTML version](https://duckduckgo.com/html) has opensearch definition xml file in it's source code:

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
