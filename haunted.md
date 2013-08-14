# Introducing Haunted: Headless Analytics Validation

At a fast-growing media company like Business Insider, keeping accurate analytics is absolutely essential. Editors rely on our analytics dashboard to manage content throughout the site and advertisers need essential information on our performance. Therefore, on the tech team, maintaining accurate metrics is a top priority.

To ensure that our analytics are properly firing, we built a custom system in Node.js to monitor the site, including development builds through Jenkins. Today, we are releasing that tool to the community as an NPM package called [Haunted](https://github.com/businessinsider/haunted). Using it, you can validate your analytics at the browser and database level.

Analytics validation at the browser level is done using [CasperJS](http://casperjs.org/). Given a set of URLs which you expect to be called (the set of tracking pixels you use), Haunted checks to make sure that resources are actually called.

Additionally, Haunted can reach into your database and check that any analytics fields which should be incremented actually are. While Haunted only ships with a datastore driver for MongoDB, it is designed in an extensible way for you to add your own drivers for other datastores.

Haunted is available on [GitHub](https://github.com/businessinsider/haunted) under the MIT license, and we encourage you to submit pull requests. As Business Insider scales to handle increasing traffic, we on the engineering team look forward to sharing more tips and tools. And we're always looking for more people to [join us](mailto:tech@businessinsider.com).